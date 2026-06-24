---
parent: Models
nav_order: 2
layout: page
title: ModelPart Objects

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

***

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

{: .note }
> Examples in each of these methods and fields will use the `player.bbmodel` from the introduction as a reference.

| Part Transformations                                  |                                                       |
| ----------------------------------------------------- | ----------------------------------------------------- |
| [getPos](full1#getPos)                                | [setPos](full1#setPos)                                |
| [getRot](full1#getRot)                                | [setRot](full1#setRot)                                |
| [getScale](full1#getScale)                            | [setScale](full1#setScale)                            |
| [getPivot](full1#getPivot)                            | [setPivot](full1#setPivot)                            |
|                                                       |                                                       |
| [getOffsetRot](full1#getOffsetRot)                    | [setOffsetRot](full1#setOffsetRot)                    |
| [getOffsetScale](full1#getOffsetScale)                | [setOffsetScale](full1#setOffsetScale)                |
| [getOffsetPivot](full1#getOffsetPivot)                | [setOffsetPivot](full1#setOffsetPivot)                |
|                                                       |                                                       |
| [getTruePos](full1#getTruePos)                        | [getAnimPos](full1#getAnimPos)                        |
| [getTrueRot](full1#getTrueRot)                        | [getAnimRot](full1#getAnimRot)                        |
| [getTrueScale](full1#getTrueScale)                    | [getAnimScale](full1#getAnimScale)                    |
| [getTruePivot](full1#getTruePivot)                    |                                                       |

| Appearence                                            |                                                       |
| ----------------------------------------------------- | ----------------------------------------------------- |
| [getVisible](full2#getVisible)                        | [setVisible](full2#setVisible)                        |
| [getUV](full2#getUV)                                  | [setUV](full2#setUV)                                  |
| [getUVPixels](full2#getUVPixels)                      | [setUVPixels](full2#setUVPixels)                      |
|                                                       |                                                       |
| [getColor](full2#getColor)                            | [setColor](full2#setColor)                            |
| [getPrimaryColor](full2#getPrimaryColor)              | [setPrimaryColor](full2#setPrimaryColor)              |
| [getSecondaryColor](full2#getSecondaryColor)          | [setSecondaryColor](full2#setSecondaryColor)          |
|                                                       |                                                       |
| [getPrimaryRenderType](full2#getPrimaryRenderType)    | [setPrimaryRenderType](full2#setPrimaryRenderType)    |
| [getSecondaryRenderType](full2#getSecondaryRenderType)| [setSecondaryRenderType](full2#setSecondaryRenderType)|
|                                                       |                                                       |
| [getTextures](full2#getTextures)                      | [setPrimaryTexture](full2#setPrimaryTexture)          |
| [getTextureSize](full2#getTextureSize)                | [setSecondaryTexture](full2#setSecondaryTexture)      |
|                                                       |                                                       |
| [getOpacity](full2#getOpacity)                        | [setOpacity](full2#setOpacity)                        |
| [getOverlay](full2#getOverlay)                        | [setOverlay](full2#setOverlay)                        |
|                                                       |                                                       |
| [getLight](full2#getLight)                            | [setLight](full2#setLight)                            |
| [getUVMatrix](full2#getUVMatrix)                      | [setUVMatrix](full2#setUVMatrix)                      |

| Part Properties                                       |                                                       |
| ----------------------------------------------------- | ----------------------------------------------------- |
| [getParentType](full3#getParentType)                  | [setParentType](full3#getParentType)                  |
|                                                       |                                                       |
| [getName](full3#getName)                              | [setMidRender](full3#getName)                         |
| [getType](full3#getType)                              | [setPostRender](full3#getType)                        |
| [getParent](full3#getParent)                          | [setPreRender](full3#getParent)                       |
| [getChildren](full3#getChildren)                      |                                                       |
|                                                       |                                                       |
| [overrideVanillaPos](full3#overrideVanillaPos)        | [getAllVertices](full3#overrideVanillaPos)            |
| [overrideVanillaRot](full3#overrideVanillaRot)        | [getVertices](full3#overrideVanillaRot)               |
| [overrideVanillaScale](full3#overrideVanillaScale)    |                                                       |

| Part Transformations via Matrices                     |                                                       |
| ----------------------------------------------------- | ----------------------------------------------------- |
| [partToWorldMatrix](full4#partToWorldMatrix)          | [setMatrix](full4#partToWorldMatrix)                  |
| [getPositionMatrix](full4#getPositionMatrix)          |                                                       |
| [getPositionMatrixRaw](full4#getPositionMatrixRaw)    |                                                       |
| [getNormalMatrix](full4#getNormalMatrix)              |                                                       |
| [getNormalMatrixRaw](full4#getNormalMatrixRaw)        |                                                       |

| Miscellaneous                                         | Fields                                                |
| ----------------------------------------------------- | ----------------------------------------------------- |
| [newText](full5#newText)                              | [preRender](full5#newText)                            |
| [newBlock](full5#newBlock)                            | [postRender](full5#newBlock)                          |
| [newItem](full5#newItem)                              | [midRender](full5#newItem)                            |
| [newSprite](full5#newSprite)                          |                                                       |
| [newTask](full5#newTask)                              |                                                       |
| [newPart](full5#newPart)                              |                                                       |
| [removeTask](full5#removeTask)                        |                                                       |
| [getTask](full5#getTask)                              |                                                       |
|                                                       |                                                       |
| [addChild](full5#addChild)                            |                                                       |
| [moveTo](full5#moveTo)                                |                                                       |
| [copy](full5#copy)                                    |                                                       |
| [removeChild](full5#removeChild)                      |                                                       |
| [isChildOf](full5#isChildOf)                          |                                                       |
