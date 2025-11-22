# Security

The `Security` class contains a number of security functions:

## Special Character Check
Special characters may pose security risks or bugs in certain scenarios, this simple function helps to identify if they may pose a risk.

```java
class Example {
    public ExamplePlugin plugin;
    
    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void ExampleFunction() {
        Security sec = new Security(this.plugin.foundryConfig);
        
        sec.hasSpecialCharacters("Does this have special?"); // true
        sec.hasSpecialCharacters("Does this have special"); // false
    }
}
```

## Watchdog
Watchdog is a security feature designed to "watch" your plugin for abnormal behaviours.
It's designed to be started once in the onEnable() command.

Watchdog currently performs the following tasks:
- Identifies plugin reloads and informs admins of the risks.

### Starting Watchdog
You should only start watchdog in the onEnable() function or a function that performs the same task.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;

    // This fires when the plugin first loads
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        new Security(this.foundryConfig).startWatchdog();
    }
}
```

### Stopping Watchdog

Watchdog can be stopped at any time. You don't need to stop Watchdog on plugin shutdown/disable, it will reset itself automatically.

For example, if your plugin reloads itself you might not want Watchdog to catch that.

```java
public class ExamplePlugin extends JavaPlugin {
    public FoundryConfig foundryConfig;
    
    // This fires when the plugin first loads or is reloaded using /reload
    @Override
    public void onEnable() {
        this.foundryConfig = new FoundryConfig(this);
        this.loadSelf();
    }

    // This fires when the plugin reloads itself (example - doesn't actually work)
    // In this case, we know it's being reloaded as it's a plugin feature.
    // Therefore, we wish to suspend Watchdog so it can be restarted later.
    // This prevents the warning from appearing.
    public void reloadSelf() {
        new Security(this.foundryConfig).stopWatchdog();
        this.loadSelf();
    }
    
    // This is fired both times, starting Watchdog.
    public void loadSelf() {
        new Security(this.foundryConfig).startWatchdog();
    }
}
```