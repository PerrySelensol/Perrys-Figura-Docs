---
layout: page
parent: Figura Documentation
title: Player and Entities
permalink: /player
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

<center style="font-size: 3em;">Player and Entites</center>

***

In figura, there are four types of entities:

- `Player`: the player entity which uses this avatar;
- `LivingEntity`: living entities such as chickens, zombies;
- `Entity`: other entites such as boats, minecarts and;
- `Viewer`: the player entity of other people.

Being the most commonly used entity, `Player` is represented by a table called `player` which contains functions related to getting data of the player entity that uses this avatar.

The list below gives all the functions found in `player` table.

{: .warning}
> As these functions rely on the player entity itself, they cannot be run while the player is not loaded. Thus, any call to `player` functions must be made in any of the following:
> - A call is made inside `if player:isLoaded() then ... end` block i.e. the call checks for the player first.
> - A call is made inside `ENTITY_INIT`, `TICK`, `RENDER` or `POST_RENDER` event.
>
> Not doing so will give the following error: `Tried to access the Entity API before its initialization in the ENTITY_INIT event...`


| Getters                                                                       |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getAbsorptionAmount]({{ "/player/full1#getAbsorptionAmount" | relative_url }})                 | [getLookDir]({{ "/player/full1#getAbsorptionAmount" | relative_url }})                                   |
| [getActiveHand]({{ "/player/full1#getActiveHand" | relative_url }})                             | [getMaxAir]({{ "/player/full1#getActiveHand" | relative_url }})                                     |
| [getActiveItem]({{ "/player/full1#getActiveItem" | relative_url }})                             | [getMaxHealth]({{ "/player/full1#getActiveItem" | relative_url }})                               |
| [getActiveItemTime]({{ "/player/full1#getActiveItemTime" | relative_url }})                     | [getModelType]({{ "/player/full1#getActiveItemTime" | relative_url }})                               |
| [getArmor]({{ "/player/full1#getArmor" | relative_url }})                                       | [getName]({{ "/player/full1#getArmor" | relative_url }})                                         |
| [getArrowCount]({{ "/player/full1#getArrowCount" | relative_url }})                             | [getNbt]({{ "/player/full1#getArrowCount" | relative_url }})                                           |
| [getBodyYaw]({{ "/player/full1#getBodyYaw" | relative_url }})                                   | [getNearestEntity]({{ "/player/full1#getBodyYaw" | relative_url }})                       |
| [getBoundingBox]({{ "/player/full1#getBoundingBox" | relative_url }})                           | [getPassengers]({{ "/player/full1#getBoundingBox" | relative_url }})                             |
| [getChargedAttackDelay]({{ "/player/full1#getChargedAttackDelay" | relative_url }})             | [getPermissionLevel]({{ "/player/full1#getChargedAttackDelay" | relative_url }})                   |
| [getControlledVehicle]({{ "/player/full1#getControlledVehicle" | relative_url }})               | [getPos]({{ "/player/full1#getControlledVehicle" | relative_url }})                                           |
| [getControllingPassenger]({{ "/player/full1#getControllingPassenger" | relative_url }})         | [getPose]({{ "/player/full1#getControllingPassenger" | relative_url }})                                         |
| [getCooldownPercent]({{ "/player/full1#getCooldownPercent" | relative_url }})                   | [getRot]({{ "/player/full1#getCooldownPercent" | relative_url }})                                           |
| [getDeathTime]({{ "/player/full1#getDeathTime" | relative_url }})                               | [getSaturation]({{ "/player/full1#getDeathTime" | relative_url }})                             |
| [getDimensionName]({{ "/player/full1#getDimensionName" | relative_url }})                       | [getShoulderEntity]({{ "/player/full1#getDimensionName" | relative_url }})                     |
| [getEntityCategory]({{ "/player/full1#getEntityCategory" | relative_url }})                     | [getStingerCount]({{ "/player/full1#getEntityCategory" | relative_url }})                         |
| [getExhaustion]({{ "/player/full1#getExhaustion" | relative_url }})                             | [getSwingArm]({{ "/player/full1#getExhaustion" | relative_url }})                                 |
| [getExperienceLevel]({{ "/player/full1#getExperienceLevel" | relative_url }})                   | [getSwingDuration]({{ "/player/full1#getExperienceLevel" | relative_url }})                       |
| [getExperienceProgress]({{ "/player/full1#getExperienceProgress" | relative_url }})             | [getSwingTime]({{ "/player/full1#getExperienceProgress" | relative_url }})                               |
| [getEyeHeight]({{ "/player/full1#getEyeHeight" | relative_url }})                               | [getTargetedBlock]({{ "/player/full1#getEyeHeight" | relative_url }})                       |
| [getEyeY]({{ "/player/full1#getEyeY" | relative_url }})                                         | [getTargetedEntity]({{ "/player/full1#getEyeY" | relative_url }})                     |
| [getFood]({{ "/player/full1#getFood" | relative_url }})                                         | [getTeamInfo]({{ "/player/full1#getFood" | relative_url }})                                 |
| [getFrozenTicks]({{ "/player/full1#getFrozenTicks" | relative_url }})                           | [getType]({{ "/player/full1#getFrozenTicks" | relative_url }})                                         |
| [getGamemode]({{ "/player/full1#getGamemode" | relative_url }})                                 | [getUUID]({{ "/player/full1#getGamemode" | relative_url }})                                         |
| [getHealth]({{ "/player/full1#getHealth" | relative_url }})                                     | [getVariable]({{ "/player/full1#getHealth" | relative_url }})                                 |
| [getHeldItem]({{ "/player/full1#getHeldItem" | relative_url }})                                 | [getVehicle]({{ "/player/full1#getHeldItem" | relative_url }})                                   |
| [getItem]({{ "/player/full1#getItem" | relative_url }})                                         | [getVelocity]({{ "/player/full1#getItem" | relative_url }})                                 |


| Others<span class="hidden">----------------</span>                            | <span class="hidden">      </span>                                            |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [hasAvatar]({{ "/player/full2#hasAvatar" | relative_url }})                                     | [hasInventory]({{ "/player/full2#hasAvatar" | relative_url }})                               |
| [hasCape]({{ "/player/full2#hasCape" | relative_url }})                                         | [hasSkin]({{ "/player/full2#hasCape" | relative_url }})                                         |
| [hasContainer]({{ "/player/full2#hasContainer" | relative_url }})                               |                                                                               |
|                                                                               |                                                                               |
| [isAlive]({{ "/player/full2#isAlive" | relative_url }})                                         | [isMoving]({{ "/player/full2#isAlive" | relative_url }})                                       |
| [isBlocking]({{ "/player/full2#isBlocking" | relative_url }})                                   | [isOnFire]({{ "/player/full2#isBlocking" | relative_url }})                                       |
| [isClimbing]({{ "/player/full2#isClimbing" | relative_url }})                                   | [isOnGround]({{ "/player/full2#isClimbing" | relative_url }})                                   |
| [isCrouching]({{ "/player/full2#isCrouching" | relative_url }})                                 | [isPlayer]({{ "/player/full2#isCrouching" | relative_url }})                                       |
| [isFalling]({{ "/player/full2#isFalling" | relative_url }})                                     | [isSensitiveToWater]({{ "/player/full2#isFalling" | relative_url }})                   |
| [isFishing]({{ "/player/full2#isFishing" | relative_url }})                                     | [isSilent]({{ "/player/full2#isFishing" | relative_url }})                                       |
| [isGliding]({{ "/player/full2#isGliding" | relative_url }})                                     | [isSkinLayerVisible]({{ "/player/full2#isGliding" | relative_url }})                   |
| [isGlowing]({{ "/player/full2#isGlowing" | relative_url }})                                     | [isSneaking]({{ "/player/full2#isGlowing" | relative_url }})                                   |
| [isInLava]({{ "/player/full2#isInLava" | relative_url }})                                       | [isSprinting]({{ "/player/full2#isInLava" | relative_url }})                                 |
| [isInRain]({{ "/player/full2#isInRain" | relative_url }})                                       | [isSwingingArm]({{ "/player/full2#isInRain" | relative_url }})                             |
| [isInvisible]({{ "/player/full2#isInvisible" | relative_url }})                                 | [isUnderwater]({{ "/player/full2#isInvisible" | relative_url }})                               |
| [isInWater]({{ "/player/full2#isInWater" | relative_url }})                                     | [isUsingItem]({{ "/player/full2#isInWater" | relative_url }})                                 |
| [isLeftHanded]({{ "/player/full2#isLeftHanded" | relative_url }})                               | [isVisuallySwimming]({{ "/player/full2#isLeftHanded" | relative_url }})                   |
| [isLiving]({{ "/player/full2#isLiving" | relative_url }})                                       | [isWet]({{ "/player/full2#isLiving" | relative_url }})                                             |
| [isLoaded]({{ "/player/full2#isLoaded" | relative_url }})                                       |                                                                               |













