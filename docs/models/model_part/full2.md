---
layout: page
parent: ModelPart Objects
title: All Part Appearence
permalink: /figura-docs/models/model_part/full2
---

<center style="font-size: 3em;">ModelPart Functions</center>

<center style="font-size: 2em;">Appearence</center>

***

<h1 id="setVisible" style="font-size: 2.5em;color:#00008B">setVisible</h1>

```lua
HeadPart = models.player.Root.Head:setVisible(is_visible)
```

Set visibility of the part. Corresponds to clicking show/hide a group, cube or mesh in Blockbench. This means setting it on a group will affects its children as well.

### Parameters

A *boolean* representing whether or not the part is visible.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setVisible(false)

-- Function chaining example
models.player.Root.Head:setVisible(true):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getVisible" style="font-size: 2.5em;color:#00008B">getVisible</h1>

```lua
PartVisible = models.player.Root.Head:getVisible()
```

Gets the visibility of the model part. The value corresponds to the value passed in `setVisible()`, and by default is whether or not it is shown in Blockbench.

### Return Value

Returns a *boolean* representing whether or not the part is visible.

### Examples

```lua
HeadVisible = models.player.Root.Head:getVisible()
```
&nbsp;

***