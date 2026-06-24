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
    <img src='player_outliner.png' height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>

&nbsp;

***

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

{: .note }
Examples in each of these methods and fields will use the `player.bbmodel` example file above as a reference.

| Part Transformations                                                                            |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getPos](model_part/full1#getPos)                                | [setPos](model_part/full1#getPos)                                |
| [getRot](model_part/full1#getRot)                                | [setRot](model_part/full1#getRot)                                |
| [getScale](model_part/full1#getScale)                            | [setScale](model_part/full1#getScale)                            |
| [getPivot](model_part/full1#getPivot)                            | [setPivot](model_part/full1#getPivot)                            |
|                                                                                                 |                                                                                                 |
| [getOffsetRot](model_part/full1#getOffsetRot)                    | [setOffsetRot](model_part/full1#getOffsetRot)                    |
| [getOffsetScale](model_part/full1#getOffsetScale)                | [setOffsetScale](model_part/full1#getOffsetScale)                |
| [getOffsetPivot](model_part/full1#getOffsetPivot)                | [setOffsetPivot](model_part/full1#getOffsetPivot)                |
|                                                                                                 |                                                                                                 |
| [getTruePos](model_part/full1#getTruePos)                        | [getAnimPos](model_part/full1#getTruePos)                        |
| [getTrueRot](model_part/full1#getTrueRot)                        | [getAnimRot](model_part/full1#getTrueRot)                        |
| [getTrueScale](model_part/full1#getTrueScale)                    | [getAnimScale](model_part/full1#getTrueScale)                    |
| [getTruePivot](model_part/full1#getTruePivot)                    |                                                                                                 |

| Appearence                                                                                      |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getVisible](model_part/full2#getVisible)                        | [setVisible](model_part/full2#getVisible)                        |
| [getUV](model_part/full2#getUV)                                  | [setUV](model_part/full2#getUV)                                  |
| [getUVPixels](model_part/full2#getUVPixels)                      | [setUVPixels](model_part/full2#getUVPixels)                      |
|                                                                                                 |                                                                                                 |
| [getColor](model_part/full2#getColor)                            | [setColor](model_part/full2#getColor)                            |
| [getPrimaryColor](model_part/full2#getPrimaryColor)              | [setPrimaryColor](model_part/full2#getPrimaryColor)              |
| [getSecondaryColor](model_part/full2#getSecondaryColor)          | [setSecondaryColor](model_part/full2#getSecondaryColor)          |
|                                                                                                 |                                                                                                 |
| [getPrimaryRenderType](model_part/full2#getPrimaryRenderType)    | [setPrimaryRenderType](model_part/full2#getPrimaryRenderType)    |
| [getSecondaryRenderType](model_part/full2#getSecondaryRenderType)| [setSecondaryRenderType](model_part/full2#getSecondaryRenderType)|
|                                                                                                 |                                                                                                 |
| [getTextures](model_part/full#getTextures)                       | [setPrimaryTexture](model_part/full#getTextures)                 |
| [getTextureSize](model_part/full#getTextureSize)                 | [setSecondaryTexture](model_part/full#getTextureSize)            |
|                                                                                                 |                                                                                                 |
| [getOpacity](model_part/full2#getOpacity)                        | [setOpacity](model_part/full2#getOpacity)                        |
| [getOverlay](model_part/full#getOverlay)                         | [setOverlay](model_part/full#getOverlay)                         |
|                                                                                                 |                                                                                                 |
| [getLight](model_part/full#getLight)                             | [setLight](model_part/full#getLight)                             |
| [getUVMatrix](model_part/full2#getUVMatrix)                      | [setUVMatrix](model_part/full2#getUVMatrix)                      |

| Part Properties                                                                                 |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getParentType](model_part/full1#getParentType)                  | [setParentType](model_part/full1#getParentType)                  |
|                                                                                                 |                                                                                                 |
| [getName](model_part/full#getName)                               | [setMidRender](model_part/full#getName)                          |
| [getType](model_part/full#getType)                               | [setPostRender](model_part/full#getType)                         |
| [getParent](model_part/full#getParent)                           | [setPreRender](model_part/full#getParent)                        |
| [getChildren](model_part/full#getChildren)                       |                                                                                                 |
|                                                                                                 |                                                                                                 |
| [overrideVanillaPos](model_part/full#overrideVanillaPos)         | [getAllVertices](model_part/full#overrideVanillaPos)             |
| [overrideVanillaRot](model_part/full#overrideVanillaRot)         | [getVertices](model_part/full#overrideVanillaRot)                |
| [overrideVanillaScale](model_part/full#overrideVanillaScale)     |                                                                                                 |

| Part Transformations via Matrices                                                               |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [partToWorldMatrix](model_part/full#partToWorldMatrix)           | [setMatrix](model_part/full#partToWorldMatrix)                   |
| [getPositionMatrix](model_part/full#getPositionMatrix)           |                                                                                                 |
| [getPositionMatrixRaw](model_part/full#getPositionMatrixRaw)     |                                                                                                 |
| [getNormalMatrix](model_part/full#getNormalMatrix)               |                                                                                                 |
| [getNormalMatrixRaw](model_part/full#getNormalMatrixRaw)         |                                                                                                 |

| Miscellaneous                                                                                   | Fields                                                                                          |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [newText](model_part/full#newText)                               | [preRender](model_part/full#newText)                             |
| [newBlock](model_part/full#newBlock)                             | [postRender](model_part/full#newBlock)                           |
| [newItem](model_part/full#newItem)                               | [midRender](model_part/full#newItem)                             |
| [newSprite](model_part/full#newSprite)                           |                                                                                                 |
| [newTask](model_part/full#newTask)                               |                                                                                                 |
| [newPart](model_part/full#newPart)                               |                                                                                                 |
| [removeTask](model_part/full#removeTask)                         |                                                                                                 |
| [getTask](model_part/full#getTask)                               |                                                                                                 |
|                                                                                                 |                                                                                                 |
| [addChild](model_part/full#addChild)                             |                                                                                                 |
| [moveTo](model_part/full#moveTo)                                 |                                                                                                 |
| [copy](model_part/full#copy)                                     |                                                                                                 |
| [removeChild](model_part/full#removeChild)                       |                                                                                                 |
| [isChildOf](model_part/full#isChildOf)                           |                                                                                                 |
