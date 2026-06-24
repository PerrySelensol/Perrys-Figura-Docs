---
layout: page
parent: Events
title: All Events
permalink: /figura-docs/events/full
nav_order: 2
---

<center style="font-size: 3em;">Events</center>

***

<h1 id="ENTITY_INIT" style="font-size: 2.5em;color:#00008B">ENTITY_INIT</h1>

```lua
events.ENTITY_INIT:register(
    function()
        ...
    end
)
```

Functions registered to this event are called once the player entity is loaded in a view for the first time (i.e. they aren't called until people are close to you.)

&nbsp;

***

<h1 id="TICK" style="font-size: 2.5em;color:#00008B">TICK</h1>

```lua
events.TICK:register(
    function()
        ...
    end
)
```

Functions registered to this event are called every game tick if the player entity is loaded in a view (i.e. they aren't called until people are close to you.)

&nbsp;

***

<h1 id="WORLD_TICK" style="font-size: 2.5em;color:#00008B">WORLD_TICK</h1>

```lua
events.WORLD_TICK:register(
    function()
        ...
    end
)
```

Functions registered to this event are called every game tick regardless of player being loaded.

&nbsp;

***

<h1 id="RENDER" style="font-size: 2.5em;color:#00008B">RENDER</h1>

```lua
events.RENDER:register(
    function(delta, context, source_matrix)
        ...
    end
)
```

Functions registered to this event are called every frame, **before** the avatar is rendered.

The functions receive these parameters on being called:

- A *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

- A *string* `context` giving out context of the current RenderMode, with is a string with the name of the source of this render event.

- A *matrix4* `source_matrix` used to render the Avatar.

&nbsp;

***

<h1 id="POST_RENDER" style="font-size: 2.5em;color:#00008B">POST_RENDER</h1>

```lua
events.POST_RENDER:register(
    function(delta, context, source_matrix)
        ...
    end
)
```

Functions registered to this event are called every frame, **after** the avatar is rendered.

The functions receive these parameters on being called:

- A *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

- A *string* `context` giving out context of the current RenderMode, with is a string with the name of the source of this render event.

- A *matrix4* `source_matrix` used to render the Avatar.

&nbsp;

***

<h1 id="WORLD_RENDER" style="font-size: 2.5em;color:#00008B">WORLD_RENDER</h1>

```lua
events.WORLD_RENDER:register(
    function(delta)
        ...
    end
)
```

Functions registered to this event are called every frame, **before** the world is rendered.

On being called, the functions receive a *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

&nbsp;

***

<h1 id="POST_WORLD_RENDER" style="font-size: 2.5em;color:#00008B">POST_WORLD_RENDER</h1>

```lua
events.POST_WORLD_RENDER:register(
    function(delta)
        ...
    end
)
```

Functions registered to this event are called every frame, **after** the world is rendered.

On being called, the functions receive a *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

&nbsp;

***

<h1 id="CHAT_SEND_MESSAGE" style="font-size: 2.5em;color:#00008B">CHAT_SEND_MESSAGE</h1>

```lua
events.CHAT_SEND_MESSAGE:register(
    function(message)
        ...
        return new_sent_message
    end
)
```

Functions registered to this event will run every time you send a message in chat.

A *string* `message` parameter is received which is the message entered in the chat box.

The functions can be made to return a string which will be the message that is actually being sent instead of the message in chat box (if allowed in settings.) This means a function returning **nil** prevents the message from being sent at all.

When multiple functions return their string at the same time, **the last function registered to this event** will get its string sent to chat.

&nbsp;

***

<h1 id="CHAT_RECEIVE_MESSAGE" style="font-size: 2.5em;color:#00008B">CHAT_RECEIVE_MESSAGE</h1>

```lua
events.CHAT_RECEIVE_MESSAGE:register(
    function(message, json_message)
        ...
        return new_receieved_message, background_color
    end
)
```

Functions registered to this event will run every time a message is received in chat. 

The functions receive these parameters on being called:

- A *string* `message` which is the raw string of the received text.

- A *string* `json_message` which is a JSON string representation of the received text.

The functions can be made to return two values:

- A *string* which is a new message replacing the original received message. Returning **false** will prevent the message from being receieved in the chat screen

- A *vector4* in a normalized RGBA format which is used as background color for this message.

When multiple functions return their string at the same time, **the first function registered to this event** will get its return values used.

&nbsp;

***

<h1 id="SKULL_RENDER" style="font-size: 2.5em;color:#00008B">SKULL_RENDER</h1>

```lua
events.SKULL_RENDER:register(
    function(delta, block, item, entity, render_type)
        ...
        return disable_render
    end
)
```

Functions registered to this event will be called on all player heads placed in the world.

The functions receive these parameters on being called:

- A *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

- A *blockstate* `block` when the head is rendered as a block.

- An *itemstack* `item` when the head is rendered as an item.

- An *entity* `entity` when the head is rendered from a entity.

- A *string* `render_type` which is the type of rendering.

Making the function returning **true** will make the head not render at all

&nbsp;

***

<h1 id="MOUSE_SCROLL" style="font-size: 2.5em;color:#00008B">MOUSE_SCROLL</h1>

```lua
events.MOUSE_SCROLL:register(
    function(delta)
        ...
        return disable_vanilla_action
    end
)
```

Functions registered to this event run every time the mouse is scrolled.

The functions receive a *number* `delta` which is the direction of the scroll.

If any of the functions return **true**, it will cancel vanilla scrolling action.

&nbsp;

***

<h1 id="MOUSE_MOVE" style="font-size: 2.5em;color:#00008B">MOUSE_MOVE</h1>

```lua
events.MOUSE_SCROLL:register(
    function(delta_x, delta_y)
        ...
        return disable_vanilla_action
    end
)
```

Functions registered to this event run every time the mouse is moved around.

On being called, the functions receive two *numbers*: `delta_x` and `delta_y` which is the difference from the mouse position from the latest saved position.

If any of the functions return **true**, its vanilla function will be cancelled and last mouse position will not be updated.

&nbsp;

***

<h1 id="MOUSE_PRESS" style="font-size: 2.5em;color:#00008B">MOUSE_PRESS</h1>

```lua
events.MOUSE_PRESS:register(
    function(button, action, modifier)
        ...
        return disable_vanilla_action
    end
)
```

Functions registered to this event run every time a mouse button is pressed.

The functions receive three parameters on being called:

- First *number* `button` which is the button pressed.

- Second *number* `action` which is the action of the press (0 for release, 1 for press, 2 for hold.)

- Third *number* `modifier` which is a number representing modifier key combinations being pressed (such as Shift or Alt keys.)

If any of the functions return **true**, its vanilla function will be cancelled.

&nbsp;

***

<h1 id="KEY_PRESS" style="font-size: 2.5em;color:#00008B">KEY_PRESS</h1>

```lua
events.KEY_PRESS:register(
    function(key, action, modifier)
        ...
        return disable_vanilla_action
    end
)
```

Functions registered to this event run every time a keyboard key is pressed.

The functions receive three parameters on being called:

- First *number* `button` which is the button pressed.

- Second *number* `action` which is the action of the press (0 for release, 1 for press, 2 for hold.)

- Third *number* `modifier` which is a number representing modifier key combinations being pressed (such as Shift or Alt keys.)

If any of the functions return **true**, its vanilla function will be cancelled.


&nbsp;

***

<h1 id="CHAR_TYPED" style="font-size: 2.5em;color:#00008B">CHAR_TYPED</h1>

```lua
events.CHAR_TYPED:register(
    function(char, action, codepoint)
        ...
    end
)
```

Functions registered event runs every time a character is inputted.

The functions receive three parameters on being called:

- A *string* `char` which is the button pressed.

- A *number* `modifier` which is a number representing modifier key combinations being pressed (such as Shift or Alt keys.)

- A *number* `codepoint` which is the codepoint of the inputted character.

&nbsp;

***

<h1 id="USE_ITEM" style="font-size: 2.5em;color:#00008B">USE_ITEM</h1>

```lua
events.USE_ITEM:register(
    function(item, action, particle_amount)
        ...
        return disable_vanilla_action
    end
)
```


Functions registered to this event run every time the entity uses an item.

The functions receive three parameters on being called:

- An *itemstack* `item` that is being used.

- A *string* `action`

- A *number* `particle_amount` that is amount of particles this item would produce.

If any of the functions return **true**, its vanilla function will be cancelled.


&nbsp;

***

<h1 id="ARROW_RENDER" style="font-size: 2.5em;color:#00008B">ARROW_RENDER</h1>

```lua
events.ARROW_RENDER:register(
    function(delta, entity)
        ...
        return disable_render
    end
)
```

Functions registered to this event run for every arrow entity shot by the Avatar owner. Requires "Vanilla Model Change" permission to have any effect on the arrows.

The functions receive two parameters on being called:

- A *number* `delta` from 0 to 1 indicating the proportion of the way the game is between ticks.

- An *entity* `entity` representing the arrow entity itself.

If any of the functions return **true**, the arrow and its parts will not render.

&nbsp;

***

<h1 id="ITEM_RENDER" style="font-size: 2.5em;color:#00008B">ITEM_RENDER</h1>

```lua
events.ITEM_RENDER:register(
    function(item, render_mode, pos, rot, scale, left_handed)
        ...
        return replacement_model
    end
)
```

Functions registered to this event run on all of your items that is being rendered.

The functions receive six parameters on being called:

- An *itemstack* `item` representing item itself.

- A *string* `render_mode` that is the rendering mode of the item.

- A *vector3* `pos` that is position transformation applied to the item.

- A *vector3* `rot` that is rotation transformation applied to the item.

- A *vector* `scale` that is scale transformation applied to the item.

- A *boolean* `left_handed` indicating whether or not the item is rendered from the left hand.

If a function returns a modelpart parented to item, the returned part will be rendered in place of the item.

&nbsp;

***

<h1 id="ON_PLAY_SOUND" style="font-size: 2.5em;color:#00008B">ON_PLAY_SOUND</h1>

```lua
events.ON_PLAY_SOUND:register(
    function(sound_id, pos, volume, pitch, is_looped, category, path)
        ...
    end
)
```

Functions registered to this event are called every time a new sound is played.

The functions receive these parameters on being called:

- A *string* `sound_id` that is the ID of the sound.

- A *vector3* `pos` that is its position in the world.

- A *number* `volume` that is volume of the sound.

- A *number* `pitch` that is pitch of the sound.

- A *boolean* `is_looped` that is whether or not the sound is looped.

- A *string* `category` that is category of the sound.

- A *string* `path` that is the path of the sound.


&nbsp;

***


<h1 id="RESOURCE_RELOAD" style="font-size: 2.5em;color:#00008B">RESOURCE_RELOAD</h1>

```lua
events.RESOURCE_RELOAD:register(
    function()
        ...
    end
)
```

Functions registered to this event are called every time the client resources are reloaded, allowing you to re-create or update resource texture references.
