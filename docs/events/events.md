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
| [ENTITY_INIT](full#ENTITY_INIT)             | [CHAT_SEND_MESSAGE](full#ENTITY_INIT)       |
| [TICK](full#TICK)                           | [CHAT_RECEIVE_MESSAGE](full#TICK) |
| [WORLD_TICK](full#WORLD_TICK)               | [MOUSE_SCROLL](full#WORLD_TICK)                 |
| [RENDER](full#RENDER)                       | [MOUSE_MOVE](full#RENDER)                     |
| [POST_RENDER](full#POST_RENDER)             | [MOUSE_PRESS](full#POST_RENDER)                   |
| [WORLD_RENDER](full#WORLD_RENDER)           | [KEY_PRESS](full#WORLD_RENDER)                       |
| [POST_WORLD_RENDER](full#POST_WORLD_RENDER) | [CHAR_TYPED](full#POST_WORLD_RENDER)                     |
| [SKULL_RENDER](full#SKULL_RENDER)           | [USE_ITEM](full#SKULL_RENDER)                         |
| [ARROW_RENDER](full#ARROW_RENDER)           | [ON_PLAY_SOUND](full#ARROW_RENDER)               |
| [ITEM_RENDER](full#ITEM_RENDER)             | [RESOURCE_RELOAD](full#ITEM_RENDER)           |