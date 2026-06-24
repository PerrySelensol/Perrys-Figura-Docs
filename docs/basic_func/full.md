---
layout: page
parent: Basic Functions
title: All Basic Functions
permalink: /figura-docs/basic_func/full
---

<center style="font-size: 3em;">Basic Functions</center>

***

<h1 id="print" style="font-size: 2.5em;color:#00008B">print</h1>

```lua
print_output = print(...)
```

Writes arguments to Minecraft's chat. Each of the argument printed will be concatenated and separated by a tab space.

### Parameters

Accepts any type of arguments.

### Return Value

Returns the *string* representation of all values.

### Examples

```lua
print("Hello World!")

print("Multiple arguments example", true, 2023, function() end, nil)

print(print("A valid example too!"))
```
&nbsp;

***

<h1 id="listFiles" style="font-size: 2.5em;color:#00008B">listFiles</h1>

```lua
fileTable = listFiles(path, include_subfolders)
```

Returns a table with all script file names from the specified `path`.

### Parameters

- A *string* `path` specifies which folder to start listing. If no path is specified, it will fetch from the root folder.

- An optional *boolean* `include_subfolders` to also list files inside subfolders.

### Return Value

Returns a *table* with all script file names from the specified `path`.

### Examples

To list script files located in `scripts/some_module` folder, either with or without subfolders.

```lua
local file_list = listFiles("scripts.some_module") -- Excluding Subfolders
local deep_list = listFiles("scripts.some_module", true) -- Including Subfolders

printTable(file_list)
printTable(deep_list)
```

To print every script file present in your avatar

```lua
printTable(listFiles("", true))
```
&nbsp;

***

<h1 id="require" style="font-size: 2.5em;color:#00008B">require</h1>

```lua
vararg = require(scriptName, fallbackFunction)
```

Runs a lua file if it hasn't already run yet.

### Parameters

- A *string* `scriptName` specifies a path to a lua file.

- An optional *function* `fallbackFunction` to be called instead if `scriptName` is invalid.

### Return Value

Returns the value that the file returns or `true` if there isn't any. If the script file has already run, then it only returns the value the file initially returned.

### Examples

To run a file called `foo` in `scripts/bar` then store its return value, and give out an error if the file doesn't exist.

```lua
local x = require(
    "scripts.bar.foo",
    function() error("No such file exists!") end
)
```
&nbsp;

***

<h1 id="printJson" style="font-size: 2.5em;color:#00008B">printJson</h1>

```lua
formattedOutput = printJson(...)
```

Prints JSON-formatted strings. All of the arguments will be concatenated together.

### Parameters

Any number of `string` arguments in a form of JSON text.

### Return Value

Returns the formatted string.

### Examples

```lua
printJson(
    '{"text":"Red","color":"red"}',
    '[{"text":"Blue","color":"blue"},{"text":"Green","color":"green"}]'
)
```

The code outputs

<code><span style="color:red">Red</span><span style="color:blue">Blue</span><span style="color:green">Green</span></code>

&nbsp;

***

<h1 id="printTable" style="font-size: 2.5em;color:#00008B">printTable</h1>

```lua
formattedOutput = printTable(object, depth, silent)
```

Prints an object as a formatted string.

### Parameters

- A *table* or any object type that Figura mod adds (such as vectors, matrices and modelPart) to be printed.

- An optional *number* `depth` to also print deeper entries in a table or Figura objects.

- An optional *boolean* `silent` to prevent formatted result from appearing in chat.

### Return Value

Returns the formatted string.

### Examples

```lua
local Table = {
    value = 42,
    array = {2,7,1,4},
    text = "tabler table!"
}

printTable(Table) --> prints value, array and text but not the contents of array

printTable(Table, 2) --> prints value, array, text AND the contents of array

-- Store formatted result without it being printed into chat
local result = printTable(Table, 2, true)
```
