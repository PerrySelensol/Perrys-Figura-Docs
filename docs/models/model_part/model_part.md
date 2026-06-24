---
layout: page
parent: Models
title: ModelPart Objects
permalink: /figura-docs/models/model_part
search_exclude: true
has_toc: false
---

<style> span.hidden {visibility: hidden;} </style>

<style> span.hidden {visibility: hidden;} </style>

<style>
    table th:first-of-type {
        width: 50%;
    }
    table th:nth-of-type(2) {
        width: 50%;
    }
</style>

<center style="font-size: 3em;">ModelPart Objects</center>

***

`ModelPart` objects are groups, cubes and meshes of a `.bbmodel` file. They are indexed according to the hierachy it appears in Blockbench.

Thus, if a model file is called `player.bbmodel` which has hierachy as shown below and you want to index `Head` group, then the index is `models.player.Root.Head`

<figure>
    <img src="/docs/images/player_outliner.png" height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>

&nbsp;

***

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

{: .note }
Examples in each of these methods and fields will use the `player.bbmodel` example file above as a reference.

| Part Transformations                                                          |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getPos](/figura-docs/models/model_part/full1#getPos)                                | [setPos](/figura-docs/models/model_part/full1#setPos)                                |
| [getRot](/figura-docs/models/model_part/full1#getRot)                                | [setRot](/figura-docs/models/model_part/full1#setRot)                                |
| [getScale](/figura-docs/models/model_part/full1#getScale)                            | [setScale](/figura-docs/models/model_part/full1#setScale)                            |
| [getPivot](/figura-docs/models/model_part/full1#getPivot)                            | [setPivot](/figura-docs/models/model_part/full1#setPivot)                            |
|                                                                               |                                                                               |
| [getOffsetRot](/figura-docs/models/model_part/full1#getOffsetRot)                    | [setOffsetRot](/figura-docs/models/model_part/full1#setOffsetRot)                    |
| [getOffsetScale](/figura-docs/models/model_part/full1#getOffsetScale)                | [setOffsetScale](/figura-docs/models/model_part/full1#setOffsetScale)                |
| [getOffsetPivot](/figura-docs/models/model_part/full1#getOffsetPivot)                | [setOffsetPivot](/figura-docs/models/model_part/full1#setOffsetPivot)                |
|                                                                               |                                                                               |
| [getTruePos](/figura-docs/models/model_part/full1#getTruePos)                        | [getAnimPos](/figura-docs/models/model_part/full1#getAnimPos)                        |
| [getTrueRot](/figura-docs/models/model_part/full1#getTrueRot)                        | [getAnimRot](/figura-docs/models/model_part/full1#getAnimRot)                        |
| [getTrueScale](/figura-docs/models/model_part/full1#getTrueScale)                    | [getAnimScale](/figura-docs/models/model_part/full1#getAnimScale)                    |
| [getTruePivot](/figura-docs/models/model_part/full1#getTruePivot)                    |                                                                               |

| Appearence                                                                    |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getVisible](/figura-docs/models/model_part/full2#getVisible)                        | [setVisible](/figura-docs/models/model_part/full2#setVisible)                        |
| [getUV](/figura-docs/models/model_part/full2#getUV)                                  | [setUV](/figura-docs/models/model_part/full2#setUV)                                  |
| [getUVPixels](/figura-docs/models/model_part/full2#getUVPixels)                      | [setUVPixels](/figura-docs/models/model_part/full2#setUVPixels)                      |
|                                                                               |                                                                               |
| [getColor](/figura-docs/models/model_part/full2#getColor)                            | [setColor](/figura-docs/models/model_part/full2#setColor)                            |
| [getPrimaryColor](/figura-docs/models/model_part/full2#getPrimaryColor)              | [setPrimaryColor](/figura-docs/models/model_part/full2#setPrimaryColor)              |
| [getSecondaryColor](/figura-docs/models/model_part/full2#getSecondaryColor)          | [setSecondaryColor](/figura-docs/models/model_part/full2#setSecondaryColor)          |
|                                                                               |                                                                               |
| [getPrimaryRenderType](/figura-docs/models/model_part/full2#getPrimaryRenderType)    | [setPrimaryRenderType](/figura-docs/models/model_part/full2#setPrimaryRenderType)    |
| [getSecondaryRenderType](/figura-docs/models/model_part/full2#getSecondaryRenderType)| [setSecondaryRenderType](/figura-docs/models/model_part/full2#setSecondaryRenderType)|
|                                                                               |                                                                               |
| [getTextures](/figura-docs/models/model_part/full#getTextures)                       | [setPrimaryTexture](/figura-docs/models/model_part/full#setPrimaryTexture)           |
| [getTextureSize](/figura-docs/models/model_part/full#getTextureSize)                 | [setSecondaryTexture](/figura-docs/models/model_part/full#setSecondaryTexture)       |
|                                                                               |                                                                               |
| [getOpacity](/figura-docs/models/model_part/full2#getOpacity)                        | [setOpacity](/figura-docs/models/model_part/full2#setOpacity)                        |
| [getOverlay](/figura-docs/models/model_part/full#getOverlay)                         | [setOverlay](/figura-docs/models/model_part/full#setOverlay)                         |
|                                                                               |                                                                               |
| [getLight](/figura-docs/models/model_part/full#getLight)                             | [setLight](/figura-docs/models/model_part/full#setLight)                             |
| [getUVMatrix](/figura-docs/models/model_part/full2#getUVMatrix)                      | [setUVMatrix](/figura-docs/models/model_part/full2#setUVMatrix)                      |

| Part Properties                                                               |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getParentType](/figura-docs/models/model_part/full1#getParentType)                  | [setParentType](/figura-docs/models/model_part/full1#setParentType)                  |
|                                                                               |                                                                               |
| [getName](/figura-docs/models/model_part/full#getName)                               | [setMidRender](/figura-docs/models/model_part/full#setMidRender)                     |
| [getType](/figura-docs/models/model_part/full#getType)                               | [setPostRender](/figura-docs/models/model_part/full#setPostRender)                   |
| [getParent](/figura-docs/models/model_part/full#getParent)                           | [setPreRender](/figura-docs/models/model_part/full#setPreRender)                     |
| [getChildren](/figura-docs/models/model_part/full#getChildren)                       |                                                                               |
|                                                                               |                                                                               |
| [overrideVanillaPos](/figura-docs/models/model_part/full#overrideVanillaPos)         | [getAllVertices](/figura-docs/models/model_part/full#getAllVertices)                 |
| [overrideVanillaRot](/figura-docs/models/model_part/full#overrideVanillaRot)         | [getVertices](/figura-docs/models/model_part/full#getVertices)                       |
| [overrideVanillaScale](/figura-docs/models/model_part/full#overrideVanillaScale)     |                                                                               |

| Part Transformations via Matrices                                             |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [partToWorldMatrix](/figura-docs/models/model_part/full#partToWorldMatrix)           | [setMatrix](/figura-docs/models/model_part/full#setMatrix)                           |
| [getPositionMatrix](/figura-docs/models/model_part/full#getPositionMatrix)           |                                                                               |
| [getPositionMatrixRaw](/figura-docs/models/model_part/full#getPositionMatrixRaw)     |                                                                               |
| [getNormalMatrix](/figura-docs/models/model_part/full#getNormalMatrix)               |                                                                               |
| [getNormalMatrixRaw](/figura-docs/models/model_part/full#getNormalMatrixRaw)         |                                                                               |

| Miscellaneous                                                                 | Fields                                                                        |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [newText](/figura-docs/models/model_part/full#newText)                               | [preRender](/figura-docs/models/model_part/full#preRender)                           |
| [newBlock](/figura-docs/models/model_part/full#newBlock)                             | [postRender](/figura-docs/models/model_part/full#postRender)                         |
| [newItem](/figura-docs/models/model_part/full#newItem)                               | [midRender](/figura-docs/models/model_part/full#midRender)                           |
| [newSprite](/figura-docs/models/model_part/full#newSprite)                           |                                                                               |
| [newTask](/figura-docs/models/model_part/full#newTask)                               |                                                                               |
| [newPart](/figura-docs/models/model_part/full#newPart)                               |                                                                               |
| [removeTask](/figura-docs/models/model_part/full#removeTask)                         |                                                                               |
| [getTask](/figura-docs/models/model_part/full#getTask)                               |                                                                               |
|                                                                               |                                                                               |
| [addChild](/figura-docs/models/model_part/full#addChild)                             |                                                                               |
| [moveTo](/figura-docs/models/model_part/full#moveTo)                                 |                                                                               |
| [copy](/figura-docs/models/model_part/full#copy)                                     |                                                                               |
| [removeChild](/figura-docs/models/model_part/full#removeChild)                       |                                                                               |
| [isChildOf](/figura-docs/models/model_part/full#isChildOf)                           |                                                                               |
