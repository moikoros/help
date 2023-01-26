Infinite Yield plugins are a way for you to add custom content to your command list. You can share this content or keep it to yourself without worrying about editing Infinite Yield every time we release an update.

Plugins are `.iy` files and should be placed in the `workspace` folder of your executor.

Start by opening your favorite Lua text editor (Examples: Notepad++, Atom, Visual Studio Code, Sublime Text, etc.).

Next, create a script that returns a table. I recommend that you name the table `Plugin`.

```lua
local Plugin = {
}

return Plugin
```

Now you need to set up the properties of the plugin and the `Commands` table by adding keys to your `Plugin` table.

The following is the basic keys used to set plugin properties:

`string PluginName` : The name of your plugin. Keep in mind that your file name must match the value of this property.

`string PluginDescription` : The description of your plugin. If the plugin name is self-explanatory, use this as the credits.

`table Commands` : A table where all of your commands will be created.

Here is a template to guide you.

```lua
local Plugin = {
    ["PluginName"] = "NAME HERE",
    ["PluginDescription"] = "DESCRIPTION HERE",
    ["Commands"] = {
    }
}

return Plugin
```
