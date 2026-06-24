---
layout: page
title: Events
permalink: /events
search_exclude: true
has_toc: false
---

<style> span.hidden {visibility: hidden;} </style>

<style>
    table th:first-of-type {
        width: 50%;
    }
    table th:nth-of-type(2) {
        width: 50%;
    }
</style>

***

<h2 id="event_list">List of all events in Figura</h2>

| Rendering Events                                                | Client Inputs                                                         |
| ----------------------------------------------------------      | --------------------------------------------------------------------- |
| [ENTITY_INIT]({{ "/events/full#ENTITY_INIT" | relative_url }})             | [CHAT_SEND_MESSAGE]({{ "/events/full#ENTITY_INIT" | relative_url }})       |
| [TICK]({{ "/events/full#TICK" | relative_url }})                           | [CHAT_RECEIVE_MESSAGE]({{ "/events/full#TICK" | relative_url }}) |
| [WORLD_TICK]({{ "/events/full#WORLD_TICK" | relative_url }})               | [MOUSE_SCROLL]({{ "/events/full#WORLD_TICK" | relative_url }})                 |
| [RENDER]({{ "/events/full#RENDER" | relative_url }})                       | [MOUSE_MOVE]({{ "/events/full#RENDER" | relative_url }})                     |
| [POST_RENDER]({{ "/events/full#POST_RENDER" | relative_url }})             | [MOUSE_PRESS]({{ "/events/full#POST_RENDER" | relative_url }})                   |
| [WORLD_RENDER]({{ "/events/full#WORLD_RENDER" | relative_url }})           | [KEY_PRESS]({{ "/events/full#WORLD_RENDER" | relative_url }})                       |
| [POST_WORLD_RENDER]({{ "/events/full#POST_WORLD_RENDER" | relative_url }}) | [CHAR_TYPED]({{ "/events/full#POST_WORLD_RENDER" | relative_url }})                     |
| [SKULL_RENDER]({{ "/events/full#SKULL_RENDER" | relative_url }})           | [USE_ITEM]({{ "/events/full#SKULL_RENDER" | relative_url }})                         |
| [ARROW_RENDER]({{ "/events/full#ARROW_RENDER" | relative_url }})           | [ON_PLAY_SOUND]({{ "/events/full#ARROW_RENDER" | relative_url }})               |
| [ITEM_RENDER]({{ "/events/full#ITEM_RENDER" | relative_url }})             | [RESOURCE_RELOAD]({{ "/events/full#ITEM_RENDER" | relative_url }})           |