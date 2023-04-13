All of the following variables/functions are globals in the source code of Infinite Yield. This will not list all of them since there is too much but it'll list some good ones for plugin development. Check the [Infinite Yield source](https://github.com/EdgeIY/infiniteyield/blob/master/source) if you wish to find more.

??? question "What are globals?"
	```lua hl_lines="2"
	local notglobal = "hello" --> local, not global
	global = "sup" --> global, not local
	```
