# FoundryConfig

FoundryConfig holds information about your plugin. The class takes a reference to your main plugin class. Most of
Foundry's classes require a FoundryConfig to be present.

**We recommend storing FoundryConfig in your main class. See 'Best Practice' for more information.**
Most examples in this wiki will use FoundryConfig from within your main class, therefore we recommend you do the same.

## From a class
```java
class Example {
    public ExamplePlugin plugin;

    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void anExampleFunction() {
        Logger log = new Logger(new FoundryConfig(this.plugin)); // Not best practice, but works.
        Logger log = new Logger(this.plugin.foundryConfig); // Best practice, see 'Best Practice' below.
    }
}
```

That's an example of how to setup a Foundry class with FoundryConfig.
The below snippet is a basic example.

```java
new FoundryConfig(plugin);
```

`plugin` refers to your plugin's main class.

```java
class Example {
    public ExamplePlugin plugin;
    public FoundryConfig foundryConfig;

    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void anExampleFunction() {
        // Not best practice, but works.
        Logger log = new Logger(new FoundryConfig(this.plugin));
        Security sec = new Security(new FoundryConfig(this.plugin));
        
        // Not best practice, but works.
        FoundryConfig localConfig = new FoundryConfig(this.plugin);
        Logger log = new Logger(localConfig);
        Security sec = new Security(localConfig);

        // Best practice, see 'Best Practice' below.
        this.foundryConfig = new FoundryConfig(this.plugin);
        Logger log = new Logger(this.foundryConfig);
        Security sec = new Security(this.foundryConfig);
    }
}
```

## From the main class
If you're using FoundryConfig from within your plugin's main class you can simply use `this`.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        // Not best practice, but works.
        Security sec = new Security(new FoundryConfig(this));
        
        // Not best practice, but works.
        FoundryConfig localConfig = new FoundryConfig(this);
        Security sec = new Security(localConfig);

        // Best practice, see 'Best Practice' below.
        this.foundryConfig = new FoundryConfig(this);
        Security sec = new Security(foundryConfig);
    }
}
```

## Best Practice
It's best practice to store the FoundryConfig instance in your main class, then reference it in all other instances.
This way, you won't have to re-create the FoundryConfig instance every time you need it.

The examples provided here might make this seem useless or overkill, but if you're using Foundry in multiple classes
this makes it much easier to keep track of your plugin's configuration, and much easier to use Foundry overall. When
done like this, any changes made to Foundry's config from any class will be reflected in all other classes automatically.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        
        new ExampleClass(this.foundryConfig);
    }
}

public class ExampleClass {
    public ExampleClass(FoundryConfig config) {
        Security sec = new Security(config);
    }
}
```

This way, you can also ensure your foundryConfig is always up to date across your plugin. For an example of this in
action, check out [](Essence.md)'s GitHub repository.

## Verbose mode
By default, Foundry operations in a 'supressed' mode, where only necessary information is outputted.
Typically, this is the mode you'll want.

However, if you'd like to debug issues, Foundry is able to output more information including [Files](FR-Files.md) actions.

To do this, you'll need to set verbose mode to true when setting up Foundry.
You must assign FoundryConfig to a variable to do this.

Note that this only sets the verbose value for this instance of FoundryConfig, not all. If you'd like this to be global
we recommend saving the instance in your main class then referencing it in all other instances.


```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        this.foundryConfig.setVerbose(true);

        // Foundry is now verbose
        // Do more stuff now it's set.
        Security sec = new Security(this.foundryConfig);
        
        // Don't want the stuff after to be verbose?
        // You can change it back!
        this.foundryConfig.setVerbose(false);
    }
}
```

## Plugin IDs
Foundry automatically gives your plugin an ID, it's usually your plugin's name.

If you wish, you can overwrite this ID by using the setPluginID function.

Note that this only overwrites the plugin ID for this instance of FoundryConfig, not all. If you'd like this to be global
we recommend saving the instance in your main class then referencing it in all other instances.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;

    @Override
    public void onEnable() {
        this.config = new FoundryConfig(this);
        this.foundryConfig.setPluginId("my-custom-id");
    }
}
```