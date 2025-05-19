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
FoundryCommands work just like standard Bukkit commands, you can register them using the built-in method or using our [Registry](FR-Registry.md).

### Registry
> We recommend using the Foundry Registry to register commands.

The Foundry Registry allows you to register commands quickly, and it handles any potential exceptions or crashes as a result of the registration process.

See [Registry](FR-Registry.md).

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