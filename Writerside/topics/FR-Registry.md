# Registry
The Foundry Registry allows you to register commands, tab completers, and event quickly. It also handles any potential exceptions or crashes as a result of the registration process.

## Commands
To register commands, you should have a command class ready to go. We recommend using one of the Foundry commands.

To register multiple commands with separate executors, the best way is to use this format:
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
This is probably the most common way of using this utility. Each statement returns true/false, you can use this if you want or ignore it.

To register multiple commands with the same executor, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.command(new String[] {"gamemode","gm"}, new ExampleCommand());
    }
}
```
The statement returns an array of true/false for each command, you can use this if you want or ignore it.

If your command has aliases, you can use one of the previous methods and just put the main command string in, it'll resolve the aliases automatically.

This is for multiple separate commands that are executed in the same class.
For example: Eseence uses this for its `/gamemode`, `/gmc`, `/gms`, etc. commands which are seperate according to Bukkit to allow us to give them different syntaxes, but on our end are processed by the same system.

To register a single command, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new Registry(new FoundryConfig(this), this).command("example", new ExampleCommand());
    }
}
```
The statement returns true/false, you can use this if you want or ignore it.

## Tab Completers
To register multiple tab completers, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.tabCompleter("example", new ExampleTabCompleter());
        registry.tabCompleter("player", new PlayerTabCompleter());
        registry.tabCompleter("console", new ConsoleTabCompleter());
    }
}
```
This is probably the most common way of using this utility. Each statement returns true/false, you can use this if you want or ignore it.

To register multiple commands with the same executor, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.tabCompleter(new String[] {"exampleOne","exampleTwo"}, new ExampleTabCompleter());
    }
}
```
The statement returns an array of true/false for each command, you can use this if you want or ignore it.

To register a single tab completer, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new Registry(new FoundryConfig(this), this).tabCompleter("example", new ExampleTabCompleter());
    }
}
```
The statement returns true/false, you can use this if you want or ignore it.

## Events
To register multiple events, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Registry registry = new Registry(new FoundryConfig(this), this);

        registry.event(new ExampleEvent());
        registry.event(new PlayerEvent());
        registry.event(new ConsoleEvent());
    }
}
```
This is probably the most common way of using this utility. Each statement returns true/false, you can use this if you want or ignore it.

To register a single event, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        new Registry(new FoundryConfig(this), this).event(new ExampleEvent());
    }
}
```
The statement returns true/false, you can use this if you want or ignore it.
