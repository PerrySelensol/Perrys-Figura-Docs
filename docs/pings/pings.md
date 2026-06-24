---
layout: page
parent: Figura Documentation
title: Pings
permalink: /figura-docs/pings
---

<center style="font-size: 3em;">Pings</center>

***

Figura avatars are client-sided. That means when others see your avatar, they actually see a copy of your avatar on your player entity running its script on their own computer independently from your avatar running its own scripts on your computer.

This means functions that you manually run by yourself (such as those from your action wheel or from `/figura run`) will not be executed on others' copy of your avatar.

Pings allow you to run a function on everyone's copy of your avatar and also send a piece of information to everyone who has your avatar loaded. Thus, they allow you to synchronize certain aspects of your avatar (such as outfits, animations played or poses.)

More simply, pings are functions that are inside the figura's `ping` table; thus a ping function can be created as follow:

```lua
function pings.MyPing(...)
    ...
end
```

When this function is called on your avatar, the function will also be called on others' computer and all arguments passed in will be sent to their computer as well.

### Examples

To see a difference between regular functions and pings, start with a script in your avatar below. This will define two functions: a regular lua function and a ping function.

```lua
function NormalFunction(arg)
    print(arg)
end

function pings.PingFunction(arg)
    print(arg)
end
```

To manually run these functions, use `/figura run` command to manually run a lua code.

If `/figura run NormalFunction("Hello World")` is run, the string "Hello World" will be printed only on your computer.

However, if `/figura run pings.PingFunction("Hello World")` is run, the string "Hello World" will be printed on everyone who has your avatar loaded. Note that the string itself is an argument passed into the ping function and it has been sent to others' computer so they can see the same message as you see on your own computer.