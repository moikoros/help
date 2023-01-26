You're going to need some basic coding knowledge for this.

Infinite Yield plugins are a way for you to add custom content to your command list. You can share this content or keep it to yourself without worrying about editing Infinite Yield every time we release an update.

Plugins are `.iy` files and should be placed in the `workspace` folder of your executor.

## Setting Up

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

## Adding Commands

Once you have a plugin setup, you are ready to start adding commands in the `Commands` table. Each command is a key in the table that is usually named the command.

Every command is a table. Here are the keys for each command.

`string ListName` : This is where you put your command (along with arguments in square brackets []). You can show the user and aliases here too.

`string Description` : The message you want to appear when the user hovers over the command in the command list for more information.

`table Aliases` : These are the aliases that you can use to run the command. Make sure that the table is sorted and each element of the table is an alias for your command. If you don't want to create any aliases for your command, leave this table empty.

`function Function` : This is the function that is executed when the user runs your command.
