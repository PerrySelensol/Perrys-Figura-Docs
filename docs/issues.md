---
layout: page
title: Common Issues
permalink: /issues
has_toc: false
nav_order: 2
---

<center style="font-size: 3em;">Common Issues</center>

***

This is a compliation of the frequent issues I have observed over time. If you're lucky, your problem might just happen to appear here.

***

<h1 id="entityapi" style="font-size: 2.5em;color:#00008B">"Tried to access the Entity API before its initialization in the ENTITY_INIT event."</h1>

This is by far the most terrifying curse that tortures many figura users with very few managed to live longer than six seconds to tell the tale. Known as "The Curse of EntityAPI," the error occurs when a function inside `player` table is called without the player entity itself loaded. The worst part? Most of the time it's others telling you that you have this error!

One of our survivors, GNanimates, has a story to tell you the moment he saw someone getting infected with the curse and trying to attack him afterwards. He too got EntityAPI'd immediately after this.
<audio controls="controls">
  <source type="audio/mp3" src='figura_stories.mp3'></source>
  <p>Your browser does not support the audio element.</p>
</audio>

## Solution
Joking aside, these are some vulnerable spots you should check out for:

### Ping functions
Any ping function that uses `player` table almost always suffer from the EntityAPI issue. The fix is to add if checks **inside** the ping function.

```lua
function pings.myPing()
    -- Some code
    if player:isLoaded() then
        -- Some code involving calling functions in player table
        pos = player:getPos()
    end
    -- The rest of the code there
end
```

or a guard clause to return the function early

```lua
function pings.myPing()
    if not player:isLoaded() then return end -- Guard clause
    -- Your code
end
```

{: .warning}
> Do not put the `player:isLoaded()` check at the ping calling, i.e. do not do this
> ```lua
> if player:isLoaded() then pings.myPing() end
> ```
> `player:isLoaded()` is almost always `true` for the host (i.e. you) Therefore you always send the ping to others no matter what. The correct solutions above let the ping be sent to people anyways, then let the ping itself decide whether or not the player is actually loaded afterwards.

### Events
Aside from `ENTITY_INIT`, `TICK`, `RENDER` and `POST_RENDER` events which never runs without the player entity being loaded, other events may run even without the player entity being loaded. Therefore you should put if checks on those player function calls as well.

```lua
-- World tick event example
local pos
function events.world_tick()
    if player:isLoaded() then
        -- player:getPos() is inside an if check; saving it from the entityapi curse
        pos = player:getPos()
    end
    if pos then
        -- More code stuffs
    end
end
```

***

<h1 id="sync_pings" style="font-size: 2.5em;color:#00008B">Sycing Variables with Pings</h1>

A mistake in using pings to sync a variable is not using the ping's arguments, as shown in these two examples:

```lua
-- Ex. #1 An attempt at syncing host:isFlying() variable
local isFlying = false
function pings.syncIsFlying()
    isFlying = host:isFlying()
end
```

```lua
-- Ex. #2 An attempt at syncing skirt with action wheel
local isWearingSkirt = false
function pings.syncSkirt()
    models.player.Skirt:setVisible(isWearingSkirt)
end

skirtAction:onLeftClick(function()
    isWearingSkirt = not isWearingSkirt
    pings.syncSkirt()
end)
```

As described in [Pings]({{ "pings" | relative_url }}), your avatar is run independently on others' computer. Therefore all variables you use in the script are also independent, i.e. with first example, your computer has your own `isFlying` variable, their computer has their own `isFlying` variable.

In the first example, when `pings.syncIsFlying` is called, `isFlying = host:isFlying()` is run fully independently on each computer; namely, `host:isFlying()` will try to get the value from whatever the computer it's being run in. Your `host:isFlying()` call will return the result correctly, but others' `host:isFlying()` call will return different result than yours (since apprently other computers can't actually tell if you're flying in creative mode or not). After an assignment, only your `isFlying` will have the correct value.

In the second example, we look at the `isWearingSkirt` variable. When your action is triggered, `isWearingSkirt = not isWearingSkirt` flips only **your** `isWearingSkirt`, so your `isWearingSkirt` is now true while others' `isWearingSkirt` stays false. Once the ping is called, `models.player.Skirt:setVisible(isWearingSkirt)` uses **each of their own** `isWearingSkirt`, which is true for you, but still false for others. Therefore only you will see your own skirt, and not others!

## Solution
These are the correct implementation for syncing variables with pings:

```lua
-- Correct Ex. #1 Syncing host:isFlying() variable
local isFlying = false
function pings.syncIsFlying(bool)
    isFlying = bool
end

function someEvent()
    pings.syncIsFlying(host:isFlying()) -- Usually call this somewhere in tick event
end
```

```lua
-- Correct Ex. #2 Syncing skirt with action wheel
local isWearingSkirt = false
function pings.syncSkirt(bool)
    models.player.Skirt:setVisible(bool)
end

skirtAction:onLeftClick(function()
    isWearingSkirt = not isWearingSkirt
    pings.syncSkirt(isWearingSkirt)
end)
```

The difference in these correct implementations here is simply the fact that ping functions take an argument. When a ping is called with arguments passed, **everyone gets the ping called with the exact same arguments as yours**. This means in the second example, `pings.syncSkirt(isWearingSkirt)` is called as `pings.syncSkirt(isWearingSkirt)` with **your** `isWearingSkirt` being used for everyone's ping call. As for the first example, `pings.syncIsFlying(host:isFlying())` first evaluates `host:isFlying()` on your computer, giving the correct value, say `true`. This `true` is then passed as an argument to everyone else's `pings.syncIsFlying` call; namely, everyone gets a `pings.syncIsFlying(true)` call.
