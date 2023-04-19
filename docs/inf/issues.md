For issues not listed here, please join the [Discord](https://discord.com/invite/78ZuWSq).

## Why is the script stuck on loading?

<img src="../../assets/stuck_loop.png" alt="infinite loading">

This is from a file corruption caused by your executor.

!!! example "Computer Solution"
	1. Go into the folder where your executor is located
	2. Look for a folder named `workspace` and open it
	3. Find the file named `IY_FE.iy`
	4. Send the file to an infinite yield developer in the discord (optional step)
	5. Delete the file
	6. Join a game and execute Infinite Yield
	
	Deleting this file will delete all your saved Infinite Yield settings (Prefix, Waypoints, etc.)

!!! example "Mobile Solution"
	Execute the following:
	
	```lua
	delfile("IY_FE.iy")
	```

	Deleting this file will delete all your saved Infinite Yield settings (Prefix, Waypoints, etc.)

## Why do some commands need a tool?

It needs a tool from the game itself that has a handle. An example of a handle is a sword. You hold the sword by it's handle which is usually an invisible block.

If there are no tools in the game then you can not use the command.

!!! warning "The sad truth"
	You can't spawn a tool with a script.
