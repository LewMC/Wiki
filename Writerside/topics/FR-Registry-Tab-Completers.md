# Tab Completers

To register multiple tab completers, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        Registry registry = new Registry(this.foundryConfig, this);

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
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        Registry registry = new Registry(this.foundryConfig, this);

        registry.tabCompleter(new String[] {"exampleOne","exampleTwo"}, new ExampleTabCompleter());
    }
}
```
The statement returns an array of true/false for each command, you can use this if you want or ignore it.

To register a single tab completer, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        new Registry(this.foundryConfig, this).tabCompleter("example", new ExampleTabCompleter());
    }
}
```
The statement returns true/false, you can use this if you want or ignore it.
