This page will be highly procrastinated on.

All of the following variables/functions are globals in the source code of Infinite Yield. This will not list all of them since there is too much but it'll list some good ones for plugin development. Check the [Infinite Yield source](https://github.com/EdgeIY/infiniteyield/blob/master/source) if you wish to find more.

Friendly reminder, a [snippet](https://en.m.wikipedia.org/wiki/Snippet_(programming)) is not fully completed code.

## What are globals?

A local variable is accessible only in the block where it’s declared.

A global variable (non-local variable) is visible to all scopes of a script.

[Roblox variable documentation](https://create.roblox.com/docs/scripting/luau/variables).

```lua hl_lines="2"
local notglobal = "hello" --> local variable
global = "sup" --> global variable
```

For a better example of globals:

=== "Code"
	```lua hl_lines="2 5"
	print(yes)
	print(globalyes)

	local yes = "test"
	globalyes = "hi"
	```

=== "Output"
	``` hl_lines="2"
	nil
	hi
	```

## getstring

`getstring(num)`

`num` is a whole number. For example: 1, 3, 8, etc. Not 1.2, 5.9, etc.

=== "Code"
	```lua
	-- Note: This is just a snippet
	["Function"] = function(args, speaker)
		print(getstring(1))
	end
	```

=== "Command"
	```
	;test well hello there
	```

=== "Output"
	```
	well hello there
	```
??? question "Explained"
	The function converts the command's provided arguments into a complete string with spaces between each argument.

	`getstring(1)` used in the example will return a string which is the first argument and everything after it combined into a full string.
