---
parent: Player and Entities
layout: page
title: All Player Getters
---

<center style="font-size: 3em;">All Player Getters</center>

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
