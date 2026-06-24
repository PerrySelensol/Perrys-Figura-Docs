---
layout: page
parent: Figura Documentation
title: Player and Entities
permalink: /figura-docs/player
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
| [getAbsorptionAmount](/figura-docs/player/full1#getAbsorptionAmount)                 | [getLookDir](/figura-docs/player/full1#getLookDir)                                   |
| [getActiveHand](/figura-docs/player/full1#getActiveHand)                             | [getMaxAir](/figura-docs/player/full1#getMaxAir)                                     |
| [getActiveItem](/figura-docs/player/full1#getActiveItem)                             | [getMaxHealth](/figura-docs/player/full1#getMaxHealth)                               |
| [getActiveItemTime](/figura-docs/player/full1#getActiveItemTime)                     | [getModelType](/figura-docs/player/full1#getModelType)                               |
| [getArmor](/figura-docs/player/full1#getArmor)                                       | [getName](/figura-docs/player/full1#getName)                                         |
| [getArrowCount](/figura-docs/player/full1#getArrowCount)                             | [getNbt](/figura-docs/player/full1#getNbt)                                           |
| [getBodyYaw](/figura-docs/player/full1#getBodyYaw)                                   | [getNearestEntity](/figura-docs/player/full1#getNearestEntity)                       |
| [getBoundingBox](/figura-docs/player/full1#getBoundingBox)                           | [getPassengers](/figura-docs/player/full1#getPassengers)                             |
| [getChargedAttackDelay](/figura-docs/player/full1#getChargedAttackDelay)             | [getPermissionLevel](/figura-docs/player/full1#getPermissionLevel)                   |
| [getControlledVehicle](/figura-docs/player/full1#getControlledVehicle)               | [getPos](/figura-docs/player/full1#getPos)                                           |
| [getControllingPassenger](/figura-docs/player/full1#getControllingPassenger)         | [getPose](/figura-docs/player/full1#getPose)                                         |
| [getCooldownPercent](/figura-docs/player/full1#getCooldownPercent)                   | [getRot](/figura-docs/player/full1#getRot)                                           |
| [getDeathTime](/figura-docs/player/full1#getDeathTime)                               | [getSaturation](/figura-docs/player/full1#getSaturation)                             |
| [getDimensionName](/figura-docs/player/full1#getDimensionName)                       | [getShoulderEntity](/figura-docs/player/full1#getShoulderEntity)                     |
| [getEntityCategory](/figura-docs/player/full1#getEntityCategory)                     | [getStingerCount](/figura-docs/player/full1#getStingerCount)                         |
| [getExhaustion](/figura-docs/player/full1#getExhaustion)                             | [getSwingArm](/figura-docs/player/full1#getSwingArm)                                 |
| [getExperienceLevel](/figura-docs/player/full1#getExperienceLevel)                   | [getSwingDuration](/figura-docs/player/full1#getSwingDuration)                       |
| [getExperienceProgress](/figura-docs/player/full1#getExperienceProgress)             | [getSwingTime](/figura-docs/player/full1#getSwingTime)                               |
| [getEyeHeight](/figura-docs/player/full1#getEyeHeight)                               | [getTargetedBlock](/figura-docs/player/full1#getTargetedBlock)                       |
| [getEyeY](/figura-docs/player/full1#getEyeY)                                         | [getTargetedEntity](/figura-docs/player/full1#getTargetedEntity)                     |
| [getFood](/figura-docs/player/full1#getFood)                                         | [getTeamInfo](/figura-docs/player/full1#getTeamInfo)                                 |
| [getFrozenTicks](/figura-docs/player/full1#getFrozenTicks)                           | [getType](/figura-docs/player/full1#getType)                                         |
| [getGamemode](/figura-docs/player/full1#getGamemode)                                 | [getUUID](/figura-docs/player/full1#getUUID)                                         |
| [getHealth](/figura-docs/player/full1#getHealth)                                     | [getVariable](/figura-docs/player/full1#getVariable)                                 |
| [getHeldItem](/figura-docs/player/full1#getHeldItem)                                 | [getVehicle](/figura-docs/player/full1#getVehicle)                                   |
| [getItem](/figura-docs/player/full1#getItem)                                         | [getVelocity](/figura-docs/player/full1#getVelocity)                                 |


| Others<span class="hidden">----------------</span>                            | <span class="hidden">      </span>                                            |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [hasAvatar](/figura-docs/player/full2#hasAvatar)                                     | [hasInventory](/figura-docs/player/full2#hasInventory)                               |
| [hasCape](/figura-docs/player/full2#hasCape)                                         | [hasSkin](/figura-docs/player/full2#hasSkin)                                         |
| [hasContainer](/figura-docs/player/full2#hasContainer)                               |                                                                               |
|                                                                               |                                                                               |
| [isAlive](/figura-docs/player/full2#isAlive)                                         | [isMoving](/figura-docs/player/full2#isMoving)                                       |
| [isBlocking](/figura-docs/player/full2#isBlocking)                                   | [isOnFire](/figura-docs/player/full2#isOnFire)                                       |
| [isClimbing](/figura-docs/player/full2#isClimbing)                                   | [isOnGround](/figura-docs/player/full2#isOnGround)                                   |
| [isCrouching](/figura-docs/player/full2#isCrouching)                                 | [isPlayer](/figura-docs/player/full2#isPlayer)                                       |
| [isFalling](/figura-docs/player/full2#isFalling)                                     | [isSensitiveToWater](/figura-docs/player/full2#isSensitiveToWater)                   |
| [isFishing](/figura-docs/player/full2#isFishing)                                     | [isSilent](/figura-docs/player/full2#isSilent)                                       |
| [isGliding](/figura-docs/player/full2#isGliding)                                     | [isSkinLayerVisible](/figura-docs/player/full2#isSkinLayerVisible)                   |
| [isGlowing](/figura-docs/player/full2#isGlowing)                                     | [isSneaking](/figura-docs/player/full2#isSneaking)                                   |
| [isInLava](/figura-docs/player/full2#isInLava)                                       | [isSprinting](/figura-docs/player/full2#isSprinting)                                 |
| [isInRain](/figura-docs/player/full2#isInRain)                                       | [isSwingingArm](/figura-docs/player/full2#isSwingingArm)                             |
| [isInvisible](/figura-docs/player/full2#isInvisible)                                 | [isUnderwater](/figura-docs/player/full2#isUnderwater)                               |
| [isInWater](/figura-docs/player/full2#isInWater)                                     | [isUsingItem](/figura-docs/player/full2#isUsingItem)                                 |
| [isLeftHanded](/figura-docs/player/full2#isLeftHanded)                               | [isVisuallySwimming](/figura-docs/player/full2#isVisuallySwimming)                   |
| [isLiving](/figura-docs/player/full2#isLiving)                                       | [isWet](/figura-docs/player/full2#isWet)                                             |
| [isLoaded](/figura-docs/player/full2#isLoaded)                                       |                                                                               |













