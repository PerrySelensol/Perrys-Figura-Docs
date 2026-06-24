---
parent: ModelPart Objects
nav_order: 1
layout: page
title: Introduction

search_exclude: true
has_toc: false
---

<center style="font-size: 3em;">ModelPart Objects</center>

***

`ModelPart` objects are groups, cubes and meshes of a `.bbmodel` file. They are indexed according to the hierachy it appears in Blockbench.

Thus, if a model file is called `player.bbmodel` which has hierachy as shown below and you want to index `Head` group, then the index is `models.player.Root.Head`

<figure>
    <img src='{{"docs_assets/player_outliner.png" | relative_url}}' height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>
