---
layout: page
parent: Events
title: Introduction
permalink: /figura-docs/events/intro
search_exclude: true
has_toc: false
nav_order: 1
---

<center style="font-size: 3em;">Events</center>

***

Events are objects belonging to `events` table, and have an ability to call your functions when a certain event occurs.

Functions can be registered to an event as follow, using `TICK` event as an example.

```lua
function my_function()
    ... -- Your code here
end

events.TICK:register(my_function, "my_event")
```

Or as an anonymous function

```lua
events.TICK:register(
    function()
        ... -- Your code here
    end,
    "my_event"
)
```

A shortcut for this registration is to define an event as if it were a function itself.

```lua
function events.tick()
    ... -- Your code here
end
```

Note that since the shortcut syntax is essentially the same as the regular registration, you can 'define' more than one of these functions unlike other usual functions.

```lua
-- This is valid, and both will get called.

function events.tick()
    ...
end

function events.tick()
    ...
end
```