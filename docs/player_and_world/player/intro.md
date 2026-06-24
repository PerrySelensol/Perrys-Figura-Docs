---
parent: Player and Entities
nav_order: 1
layout: page
title: Introduction

search_exclude: true
has_toc: false
---

<center style="font-size: 3em;">Player and Entites</center>

***

In figura, there are four types of entities:

- `Player`: the player entity which uses this avatar;
- `LivingEntity`: living entities such as chickens, zombies;
- `Entity`: other entites such as boats, minecarts and;
- `Viewer`: the player entity of other people.

Being the most commonly used entity, `Player` is represented by a table called `player` which contains functions related to getting data of the player entity that uses this avatar.

{: .warning}
> As these functions rely on the player entity itself, they cannot be run while the player is not loaded. Thus, any call to `player` functions must be made in any of the following:
> - A call is made inside `if player:isLoaded() then ... end` block i.e. the call checks for the player first.
> - A call is made inside `ENTITY_INIT`, `TICK`, `RENDER` or `POST_RENDER` event.
>
> Not doing so will give the following error: `Tried to access the Entity API before its initialization in the ENTITY_INIT event...`
