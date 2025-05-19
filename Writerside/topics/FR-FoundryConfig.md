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
    }
}
```