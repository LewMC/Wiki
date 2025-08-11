# Commands

To register commands, you should have a command class ready to go. We recommend using one of the Foundry commands.

## What type of command do I need to register?
Regardless of if you're using a FoundryCommand or standard Bukkit-based executor, there's different ways to send commands
into the Foundry registry.

**If your command IS in your plugin.yml file, you need to use YML Commands.**
This format is generally recommended and preferred by developers.

**If your command IS NOT in your plugin.yml file, you need to use Runtime Commands.**
This format allows you to dynamically register commands, but means you can't use some plugin.yml features.

Both formats use the same style of method, just with different function names.

## YML Commands
> **This is the normal way to register commands, most plugins will use this method.** These commands MUST be defined in your plugin.yml file as is standard for Bukkit-based plugins.

_As of Foundry 1.2.0, command is now an alias of ymlCommand._

**Register a single command:** - It returns true/false, you can use this if you want or ignore it.
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new Registry(new FoundryConfig(this), this).command("example", new ExampleCommand());
    }
}
```

**Register multiple commands with different executors** - RECOMMENDED METHOD - this is probably the most common way of using this utility. Each call returns true/false, you can use this if you want or ignore it.
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.command("example", new ExampleCommand());
        registry.command("player", new ExamplePlayerCommand());
        registry.command("console", new ExampleConsoleCommand());
    }
}
```

**Register multiple commands with the same different executors** - Each call returns true/false, you can use this if you want or ignore it.
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.command(new String[] {"gamemode","gm"}, new ExampleCommand());
        registry.command(new String[] {"teleport","goto"}, new ExamplePlayerCommand());
    }
}
```

If your command has aliases in the plugin.yml, you only need to register the main command, it'll resolve the aliases automatically.

## Runtime Commands
<warning>
    <strong>Runtime commands should NOT be defined in your plugin.yml file.</strong>
    Due to this, they do not provide feedback if not registered.
    Most plugin authors will wish to use YML commands as shown above.
</warning>

If your command has aliases in the plugin.yml, you should pass them in as well.

**Register a single command:** - It returns true/false, you can use this if you want or ignore it.
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new Registry(new FoundryConfig(this), this).runtimeCommand("example", new ExampleCommand());
    }
}
```

**Register multiple commands with different executors** - Each call returns true/false, you can use this if you want or ignore it.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.runtimeCommand("example", new ExampleCommand());
        registry.runtimeCommand("player", new ExamplePlayerCommand(), "p", "play");
        registry.runtimeCommand("console", new ExampleConsoleCommand());
    }
}
```

**Register multiple commands with the same different executors** - Each call returns true/false, you can use this if you want or ignore it.
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.runtimeCommand(new String[] {"gamemode","gm"}, new ExampleCommand());
        registry.runtimeCommand(new String[] {"teleport","goto"}, new ExamplePlayerCommand());
    }
}
```

**Aliases do not register automatically**

Since there's no definition of this command in the plugin.yml, you'll need to tell it what the aliases of it are if you wish to register them as well.
To do so, simply pass them in as additional string arguments at the end of the call.

All three of the above methods support aliases.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        // Method 1:
        new Registry(new FoundryConfig(this), this).runtimeCommand("example", new ExampleCommand(), "alias1", "alias2", "etc");
        
        // Method 2:
        Registry registry = new Registry(new FoundryConfig(this), this);
        registry.runtimeCommand(new String[] {"gamemode","gm"}, new ExampleCommand(), "alias1", "alias2", "etc");
        
        // Method 3:
        Registry registry = new Registry(new FoundryConfig(this), this);
        registry.runtimeCommand(new String[] {"gamemode","gm"}, new ExampleCommand(), "alias1", "alias2", "etc");
    }
}
```