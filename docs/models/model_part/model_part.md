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
    <img src='{{ "/docs_assets/player_outliner.png" | relative_url }}' height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>

&nbsp;

***

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

{: .note }
Examples in each of these methods and fields will use the `player.bbmodel` example file above as a reference.

| Part Transformations                                                                            |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getPos]({{ "/models/model_part/full1#getPos" | relative_url }})                                | [setPos]({{ "/models/model_part/full1#getPos" | relative_url }})                                |
| [getRot]({{ "/models/model_part/full1#getRot" | relative_url }})                                | [setRot]({{ "/models/model_part/full1#getRot" | relative_url }})                                |
| [getScale]({{ "/models/model_part/full1#getScale" | relative_url }})                            | [setScale]({{ "/models/model_part/full1#getScale" | relative_url }})                            |
| [getPivot]({{ "/models/model_part/full1#getPivot" | relative_url }})                            | [setPivot]({{ "/models/model_part/full1#getPivot" | relative_url }})                            |
|                                                                                                 |                                                                                                 |
| [getOffsetRot]({{ "/models/model_part/full1#getOffsetRot" | relative_url }})                    | [setOffsetRot]({{ "/models/model_part/full1#getOffsetRot" | relative_url }})                    |
| [getOffsetScale]({{ "/models/model_part/full1#getOffsetScale" | relative_url }})                | [setOffsetScale]({{ "/models/model_part/full1#getOffsetScale" | relative_url }})                |
| [getOffsetPivot]({{ "/models/model_part/full1#getOffsetPivot" | relative_url }})                | [setOffsetPivot]({{ "/models/model_part/full1#getOffsetPivot" | relative_url }})                |
|                                                                                                 |                                                                                                 |
| [getTruePos]({{ "/models/model_part/full1#getTruePos" | relative_url }})                        | [getAnimPos]({{ "/models/model_part/full1#getTruePos" | relative_url }})                        |
| [getTrueRot]({{ "/models/model_part/full1#getTrueRot" | relative_url }})                        | [getAnimRot]({{ "/models/model_part/full1#getTrueRot" | relative_url }})                        |
| [getTrueScale]({{ "/models/model_part/full1#getTrueScale" | relative_url }})                    | [getAnimScale]({{ "/models/model_part/full1#getTrueScale" | relative_url }})                    |
| [getTruePivot]({{ "/models/model_part/full1#getTruePivot" | relative_url }})                    |                                                                                                 |

| Appearence                                                                                      |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getVisible]({{ "/models/model_part/full2#getVisible" | relative_url }})                        | [setVisible]({{ "/models/model_part/full2#getVisible" | relative_url }})                        |
| [getUV]({{ "/models/model_part/full2#getUV" | relative_url }})                                  | [setUV]({{ "/models/model_part/full2#getUV" | relative_url }})                                  |
| [getUVPixels]({{ "/models/model_part/full2#getUVPixels" | relative_url }})                      | [setUVPixels]({{ "/models/model_part/full2#getUVPixels" | relative_url }})                      |
|                                                                                                 |                                                                                                 |
| [getColor]({{ "/models/model_part/full2#getColor" | relative_url }})                            | [setColor]({{ "/models/model_part/full2#getColor" | relative_url }})                            |
| [getPrimaryColor]({{ "/models/model_part/full2#getPrimaryColor" | relative_url }})              | [setPrimaryColor]({{ "/models/model_part/full2#getPrimaryColor" | relative_url }})              |
| [getSecondaryColor]({{ "/models/model_part/full2#getSecondaryColor" | relative_url }})          | [setSecondaryColor]({{ "/models/model_part/full2#getSecondaryColor" | relative_url }})          |
|                                                                                                 |                                                                                                 |
| [getPrimaryRenderType]({{ "/models/model_part/full2#getPrimaryRenderType" | relative_url }})    | [setPrimaryRenderType]({{ "/models/model_part/full2#getPrimaryRenderType" | relative_url }})    |
| [getSecondaryRenderType]({{ "/models/model_part/full2#getSecondaryRenderType" | relative_url }})| [setSecondaryRenderType]({{ "/models/model_part/full2#getSecondaryRenderType" | relative_url }})|
|                                                                                                 |                                                                                                 |
| [getTextures]({{ "/models/model_part/full#getTextures" | relative_url }})                       | [setPrimaryTexture]({{ "/models/model_part/full#getTextures" | relative_url }})                 |
| [getTextureSize]({{ "/models/model_part/full#getTextureSize" | relative_url }})                 | [setSecondaryTexture]({{ "/models/model_part/full#getTextureSize" | relative_url }})            |
|                                                                                                 |                                                                                                 |
| [getOpacity]({{ "/models/model_part/full2#getOpacity" | relative_url }})                        | [setOpacity]({{ "/models/model_part/full2#getOpacity" | relative_url }})                        |
| [getOverlay]({{ "/models/model_part/full#getOverlay" | relative_url }})                         | [setOverlay]({{ "/models/model_part/full#getOverlay" | relative_url }})                         |
|                                                                                                 |                                                                                                 |
| [getLight]({{ "/models/model_part/full#getLight" | relative_url }})                             | [setLight]({{ "/models/model_part/full#getLight" | relative_url }})                             |
| [getUVMatrix]({{ "/models/model_part/full2#getUVMatrix" | relative_url }})                      | [setUVMatrix]({{ "/models/model_part/full2#getUVMatrix" | relative_url }})                      |

| Part Properties                                                                                 |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [getParentType]({{ "/models/model_part/full1#getParentType" | relative_url }})                  | [setParentType]({{ "/models/model_part/full1#getParentType" | relative_url }})                  |
|                                                                                                 |                                                                                                 |
| [getName]({{ "/models/model_part/full#getName" | relative_url }})                               | [setMidRender]({{ "/models/model_part/full#getName" | relative_url }})                          |
| [getType]({{ "/models/model_part/full#getType" | relative_url }})                               | [setPostRender]({{ "/models/model_part/full#getType" | relative_url }})                         |
| [getParent]({{ "/models/model_part/full#getParent" | relative_url }})                           | [setPreRender]({{ "/models/model_part/full#getParent" | relative_url }})                        |
| [getChildren]({{ "/models/model_part/full#getChildren" | relative_url }})                       |                                                                                                 |
|                                                                                                 |                                                                                                 |
| [overrideVanillaPos]({{ "/models/model_part/full#overrideVanillaPos" | relative_url }})         | [getAllVertices]({{ "/models/model_part/full#overrideVanillaPos" | relative_url }})             |
| [overrideVanillaRot]({{ "/models/model_part/full#overrideVanillaRot" | relative_url }})         | [getVertices]({{ "/models/model_part/full#overrideVanillaRot" | relative_url }})                |
| [overrideVanillaScale]({{ "/models/model_part/full#overrideVanillaScale" | relative_url }})     |                                                                                                 |

| Part Transformations via Matrices                                                               |                                                                                                 |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [partToWorldMatrix]({{ "/models/model_part/full#partToWorldMatrix" | relative_url }})           | [setMatrix]({{ "/models/model_part/full#partToWorldMatrix" | relative_url }})                   |
| [getPositionMatrix]({{ "/models/model_part/full#getPositionMatrix" | relative_url }})           |                                                                                                 |
| [getPositionMatrixRaw]({{ "/models/model_part/full#getPositionMatrixRaw" | relative_url }})     |                                                                                                 |
| [getNormalMatrix]({{ "/models/model_part/full#getNormalMatrix" | relative_url }})               |                                                                                                 |
| [getNormalMatrixRaw]({{ "/models/model_part/full#getNormalMatrixRaw" | relative_url }})         |                                                                                                 |

| Miscellaneous                                                                                   | Fields                                                                                          |
| ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| [newText]({{ "/models/model_part/full#newText" | relative_url }})                               | [preRender]({{ "/models/model_part/full#newText" | relative_url }})                             |
| [newBlock]({{ "/models/model_part/full#newBlock" | relative_url }})                             | [postRender]({{ "/models/model_part/full#newBlock" | relative_url }})                           |
| [newItem]({{ "/models/model_part/full#newItem" | relative_url }})                               | [midRender]({{ "/models/model_part/full#newItem" | relative_url }})                             |
| [newSprite]({{ "/models/model_part/full#newSprite" | relative_url }})                           |                                                                                                 |
| [newTask]({{ "/models/model_part/full#newTask" | relative_url }})                               |                                                                                                 |
| [newPart]({{ "/models/model_part/full#newPart" | relative_url }})                               |                                                                                                 |
| [removeTask]({{ "/models/model_part/full#removeTask" | relative_url }})                         |                                                                                                 |
| [getTask]({{ "/models/model_part/full#getTask" | relative_url }})                               |                                                                                                 |
|                                                                                                 |                                                                                                 |
| [addChild]({{ "/models/model_part/full#addChild" | relative_url }})                             |                                                                                                 |
| [moveTo]({{ "/models/model_part/full#moveTo" | relative_url }})                                 |                                                                                                 |
| [copy]({{ "/models/model_part/full#copy" | relative_url }})                                     |                                                                                                 |
| [removeChild]({{ "/models/model_part/full#removeChild" | relative_url }})                       |                                                                                                 |
| [isChildOf]({{ "/models/model_part/full#isChildOf" | relative_url }})                           |                                                                                                 |
