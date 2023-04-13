All of the following variables/functions are globals in the source code of Infinite Yield. This will not list all of them since there is too much but it'll list some good ones for plugin development. Check the [Infinite Yield source](https://github.com/EdgeIY/infiniteyield/blob/master/source) if you wish to find more.

!!! question "What are globals?"
	A local variable is accessible only in the block where it’s declared.

	A global variable (non-local variable) is visible to all scopes of a script.

	```lua hl_lines="2"
	local notglobal = "hello" --> local variable
	global = "sup" --> global variable
	```

	[Roblox variable documentation](https://create.roblox.com/docs/scripting/luau/variables).

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
