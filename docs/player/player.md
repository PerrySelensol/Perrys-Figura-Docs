---
layout: page
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
| [getAbsorptionAmount](full1#getAbsorptionAmount)                 | [getLookDir](full1#getAbsorptionAmount)                                   |
| [getActiveHand](full1#getActiveHand)                             | [getMaxAir](full1#getActiveHand)                                     |
| [getActiveItem](full1#getActiveItem)                             | [getMaxHealth](full1#getActiveItem)                               |
| [getActiveItemTime](full1#getActiveItemTime)                     | [getModelType](full1#getActiveItemTime)                               |
| [getArmor](full1#getArmor)                                       | [getName](full1#getArmor)                                         |
| [getArrowCount](full1#getArrowCount)                             | [getNbt](full1#getArrowCount)                                           |
| [getBodyYaw](full1#getBodyYaw)                                   | [getNearestEntity](full1#getBodyYaw)                       |
| [getBoundingBox](full1#getBoundingBox)                           | [getPassengers](full1#getBoundingBox)                             |
| [getChargedAttackDelay](full1#getChargedAttackDelay)             | [getPermissionLevel](full1#getChargedAttackDelay)                   |
| [getControlledVehicle](full1#getControlledVehicle)               | [getPos](full1#getControlledVehicle)                                           |
| [getControllingPassenger](full1#getControllingPassenger)         | [getPose](full1#getControllingPassenger)                                         |
| [getCooldownPercent](full1#getCooldownPercent)                   | [getRot](full1#getCooldownPercent)                                           |
| [getDeathTime](full1#getDeathTime)                               | [getSaturation](full1#getDeathTime)                             |
| [getDimensionName](full1#getDimensionName)                       | [getShoulderEntity](full1#getDimensionName)                     |
| [getEntityCategory](full1#getEntityCategory)                     | [getStingerCount](full1#getEntityCategory)                         |
| [getExhaustion](full1#getExhaustion)                             | [getSwingArm](full1#getExhaustion)                                 |
| [getExperienceLevel](full1#getExperienceLevel)                   | [getSwingDuration](full1#getExperienceLevel)                       |
| [getExperienceProgress](full1#getExperienceProgress)             | [getSwingTime](full1#getExperienceProgress)                               |
| [getEyeHeight](full1#getEyeHeight)                               | [getTargetedBlock](full1#getEyeHeight)                       |
| [getEyeY](full1#getEyeY)                                         | [getTargetedEntity](full1#getEyeY)                     |
| [getFood](full1#getFood)                                         | [getTeamInfo](full1#getFood)                                 |
| [getFrozenTicks](full1#getFrozenTicks)                           | [getType](full1#getFrozenTicks)                                         |
| [getGamemode](full1#getGamemode)                                 | [getUUID](full1#getGamemode)                                         |
| [getHealth](full1#getHealth)                                     | [getVariable](full1#getHealth)                                 |
| [getHeldItem](full1#getHeldItem)                                 | [getVehicle](full1#getHeldItem)                                   |
| [getItem](full1#getItem)                                         | [getVelocity](full1#getItem)                                 |


| Others<span class="hidden">----------------</span>                            | <span class="hidden">      </span>                                            |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [hasAvatar](full2#hasAvatar)                                     | [hasInventory](full2#hasAvatar)                               |
| [hasCape](full2#hasCape)                                         | [hasSkin](full2#hasCape)                                         |
| [hasContainer](full2#hasContainer)                               |                                                                               |
|                                                                               |                                                                               |
| [isAlive](full2#isAlive)                                         | [isMoving](full2#isAlive)                                       |
| [isBlocking](full2#isBlocking)                                   | [isOnFire](full2#isBlocking)                                       |
| [isClimbing](full2#isClimbing)                                   | [isOnGround](full2#isClimbing)                                   |
| [isCrouching](full2#isCrouching)                                 | [isPlayer](full2#isCrouching)                                       |
| [isFalling](full2#isFalling)                                     | [isSensitiveToWater](full2#isFalling)                   |
| [isFishing](full2#isFishing)                                     | [isSilent](full2#isFishing)                                       |
| [isGliding](full2#isGliding)                                     | [isSkinLayerVisible](full2#isGliding)                   |
| [isGlowing](full2#isGlowing)                                     | [isSneaking](full2#isGlowing)                                   |
| [isInLava](full2#isInLava)                                       | [isSprinting](full2#isInLava)                                 |
| [isInRain](full2#isInRain)                                       | [isSwingingArm](full2#isInRain)                             |
| [isInvisible](full2#isInvisible)                                 | [isUnderwater](full2#isInvisible)                               |
| [isInWater](full2#isInWater)                                     | [isUsingItem](full2#isInWater)                                 |
| [isLeftHanded](full2#isLeftHanded)                               | [isVisuallySwimming](full2#isLeftHanded)                   |
| [isLiving](full2#isLiving)                                       | [isWet](full2#isLiving)                                             |
| [isLoaded](full2#isLoaded)                                       |                                                                               |













