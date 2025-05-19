# Logging

## Standard logging

The `Logger` class contains a number of different logs:

```java
class Example {
    public void ExampleFunction() {
        Logger log = new Logger(new FoundryConfig(this));

        log.info("This is an informational log.");
        log.warn("This is a warning.");
        log.severe("This is a severe warning.");
        log.noConsole(); // This tells the console to go away!
    }
}
```

Outputs:

```
[00:00:00 INFO]: [EXAMPLE] This is an informational log.
[00:00:00 WARN]: [EXAMPLE] This is an informational log.
[00:00:00 SEVERE]: [EXAMPLE] This is an informational log.
```

## Preset Logs

Certain logs have preset messages;

```java
class Example {
    public void ExampleFunction() {
        Logger log = new Logger(new FoundryConfig(this));

        log.noConsole(); // This tells the console to go away!
    }
}
```

Outputs:

```
[00:00:00 WARN]: [EXAMPLE] Sorry, you need to be an in-game player to use this command.
```

## Single Logs
If you only need to output a single line of log, you can do a shorter version.
Using the info log as an example:

```java
class Example {
    public void ExampleFunction() {
        new Logger(new FoundryConfig(this)).info("This is an informational log.");
    }
}
```

That's two lines in one! It works in the same way, but only for one line.
If you're outputting more than one line you should create a variable and reference it instead of creating a new instance on each line.