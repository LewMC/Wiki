# Commands

## Foundry Commands
Foundry provides classes for handling commands. These classes allow for automatic permission and entity checks.

Three classes are provided: `FoundryCommand`, `FoundryPlayerCommand`, and `FoundryConsoleCommand`.
Each class has a specific purpose as shown in the table below.
If a player tries to run a console-only command (or vice versa) then an error is thrown and the command does not execute.

| Class                 | Runnable by Players | Runnable from the Console |
|-----------------------|---------------------|---------------------------|
| FoundryCommand        | ✅                   | ✅                         |
| FoundryPlayerCommand  | ✅                   | ❌                         |
| FoundryConsoleCommand | ❌                   | ✅                         |

The class's content requirements are exactly the same, and you can therefore switch between or back to FoundryCommand without having to change anything else.

### Examples
```java
package net.lewmc.foundry.command;

import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;

public class ExampleCommand extends FoundryCommand {
    @Override
    protected String requiredPermission() {
        return "the.required.permission";
    }

    @Override
    protected boolean onRun(CommandSender sender, Command command, String label, String[] args) {
        // Your command logic here.
        return false;
    }
}
```

To create player-only commands or console-only commands, simply replace `FoundryCommand`.

```java
public class ExamplePlayerCommand extends FoundryPlayerCommand { /* ... */ }
```
```java
public class ExampleConsoleCommand extends FoundryConsoleCommand { /* ... */ }
```

## Registering Commands
FoundryCommands work just like standard Bukkit commands, you can register them using the built-in method or using our CommandRegistry.

### CommandRegistry
The Foundry CommandRegistry allows you to register commands quickly, and it handles any potential exceptions or crashes as a result of the registration process.

To register commands, you should have a command class ready to go. We recommend using one of the Foundry commands.

To register a single command, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new CommandRegistry(new FoundryConfig(this), this).register("example", new ExampleCommand());
    }
}
```

To register multiple commands, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        CommandRegistry commands = new CommandRegistry(new FoundryConfig(this), this);
        
        commands.register("example", new ExampleCommand());
        commands.register("player", new ExamplePlayerCommand());
        commands.register("console", new ExampleConsoleCommand());
    }
}
```

### Bukkit
The traditional Bukkit method of registering commands also works with Foundry Commands.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        this.plugin.getCommand("example").setExecutor(new ExampleCommand());
    }
}
```

Be aware that this may throw a NullPointerException unless handled, as with any Bukkit command.