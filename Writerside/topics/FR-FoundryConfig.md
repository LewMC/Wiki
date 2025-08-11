# FoundryConfig

FoundryConfig holds information about your plugin. The class takes a reference to your main plugin class.

Most of Foundry's classes require a FoundryConfig to be present.

## From a class
```java
class Example {
    public ExamplePlugin plugin;

    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void anExampleFunction() {
        Logger log = new Logger(new FoundryConfig(this.plugin));
    }
}
```

That's an example of how to setup a Foundry class with FoundryConfig.
The below snippet is a basic example.

```java
new FoundryConfig(plugin);
```

`plugin` refers to your plugin's main class.

If you're using multiple Foundry classes, we recommend assigning FoundryConfig to a variable.

```java
class Example {
    public ExamplePlugin plugin;

    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void anExampleFunction() {
        FoundryConfig config = new FoundryConfig(this.plugin);
        
        Logger log = new Logger(config);
        Security sec = new Security(config);
    }
}
```

## From the main class
If you're using FoundryConfig from within your plugin's main class you can simply use `this`.

```java
public class ExamplePlugin extends JavaPlugin {
    @Override
    public void onEnable() {
        Security sec = new Security(new FoundryConfig(this));
        
        // or
        
        FoundryConfig config = new FoundryConfig(this);
        Security sec = new Security(config);
    }
}
```

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
    @Override
    public void onEnable() {
        FoundryConfig config = new FoundryConfig(this);
        config.setVerbose(true);

        // Foundry is now verbose
        // Do more stuff now it's set.
        Security sec = new Security(config);
        
        // Don't want the stuff after to be verbose?
        // You can change it back!
        config.setVerbose(false);
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
    @Override
    public void onEnable() {
        FoundryConfig config = new FoundryConfig(this);
        config.setPluginId("my-custom-id");
    }
}
```