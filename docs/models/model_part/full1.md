---
layout: page
parent: ModelPart Objects
title: All Part Transformations
permalink: /figura-docs/models/model_part/full1
---

<center style="font-size: 3em;">ModelPart Functions</center>

<center style="font-size: 2em;">Part Transformations</center>

***

<h1 id="setPos" style="font-size: 2.5em;color:#00008B">setPos</h1>

```lua
HeadPart = models.player.Root.Head:setPos(x, y, z)

HeadPart = models.player.Root.Head:setPos(xyz_vector)
```

Sets the position offset and its pivot for this part from its Blockbench position.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the offset. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setPos(1, 2, 3)

models.player.Root.Head:setPos(vec(3, 6, 5))

-- Function chaining example
models.player.Root.Head:setPos(vec(3, 6, 5)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getPos" style="font-size: 2.5em;color:#00008B">getPos</h1>

```lua
PartPos = models.player.Root.Head:getPos()
```

Gets the position offset of the model part. The values corresponds to the value passed in `setPos()`, and thus by default is `vec(0,0,0)`.

### Return Value

Returns a *vector3* which is the position offset of the model part.

### Examples

```lua
HeadPos = models.player.Root.Head:getPos()
```
&nbsp;

***

<h1 id="setRot" style="font-size: 2.5em;color:#00008B">setRot</h1>

```lua
HeadPart = models.player.Root.Head:setRot(x, y, z)

HeadPart = models.player.Root.Head:setRot(xyz_vector)
```

Sets the absolute rotation for this part in degrees. The rotation corresponds exactly to the "Rotation" property in Blockbench, and thus are Euler angles in XYZ order (the format that Blockbench use.)

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the absolute rotation. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setRot(30, 45, -60)

models.player.Root.Head:setRot(vec(30, 45, -60))

-- Function chaining example
models.player.Root.Head:setRot(vec(30, 45, -60)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getRot" style="font-size: 2.5em;color:#00008B">getRot</h1>

```lua
PartRot = models.player.Root.Head:getRot()
```

Gets the absolute rotation of the model part in degrees. The values corresponds to the value passed in `setRot()`, but by default would be the value of "Rotation" property in Blockbench. The angles are in Euler angles in XYZ order.

### Return Value

Returns a *vector3* which is the absolute rotation of the model part.

### Examples

```lua
HeadRot = models.player.Root.Head:getRot()
```
&nbsp;

***

<h1 id="setScale" style="font-size: 2.5em;color:#00008B">setScale</h1>

```lua
HeadPart = models.player.Root.Head:setScale(x, y, z)

HeadPart = models.player.Root.Head:setScale(xyz_vector)
```

Sets the scale of this part along its local X, Y and Z axis.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the scale factors. Nil values are taken as 1.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setScale(1, 0.5, 2)

models.player.Root.Head:setScale(vec(1, 0.5, 2))

-- Function chaining example
models.player.Root.Head:setScale(vec(1, 0.5, 2)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getScale" style="font-size: 2.5em;color:#00008B">getScale</h1>

```lua
PartScale = models.player.Root.Head:getScale()
```

Gets the scale factors of the part in its local X, Y and Z axis. The values corresponds to the value passed in `setScale()`

### Return Value

Returns a *vector3* which are the scale factors of the part in its local X, Y and Z axis, and are defaulted to `vec(1,1,1)`.

### Examples

```lua
HeadScale = models.player.Root.Head:getScale()
```
&nbsp;

***

<h1 id="setPivot" style="font-size: 2.5em;color:#00008B">setPivot</h1>

```lua
HeadPart = models.player.Root.Head:setPivot(x, y, z)

HeadPart = models.player.Root.Head:setPivot(xyz_vector)
```

Sets the absolute pivot of this part, the numbers correspond exactly to "Pivot&nbsp;Point" property in Blockbench. This effectively changes the center of rotation of a part.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the pivot position. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setPivot(0, 0, 2)

models.player.Root.Head:setPivot(vec(0, 0, 2))

-- Function chaining example
models.player.Root.Head:setPivot(vec(0, 0, 2)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getPivot" style="font-size: 2.5em;color:#00008B">getPivot</h1>

```lua
PartPivot = models.player.Root.Head:getPivot()
```

Gets the absolute pivot of this part. The values corresponds to the value passed in `setPivot()`

### Return Value

Returns a *vector3* which is the absolute pivot of this part, by default this would be the value of "Pivot&nbsp;Point" property in Blockbench.

### Examples

```lua
HeadPivot = models.player.Root.Head:getPivot()
```
&nbsp;

***

<h1 id="setOffsetRot" style="font-size: 2.5em;color:#00008B">setOffsetRot</h1>

```lua
HeadPart = models.player.Root.Head:setOffsetRot(x, y, z)

HeadPart = models.player.Root.Head:setOffsetRot(xyz_vector)
```

Sets the **offset** rotation for this part in degrees. The rotation adds to the rotation set by `setRot()`.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the rotation offset. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setOffsetRot(30, 45, -60)

models.player.Root.Head:setOffsetRot(vec(30, 45, -60))

-- Function chaining example
models.player.Root.Head:setOffsetRot(vec(30, 45, -60)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getOffsetRot" style="font-size: 2.5em;color:#00008B">getOffsetRot</h1>

```lua
PartOffsetRot = models.player.Root.Head:getOffsetRot()
```

Gets the **offset** rotation of the model part in degrees. The values corresponds to the value passed in `setOffsetRot()`.

### Return Value

Returns a *vector3* which is the offset rotation of the model part.

### Examples

```lua
HeadOffsetRot = models.player.Root.Head:getOffsetRot()
```
&nbsp;

***

<h1 id="setOffsetScale" style="font-size: 2.5em;color:#00008B">setOffsetScale</h1>

```lua
HeadPart = models.player.Root.Head:setOffsetScale(x, y, z)

HeadPart = models.player.Root.Head:setOffsetScale(xyz_vector)
```

Sets the **offset** scale of this part along its local X, Y and Z axis. The scale multiplies to scale set by `setScale()`.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the offset scale factors. Nil values are taken as 1.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setOffsetScale(1, 0.5, 2)

models.player.Root.Head:setOffsetScale(vec(1, 0.5, 2))

-- Function chaining example
models.player.Root.Head:setOffsetScale(vec(1, 0.5, 2)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getOffsetScale" style="font-size: 2.5em;color:#00008B">getOffsetScale</h1>

```lua
PartOffsetScale = models.player.Root.Head:getOffsetScale()
```

Gets the **offset** scale factors of the part in its local X, Y and Z axis. The values corresponds to the value passed in `setOffsetScale()`

### Return Value

Returns a *vector3* which are the offset scale factors of the part in its local X, Y and Z axis, and are defaulted to `vec(1,1,1)`.

### Examples

```lua
HeadOffsetScale = models.player.Root.Head:getOffsetScale()
```
&nbsp;

***

<h1 id="setOffsetPivot" style="font-size: 2.5em;color:#00008B">setOffsetPivot</h1>

```lua
HeadPart = models.player.Root.Head:setOffsetPivot(x, y, z)

HeadPart = models.player.Root.Head:setOffsetPivot(xyz_vector)
```

Sets the **offset** pivot of this part, the numbers adds to the value set by `setPivot()`.

### Parameters

Either a *vector3* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the pivot offset. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setOffsetPivot(0, 0, 2)

models.player.Root.Head:setOffsetPivot(vec(0, 0, 2))

-- Function chaining example
models.player.Root.Head:setOffsetPivot(vec(0, 0, 2)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getOffsetPivot" style="font-size: 2.5em;color:#00008B">getOffsetPivot</h1>

```lua
PartOffsetPivot = models.player.Root.Head:getOffsetPivot()
```

Gets the offset pivot of this part. The values corresponds to the value passed in `setOffsetPivot()`

### Return Value

Returns a *vector3* which is the offset pivot of this part.

### Examples

```lua
HeadOffsetPivot = models.player.Root.Head:getOffsetPivot()
```
&nbsp;

***

<h1 id="getTruePos" style="font-size: 2.5em;color:#00008B">getTruePos</h1>

```lua
PartTruePos = models.player.Root.Head:getTruePos()
```

Gets the true position of this part, which is the position after `setPos()` and Blockbench animations are applied.

### Return Value

Returns a *vector3* which is the true position of this part.

### Examples

```lua
HeadTruePos = models.player.Root.Head:getTruePos()
```
&nbsp;

***

<h1 id="getTrueRot" style="font-size: 2.5em;color:#00008B">getTrueRot</h1>

```lua
PartTrueRot = models.player.Root.Head:getTrueRot()
```

Gets the true rotation of this part, which is the rotation after `setRot()`, `setOffsetRot()` and Blockbench animations are applied.

### Return Value

Returns a *vector3* which is the true rotation of this part.

### Examples

```lua
HeadTrueRot = models.player.Root.Head:getTrueRot()
```
&nbsp;

***

<h1 id="getTrueScale" style="font-size: 2.5em;color:#00008B">getTrueScale</h1>

```lua
PartTrueScale = models.player.Root.Head:getTrueScale()
```

Gets the true scale of this part, which is the scale after `setScale()`, `setOffsetScale()` and Blockbench animations are applied.

### Return Value

Returns a *vector3* which is the true scale of this part.

### Examples

```lua
HeadTrueScale = models.player.Root.Head:getTrueScale()
```
&nbsp;

***

<h1 id="getTruePivot" style="font-size: 2.5em;color:#00008B">getTruePivot</h1>

```lua
PartTruePivot = models.player.Root.Head:getTruePivot()
```

Gets the true pivot of this part, which is the pivot after `setPivot()` and `setOffsetPivot()` are applied.

### Return Value

Returns a *vector3* which is the true pivot of this part.

### Examples

```lua
HeadTruePivot = models.player.Root.Head:getTruePivot()
```
&nbsp;

***

<h1 id="getAnimPos" style="font-size: 2.5em;color:#00008B">getAnimPos</h1>

```lua
PartAnimPos = models.player.Root.Head:getAnimPos()
```

Gets the position offset applied by all currently playing Blockbench animations. The value corresponds to those "Position" channel values in Blockbench of each animation, all added together.

### Return Value

Returns a *vector3* which is the sum of all playing Blockbench animation offset applied to this part.

### Examples

```lua
HeadAnimPos = models.player.Root.Head:getAnimPos()
```
&nbsp;

***

<h1 id="getAnimRot" style="font-size: 2.5em;color:#00008B">getAnimRot</h1>

```lua
PartAnimRot = models.player.Root.Head:getAnimRot()
```

Gets the rotation offset applied by all currently playing Blockbench animations. The value corresponds to those "Rotation" channel values in Blockbench of each animation, all added together.

### Return Value

Returns a *vector3* which is the sum of all playing Blockbench animation offset applied to this part.

### Examples

```lua
HeadAnimRot = models.player.Root.Head:getAnimRot()
```
&nbsp;

***

<h1 id="getAnimScale" style="font-size: 2.5em;color:#00008B">getAnimScale</h1>

```lua
PartAnimScale = models.player.Root.Head:getAnimScale()
```

Gets the scale offset applied by all currently playing Blockbench animations. The value corresponds to those "Scale" channel values in Blockbench of each animation, all multiplied together.

### Return Value

Returns a *vector3* which is the product of all playing Blockbench animation offset applied to this part.

### Examples

```lua
HeadAnimScale = models.player.Root.Head:getAnimScale()
```
&nbsp;

***