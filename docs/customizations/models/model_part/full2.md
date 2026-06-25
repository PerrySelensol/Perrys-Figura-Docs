---
parent: ModelPart Objects
layout: page
title: All Part Appearence
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

<h1 id="setUV" style="font-size: 2.5em;color:#00008B">setUV</h1>

```lua
HeadPart = models.player.Root.Head:setUV(u, v)

HeadPart = models.player.Root.Head:setUV(uv_vector)
```

Offsets the UV of this part from its original UV location.
The u and v values are normalized, i.e. ranges from 0 as no movement to 1 as fully moved across the whole image.

### Parameters

Either a *vector2* `uv_vector` or 2 *numbers* `u`, `v` representing the offset.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setUV(0.5, 0.25)

-- Function chaining example
models.player.Root.Head:setUV(0.5, 0.25):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getUV" style="font-size: 2.5em;color:#00008B">getUV</h1>

```lua
PartUV = models.player.Root.Head:getUV()
```

Gets the UV offset of this part from its original UV location. The value corresponds to the value passed to `setUV()` with `{0, 0}` being the default if there is no offset.
The u and v values are normalized, i.e. ranges from 0 as no movement to 1 as fully moved across the whole image.

### Return Value

Returns a *vector2* representing the offset.

### Examples

```lua
UV_vector = models.player.Root.Head:getUV()
```
&nbsp;

***

<h1 id="setUVPixels" style="font-size: 2.5em;color:#00008B">setUVPixels</h1>

```lua
HeadPart = models.player.Root.Head:setUVPixels(u, v)

HeadPart = models.player.Root.Head:setUVPixels(uv_vector)
```

Offsets the UV of this part from its original UV location. The u and v values are measured in pixels.

### Parameters

Either a *vector2* `uv_vector` or 2 *numbers* `u`, `v` representing the offset.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setUVPixels(20, -15)

-- Function chaining example
models.player.Root.Head:setUVPixels(20, -15):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getUVPixels" style="font-size: 2.5em;color:#00008B">getUVPixels</h1>

```lua
PartUV = models.player.Root.Head:getUVPixels()
```

Gets the UV offset of this part from its original UV location. The u and v values are measured in pixels. The value corresponds to the value passed to `setUVPixels()` with `{0, 0}` being the default if there is no offset.

### Return Value

Returns a *vector2* representing the offset.

### Examples

```lua
UV_vector = models.player.Root.Head:getUVPixels()
```
&nbsp;

***

<h1 id="setColor" style="font-size: 2.5em;color:#00008B">setColor</h1>

```lua
HeadPart = models.player.Root.Head:setColor(r, g, b)

HeadPart = models.player.Root.Head:setColor(rgb_vector)
```

Sets the color multiplier for this part for primary and secondary colors. This color will further tint the existing color on the model part's texture, making it darker. If you want your model part to be colorable via `setColor()`, make that part's image texture white.
Values are in RGB format, with each individual number ranges from 0 (darkest) to 1 (brightest).

Equivalent to calling both `setPrimaryColor()` and `setSecondaryColor()` with the same color passed to both.

### Parameters

Either a *vector3* `rgb_vector` or 3 *numbers* `r`, `g`, `b` representing the multipliers.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setColor(0.2, 0.5, 1)

-- Function chaining example
models.player.Root.Head:setColor(0.2, 0.5, 1):setRot(30, 0, 0)
```
&nbsp;

***

<h1 id="getColor" style="font-size: 2.5em;color:#00008B">getColor</h1>

```lua
PartRGB = models.player.Root.Head:getColor()
```

Gets the set color multiplier for this part. The value corresponds to either the following:
- If `setColor` was used, `getColor` simply gets the value passed into `setColor`.
- If primary and secondary colors were set separately via `setPrimaryColor()` and `setSecondaryColor()`, return an average of the two, i.e. `(primary + secondary)/2`.

### Return Value

Returns a *vector3* representing the color multiplier.

### Examples

```lua
RGB_Tint = models.player.Root.Head:getColor()
```
&nbsp;

***

<h1 id="setPrimaryColor" style="font-size: 2.5em;color:#00008B">setPrimaryColor</h1>

```lua
HeadPart = models.player.Root.Head:setPrimaryColor(r, g, b)

HeadPart = models.player.Root.Head:setPrimaryColor(rgb_vector)
```

Similar to [`setColor`](#setColor), except sets only primary color.

### Parameters

Either a *vector3* `rgb_vector` or 3 *numbers* `r`, `g`, `b` representing the multipliers.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setPrimaryColor(0.2, 0.5, 1)

-- Function chaining example
models.player.Root.Head:setPrimaryColor(0.2, 0.5, 1):setRot(30, 0, 0)
```
&nbsp;

***

<h1 id="getPrimaryColor" style="font-size: 2.5em;color:#00008B">getPrimaryColor</h1>

```lua
PartRGB = models.player.Root.Head:getPrimaryColor()
```

Gets the set primary color multiplier for this part. Corresponds to the value passed to `setPrimaryColor()`.

### Return Value

Returns a *vector3* representing the color multiplier.

### Examples

```lua
RGB_Tint = models.player.Root.Head:getPrimaryColor()
```
&nbsp;

***

<h1 id="setSecondaryColor" style="font-size: 2.5em;color:#00008B">setSecondaryColor</h1>

```lua
HeadPart = models.player.Root.Head:setSecondaryColor(r, g, b)

HeadPart = models.player.Root.Head:setSecondaryColor(rgb_vector)
```

Similar to [`setColor`](#setColor), except sets only secondary color.

### Parameters

Either a *vector3* `rgb_vector` or 3 *numbers* `r`, `g`, `b` representing the multipliers.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setSecondaryColor(0.2, 0.5, 1)

-- Function chaining example
models.player.Root.Head:setSecondaryColor(0.2, 0.5, 1):setRot(30, 0, 0)
```
&nbsp;

***

<h1 id="getSecondaryColor" style="font-size: 2.5em;color:#00008B">getSecondaryColor</h1>

```lua
PartRGB = models.player.Root.Head:getSecondaryColor()
```

Gets the set secondary color multiplier for this part. Corresponds to the value passed to `setSecondaryColor()`.

### Return Value

Returns a *vector3* representing the color multiplier.

### Examples

```lua
RGB_Tint = models.player.Root.Head:getSecondaryColor()
```
&nbsp;

***
