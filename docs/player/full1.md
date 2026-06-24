---
layout: page
parent: Player and Entities
title: All Player Getters
permalink: /figura-docs/player/full1
---

<center style="font-size: 3em;">Player Functions</center>

<center style="font-size: 2em;">Getters</center>

***

<h1 id="getAbsorptionAmount" style="font-size: 2.5em;color:#00008B">getAbsorptionAmount</h1>

```lua
absorptionAmount = player:getAbsorptionAmount()
```

Gets absorption points. That is, the amount of yellow hearts measured in half-hearts.

### Return Value

Returns *number* representing absorption points.

### Examples

```lua
models.player.Root.Head:setVisible(false)

-- Function chaining example
models.player.Root.Head:setVisible(true):setColor(0, 0.5, 1)
```
&nbsp;

***
