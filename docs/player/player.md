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
> Not doing so will give the following error: `Tried to access Entity API before its initialization in the ENTITY_INIT event...`


| Getters                                                                       |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getAbsorptionAmount](/player/full1#getAbsorptionAmount)                 | [getLookDir](/player/full1#getLookDir)                                   |
| [getActiveHand](/player/full1#getActiveHand)                             | [getMaxAir](/player/full1#getMaxAir)                                     |
| [getActiveItem](/player/full1#getActiveItem)                             | [getMaxHealth](/player/full1#getMaxHealth)                               |
| [getActiveItemTime](/player/full1#getActiveItemTime)                     | [getModelType](/player/full1#getModelType)                               |
| [getArmor](/player/full1#getArmor)                                       | [getName](/player/full1#getName)                                         |
| [getArrowCount](/player/full1#getArrowCount)                             | [getNbt](/player/full1#getNbt)                                           |
| [getBodyYaw](/player/full1#getBodyYaw)                                   | [getNearestEntity](/player/full1#getNearestEntity)                       |
| [getBoundingBox](/player/full1#getBoundingBox)                           | [getPassengers](/player/full1#getPassengers)                             |
| [getChargedAttackDelay](/player/full1#getChargedAttackDelay)             | [getPermissionLevel](/player/full1#getPermissionLevel)                   |
| [getControlledVehicle](/player/full1#getControlledVehicle)               | [getPos](/player/full1#getPos)                                           |
| [getControllingPassenger](/player/full1#getControllingPassenger)         | [getPose](/player/full1#getPose)                                         |
| [getCooldownPercent](/player/full1#getCooldownPercent)                   | [getRot](/player/full1#getRot)                                           |
| [getDeathTime](/player/full1#getDeathTime)                               | [getSaturation](/player/full1#getSaturation)                             |
| [getDimensionName](/player/full1#getDimensionName)                       | [getShoulderEntity](/player/full1#getShoulderEntity)                     |
| [getEntityCategory](/player/full1#getEntityCategory)                     | [getStingerCount](/player/full1#getStingerCount)                         |
| [getExhaustion](/player/full1#getExhaustion)                             | [getSwingArm](/player/full1#getSwingArm)                                 |
| [getExperienceLevel](/player/full1#getExperienceLevel)                   | [getSwingDuration](/player/full1#getSwingDuration)                       |
| [getExperienceProgress](/player/full1#getExperienceProgress)             | [getSwingTime](/player/full1#getSwingTime)                               |
| [getEyeHeight](/player/full1#getEyeHeight)                               | [getTargetedBlock](/player/full1#getTargetedBlock)                       |
| [getEyeY](/player/full1#getEyeY)                                         | [getTargetedEntity](/player/full1#getTargetedEntity)                     |
| [getFood](/player/full1#getFood)                                         | [getTeamInfo](/player/full1#getTeamInfo)                                 |
| [getFrozenTicks](/player/full1#getFrozenTicks)                           | [getType](/player/full1#getType)                                         |
| [getGamemode](/player/full1#getGamemode)                                 | [getUUID](/player/full1#getUUID)                                         |
| [getHealth](/player/full1#getHealth)                                     | [getVariable](/player/full1#getVariable)                                 |
| [getHeldItem](/player/full1#getHeldItem)                                 | [getVehicle](/player/full1#getVehicle)                                   |
| [getItem](/player/full1#getItem)                                         | [getVelocity](/player/full1#getVelocity)                                 |


| Others<span class="hidden">----------------</span>                            | <span class="hidden">      </span>                                            |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [hasAvatar](/player/full2#hasAvatar)                                     | [hasInventory](/player/full2#hasInventory)                               |
| [hasCape](/player/full2#hasCape)                                         | [hasSkin](/player/full2#hasSkin)                                         |
| [hasContainer](/player/full2#hasContainer)                               |                                                                               |
|                                                                               |                                                                               |
| [isAlive](/player/full2#isAlive)                                         | [isMoving](/player/full2#isMoving)                                       |
| [isBlocking](/player/full2#isBlocking)                                   | [isOnFire](/player/full2#isOnFire)                                       |
| [isClimbing](/player/full2#isClimbing)                                   | [isOnGround](/player/full2#isOnGround)                                   |
| [isCrouching](/player/full2#isCrouching)                                 | [isPlayer](/player/full2#isPlayer)                                       |
| [isFalling](/player/full2#isFalling)                                     | [isSensitiveToWater](/player/full2#isSensitiveToWater)                   |
| [isFishing](/player/full2#isFishing)                                     | [isSilent](/player/full2#isSilent)                                       |
| [isGliding](/player/full2#isGliding)                                     | [isSkinLayerVisible](/player/full2#isSkinLayerVisible)                   |
| [isGlowing](/player/full2#isGlowing)                                     | [isSneaking](/player/full2#isSneaking)                                   |
| [isInLava](/player/full2#isInLava)                                       | [isSprinting](/player/full2#isSprinting)                                 |
| [isInRain](/player/full2#isInRain)                                       | [isSwingingArm](/player/full2#isSwingingArm)                             |
| [isInvisible](/player/full2#isInvisible)                                 | [isUnderwater](/player/full2#isUnderwater)                               |
| [isInWater](/player/full2#isInWater)                                     | [isUsingItem](/player/full2#isUsingItem)                                 |
| [isLeftHanded](/player/full2#isLeftHanded)                               | [isVisuallySwimming](/player/full2#isVisuallySwimming)                   |
| [isLiving](/player/full2#isLiving)                                       | [isWet](/player/full2#isWet)                                             |
| [isLoaded](/player/full2#isLoaded)                                       |                                                                               |













