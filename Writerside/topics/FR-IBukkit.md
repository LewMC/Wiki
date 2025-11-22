# IBukkit

<warning>
    <strong>IBukkit accesses Bukkit's internal classes.</strong> Caution is required when using these functions.
</warning>

## Accessing the CommandMap
You can access Bukkit's command map using Foundry.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        
        IBukkit ib = new IBukkit(foundryConfig, this);
        CommandMap cm = ib.getCommandMap();
        
        // or
        
        CommandMap cm = new IBukkit(foundryConfig, this).getCommandMap();
    }
}
```

## Accessing the PluginManager
You can access Bukkit's plugin manager using Foundry.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        
        IBukkit ib = new IBukkit(foundryConfig, this);
        PluginManager pm = ib.getPluginManager();
        
        // or

        PluginManager pm = new IBukkit(foundryConfig, this).getPluginManager();
    }
}
```

## Constructing runtime commands
You can construct runtime commands using Foundry. This example will create a PluginCommand "/example".

This does not register the command. To register commands use [the registry](FR-Registry.md)'s runtimeCommand function **instead** of this.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        
        IBukkit ib = new IBukkit(foundryConfig, this);
        PluginCommand runtimeCommand = ib.constructRuntimeCommand("example");

        // or

        PluginCommand runtimeCommand = new IBukkit(foundryConfig, this).constructRuntimeCommand("example");
    }
}
```