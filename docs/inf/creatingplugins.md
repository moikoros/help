You're going to need some basic coding knowledge for this.

Infinite Yield plugins are a way for you to add custom content to your command list. You can share this content or keep it to yourself without worrying about editing Infinite Yield every time we release an update.

Plugins are `.iy` files and should be placed in the `workspace` folder of your executor.

Friendly reminder, a `[snippet](https://en.m.wikipedia.org/wiki/Snippet_(programming))` is not fully completed code.

## Setting Up

Start by opening your favorite Lua text editor (IDE). Examples: [Visual Studio Code](https://code.visualstudio.com/download), [Sublime Text](https://www.sublimetext.com/download), [Atom](https://github.com/atom/atom#installing), [Notepad++](https://notepad-plus-plus.org/downloads), etc.

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

`string ListName` : This is where you put your command (along with arguments in square brackets []). You can show the user and aliases here too. It's what shows up in the command list, meaning it's a visual feature.

`string Description` : The message you want to appear when the user hovers over the command in the command list for more information.

`table Aliases` : These are the aliases that you can use to run the command. Make sure that the table is sorted and each element of the table is an alias for your command. If you don't want to create any aliases for your command, leave this table empty.

=== "Aliases"
	```lua
	-- Note: This is just a snippet
	["Aliases"] = {"burgerman"}
	```

=== "None"
	```lua
	-- Note: This is just a snippet
	["Aliases"] = {}
	```

`function Function` : This is the function that is executed when the user runs your command.

A function for the command usually contains these arguments.

`table args` : A table containing the arguments passed into the command.

=== "Command with args"
	```
	;notify well hello there
	```

=== "Args table"
	```lua
	-- Note: This is just a snippet
	{"well", "hello", "there"}
	```

`Instance speaker` : The user's [player object](https://developer.roblox.com/api-reference/class/Player) (game.Players.LocalPlayer)

Infinite Yield contains global functions that you can use in commands. These are covered in the Plugin Functions page.

Each command should follow the following format.

```lua
-- Note: This is just a snippet
["exactcommand"] = { -- exactcommand is the exact text the person needs to run the command. example: audiologger
    ["ListName"] = "command [argument]",
    ["Description"] = "description here",
    ["Aliases"] = {"alias1", "alias2", "alias3"},
    ["Function"] = function(args, speaker)
        -- code here
    end
}
```

Here is an example.

```lua
local Plugin = {
    ["PluginName"] = "ExamplePlugin",
    ["PluginDescription"] = "This is a helpful template",
    ["Commands"] = {
        ["print"] = {
            ["ListName"] = "print [text]",
            ["Description"] = "Outputs text to the Roblox console",
            ["Aliases"] = {},
            ["Function"] = function(args, speaker)
                print(getstring(1))  
            end
        },
        ["notify"] = {
            ["ListName"] = "notify / alert [text]",
            ["Description"] = "uses the notification function",
            ["Aliases"] = {"alert"},
            ["Function"] = function(args, speaker)
                notify("Notification Title", getstring(1))
            end
        }
    }
}

return Plugin
```

If you are struggling, feel free to use the following template.

```lua
local Plugin = {
    ["PluginName"] = "name here",
    ["PluginDescription"] = "description here",
    ["Commands"] = {
        ["exactcommand"] = {
            ["ListName"] = "command [argument]",
            ["Description"] = "description here",
            ["Aliases"] = {"alias1", "alias2", "alias3"},
            ["Function"] = function(args, speaker)
                -- code here  
            end
        }
    }
}

return Plugin
```
