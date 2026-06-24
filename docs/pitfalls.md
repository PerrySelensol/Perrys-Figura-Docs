---
layout: page
parent: Figura Documentation
title: Common Issues
permalink: /issues
has_toc: false
nav_order: 1
---

<center style="font-size: 3em;">Common Issues</center>

***

This is a compliation of the frequent errors I have observed over time. If you're lucky, your problem might just happen to appear here.

***

<h1 id="entityapi" style="font-size: 2.5em;color:#00008B">"Tried to access the Entity API before its initialization in the ENTITY_INIT event."</h1>

This is by far the most terrifying curse that tortures many figura users with very few managed to live longer than six seconds to tell the tale. Known as "The Curse of EntityAPI," the error occurs when a function inside `player` table is called without the player entity itself loaded. The worst part? Most of the time it's others telling you that you have this error!

## Solution
These are vulnerable spots you should check at

### Ping functions
Any ping function that uses `player` table is almost always a prey of EntityAPI curse. The fix is to add if checks **inside** the ping function.

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

or with a guard clause to return the function early

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