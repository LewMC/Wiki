# Events

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