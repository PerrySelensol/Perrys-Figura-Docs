---
layout: page
parent: Models
title: ModelPart Objects
permalink: /models/model_part
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
    <img src='{{ "/images/player_outliner.png" | relative_url }}' height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>

&nbsp;

***

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

{: .note }
Examples in each of these methods and fields will use the `player.bbmodel` example file above as a reference.

| Part Transformations                                                          |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getPos](/models/model_part/full1#getPos)                                | [setPos](/models/model_part/full1#setPos)                                |
| [getRot](/models/model_part/full1#getRot)                                | [setRot](/models/model_part/full1#setRot)                                |
| [getScale](/models/model_part/full1#getScale)                            | [setScale](/models/model_part/full1#setScale)                            |
| [getPivot](/models/model_part/full1#getPivot)                            | [setPivot](/models/model_part/full1#setPivot)                            |
|                                                                               |                                                                               |
| [getOffsetRot](/models/model_part/full1#getOffsetRot)                    | [setOffsetRot](/models/model_part/full1#setOffsetRot)                    |
| [getOffsetScale](/models/model_part/full1#getOffsetScale)                | [setOffsetScale](/models/model_part/full1#setOffsetScale)                |
| [getOffsetPivot](/models/model_part/full1#getOffsetPivot)                | [setOffsetPivot](/models/model_part/full1#setOffsetPivot)                |
|                                                                               |                                                                               |
| [getTruePos](/models/model_part/full1#getTruePos)                        | [getAnimPos](/models/model_part/full1#getAnimPos)                        |
| [getTrueRot](/models/model_part/full1#getTrueRot)                        | [getAnimRot](/models/model_part/full1#getAnimRot)                        |
| [getTrueScale](/models/model_part/full1#getTrueScale)                    | [getAnimScale](/models/model_part/full1#getAnimScale)                    |
| [getTruePivot](/models/model_part/full1#getTruePivot)                    |                                                                               |

| Appearence                                                                    |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getVisible](/models/model_part/full2#getVisible)                        | [setVisible](/models/model_part/full2#setVisible)                        |
| [getUV](/models/model_part/full2#getUV)                                  | [setUV](/models/model_part/full2#setUV)                                  |
| [getUVPixels](/models/model_part/full2#getUVPixels)                      | [setUVPixels](/models/model_part/full2#setUVPixels)                      |
|                                                                               |                                                                               |
| [getColor](/models/model_part/full2#getColor)                            | [setColor](/models/model_part/full2#setColor)                            |
| [getPrimaryColor](/models/model_part/full2#getPrimaryColor)              | [setPrimaryColor](/models/model_part/full2#setPrimaryColor)              |
| [getSecondaryColor](/models/model_part/full2#getSecondaryColor)          | [setSecondaryColor](/models/model_part/full2#setSecondaryColor)          |
|                                                                               |                                                                               |
| [getPrimaryRenderType](/models/model_part/full2#getPrimaryRenderType)    | [setPrimaryRenderType](/models/model_part/full2#setPrimaryRenderType)    |
| [getSecondaryRenderType](/models/model_part/full2#getSecondaryRenderType)| [setSecondaryRenderType](/models/model_part/full2#setSecondaryRenderType)|
|                                                                               |                                                                               |
| [getTextures](/models/model_part/full#getTextures)                       | [setPrimaryTexture](/models/model_part/full#setPrimaryTexture)           |
| [getTextureSize](/models/model_part/full#getTextureSize)                 | [setSecondaryTexture](/models/model_part/full#setSecondaryTexture)       |
|                                                                               |                                                                               |
| [getOpacity](/models/model_part/full2#getOpacity)                        | [setOpacity](/models/model_part/full2#setOpacity)                        |
| [getOverlay](/models/model_part/full#getOverlay)                         | [setOverlay](/models/model_part/full#setOverlay)                         |
|                                                                               |                                                                               |
| [getLight](/models/model_part/full#getLight)                             | [setLight](/models/model_part/full#setLight)                             |
| [getUVMatrix](/models/model_part/full2#getUVMatrix)                      | [setUVMatrix](/models/model_part/full2#setUVMatrix)                      |

| Part Properties                                                               |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getParentType](/models/model_part/full1#getParentType)                  | [setParentType](/models/model_part/full1#setParentType)                  |
|                                                                               |                                                                               |
| [getName](/models/model_part/full#getName)                               | [setMidRender](/models/model_part/full#setMidRender)                     |
| [getType](/models/model_part/full#getType)                               | [setPostRender](/models/model_part/full#setPostRender)                   |
| [getParent](/models/model_part/full#getParent)                           | [setPreRender](/models/model_part/full#setPreRender)                     |
| [getChildren](/models/model_part/full#getChildren)                       |                                                                               |
|                                                                               |                                                                               |
| [overrideVanillaPos](/models/model_part/full#overrideVanillaPos)         | [getAllVertices](/models/model_part/full#getAllVertices)                 |
| [overrideVanillaRot](/models/model_part/full#overrideVanillaRot)         | [getVertices](/models/model_part/full#getVertices)                       |
| [overrideVanillaScale](/models/model_part/full#overrideVanillaScale)     |                                                                               |

| Part Transformations via Matrices                                             |                                                                               |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [partToWorldMatrix](/models/model_part/full#partToWorldMatrix)           | [setMatrix](/models/model_part/full#setMatrix)                           |
| [getPositionMatrix](/models/model_part/full#getPositionMatrix)           |                                                                               |
| [getPositionMatrixRaw](/models/model_part/full#getPositionMatrixRaw)     |                                                                               |
| [getNormalMatrix](/models/model_part/full#getNormalMatrix)               |                                                                               |
| [getNormalMatrixRaw](/models/model_part/full#getNormalMatrixRaw)         |                                                                               |

| Miscellaneous                                                                 | Fields                                                                        |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [newText](/models/model_part/full#newText)                               | [preRender](/models/model_part/full#preRender)                           |
| [newBlock](/models/model_part/full#newBlock)                             | [postRender](/models/model_part/full#postRender)                         |
| [newItem](/models/model_part/full#newItem)                               | [midRender](/models/model_part/full#midRender)                           |
| [newSprite](/models/model_part/full#newSprite)                           |                                                                               |
| [newTask](/models/model_part/full#newTask)                               |                                                                               |
| [newPart](/models/model_part/full#newPart)                               |                                                                               |
| [removeTask](/models/model_part/full#removeTask)                         |                                                                               |
| [getTask](/models/model_part/full#getTask)                               |                                                                               |
|                                                                               |                                                                               |
| [addChild](/models/model_part/full#addChild)                             |                                                                               |
| [moveTo](/models/model_part/full#moveTo)                                 |                                                                               |
| [copy](/models/model_part/full#copy)                                     |                                                                               |
| [removeChild](/models/model_part/full#removeChild)                       |                                                                               |
| [isChildOf](/models/model_part/full#isChildOf)                           |                                                                               |
