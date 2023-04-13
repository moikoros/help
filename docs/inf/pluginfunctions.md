All of the following variables/functions are globals in the source code of Infinite Yield. This will not list all of them since there is too much but it'll list some good ones for plugin development. Check the [Infinite Yield source](https://github.com/EdgeIY/infiniteyield/blob/master/source) if you wish to find more.

??? question "What are globals?"
	A local variable is accessible only in the block where it’s declared.

	A global variable (non-local variable) is visible to all scopes of a script.

	```lua hl_lines="2"
	local notglobal = "hello" --> local, not global
	global = "sup" --> global, not local
	```

	[Roblox variable documentation](https://create.roblox.com/docs/scripting/luau/variables).
