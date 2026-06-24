---
layout: page
parent: Figura Documentation
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
| [ENTITY_INIT](/events/full#ENTITY_INIT)             | [CHAT_SEND_MESSAGE](/events/full#CHAT_SEND_MESSAGE)       |
| [TICK](/events/full#TICK)                           | [CHAT_RECEIVE_MESSAGE](/events/full#CHAT_RECEIVE_MESSAGE) |
| [WORLD_TICK](/events/full#WORLD_TICK)               | [MOUSE_SCROLL](/events/full#MOUSE_SCROLL)                 |
| [RENDER](/events/full#RENDER)                       | [MOUSE_MOVE](/events/full#MOUSE_MOVE)                     |
| [POST_RENDER](/events/full#POST_RENDER)             | [MOUSE_PRESS](/events/full#MOUSE_PRESS)                   |
| [WORLD_RENDER](/events/full#WORLD_RENDER)           | [KEY_PRESS](/events/full#KEY_PRESS)                       |
| [POST_WORLD_RENDER](/events/full#POST_WORLD_RENDER) | [CHAR_TYPED](/events/full#CHAR_TYPED)                     |
| [SKULL_RENDER](/events/full#SKULL_RENDER)           | [USE_ITEM](/events/full#USE_ITEM)                         |
| [ARROW_RENDER](/events/full#ARROW_RENDER)           | [ON_PLAY_SOUND](/events/full#ON_PLAY_SOUND)               |
| [ITEM_RENDER](/events/full#ITEM_RENDER)             | [RESOURCE_RELOAD](/events/full#RESOURCE_RELOAD)           |