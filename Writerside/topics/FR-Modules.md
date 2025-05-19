# Modules

Modules are self-contained sets of commands, tab completers, and events registered by the [Foundry Registry](FR-Registry.md).

## Using Modules
To make a Module, you should extend FoundryModule. Here's an example from Essence:
```Java
public class ModuleAdmin extends FoundryModule {
    public ModuleAdmin(@NotNull JavaPlugin plugin, @NotNull Registry reg) {
        super(plugin, reg);
    }

    @Override
    public void registerCommands() {
        reg.command("command", new ExampleCommand(plugin));
    }

    @Override
    public void registerTabCompleters() {
        reg.tabCompleter("command", new ExampleTabCompleter(plugin));
    }

    @Override
    public void registerEvents() {
        reg.tabCompleter(new ExampleEvent(plugin));
    }
}
```

Note that you may need to cast your plugin's main class to the plugin variable, shown below in an example from our plugin Essence.

```java
reg.command("info", new CommandInfo((Essence) plugin));
```

Now, from your plugin's main class (or wherever you'd like to load the module) add this:

```java
Registry reg = new Registry(this.config, this);
new ExampleModuleOne(plugin, reg);
new ExampleModuleTwo(plugin, reg);
```

For example, here's how we do it in Essence:

```java
public class Essence extends JavaPlugin {
    /* ... */
    private void loadModules() {
        Registry reg = new Registry(this.config, this);

        new ModuleAdmin(this, reg);
        new ModuleChat(this, reg);
        new ModuleCore(this, reg);
        new ModuleEconomy(this, reg);
        new ModuleGamemode(this, reg);
        new ModuleInventory(this, reg);
        new ModuleKit(this, reg);
        new ModuleStats(this, reg);
        new ModuleTeam(this, reg);
        new ModuleTeleportation(this, reg);
    }
    /* ... */
}
```

## When to use Modules
Whenever you'd like - we use them in Essence to help prevent code clutter, they're great for reducing the size of your main file and keeping stuff tidy.

## Foundry vs Traditional
They're not like traditional "modules" in the sense of they can't be removed or added on their own.

If you'd like to add this functionality it will require some additional programming.
However, Foundry modules can assist with that by holding all the code for each module in one place.