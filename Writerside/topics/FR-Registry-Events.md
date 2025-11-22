# Events

To register multiple events, the best way is to use this format:
```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        Registry registry = new Registry(this.foundryConfig, this);

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
    public FoundryConfig foundryConfig;
    
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        new Registry(this.foundryConfig, this).event(new ExampleEvent());
    }
}
```
The statement returns true/false, you can use this if you want or ignore it.