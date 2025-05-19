# Files

> File handles YAML (.yml) files and directories only.

## Initialising the Class

Once constructed, you're good to start using the function on files.

If you need to open multiple files concurrently you can create more instances of the class and assign them to different variables.

Files will persist across functions if the variable is declared globally.

```java
class Example {
    public Files f;
    
    public Example() {
        Files this.f = new Files(new FoundryConfig(plugin), plugin);
        
        Files anotherfile = new Files(new FoundryConfig(plugin), plugin);
    }
}
```

## Handling Files

### Creating a File
When creating a file the function will return true or false, you can use that to display error/success messages.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        if (f.create("example.yml")) {
            // File was created!
        } else {
            // Couldn't create the file, throw an error message!
        }
    }
}
```

### Checking if a file exists
When using the function it will return true or false, you can use that to display error/success messages.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        if (f.exists("example.yml")) {
            // File was created!
        } else {
            // Couldn't create the file, maybe create it?
        }
    }
}
```

### Opening a File
Files are kept in memory, not assigned to a variable.
The below example shows how this works.

Files are opened from within the plugin's folder.
The file name is also parsed and checked using this function.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("config.yml"); // You don't need to assign this anything.
    }
}
```

If you'd like to access a file from outside of the plugin's folder, you can use the following:

You'll need to pass a native Java File into the function.

This function is more dangerous than the standard `load` as it does not check or parse the file name.
You should probably avoid using it where possible.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.loadNoReformat(new File("config.yml")); // You don't need to assign this anything.
    }
}
```

### Deleting a File
When using the function it will return true or false, you can use that to display error/success messages.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        if (f.delete("example.yml")) {
            // File was created!
        } else {
            // Couldn't delete the file, maybe do something else?
        }
    }
}
```

### Saving a File
> Saving a file also closes it. You don't need to use f.close() as well.

When using the function it will return true or false, you can use that to display error/success messages.

The `f.save()` function saves the current open file.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        if (f.save()) {
            // File was created!
        } else {
            // Couldn't save the file, hmm?
        }
    }
}
```

The `f.save(File)` function saves the current open file to a new location.

Note that File does not parse or check the passed file. It works from the server root, not the plugin folder. 

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        if (f.save(new File("newFile.yml"))) {
            // File was created! Maybe delete the old one?
        } else {
            // Couldn't save the file, maybe scream?
        }
    }
}
```

### Closing a File
> If you've used `f.save()` you do not need to close it as well.

Make sure to use `f.save()` if you've made changes.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        // If you've made changes.
        f.save();
        
        // If you've not made changes
        f.close();
    }
}
```

### Checking if a file is open
You can check if a file is open using `f.isOpen();`

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("example.yml");
        
        if (f.isOpen()) {
            // The file is open, hooray!
        } else {
            // The file is not open, what happened???
        }
    }
}
```

## Handling YAML contents

<warning>
    <strong>Setting a value does not save it.</strong> You must use f.save() to save your changes.
</warning>

### Setting a Key
When using the function it will return true or false, you can use that to display error/success messages.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("example.yml");
        
        // You can use any type of variable
        f.set("aBoolean", true);
        f.set("aString", "Hello");
        f.set("anInteger", 1);
        f.set("aDouble", 1.2);
    }
}
```

### Getting a Key's Value
When using the function it will return various things, you should use the relevant function.

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("example.yml");
        
        Object obj = f.get("anObject"); // Use this if you don't know what you're getting
        boolean bool = f.getBoolean("aBoolean");
        String str = f.getString("aString");
        int number = f.getInt("anInteger");
        double dbl = f.getDouble("aDouble");
        List<String> strList = f.getStringList("aStringList");
    }
}
```

## Getting a list of keys
```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("example.yml");
        
        // If the keys are the root keys, use this function.
        Set<String> keys = f.getKeys(true);
        
        // If you want keys within another key, use this one.
        Set<String> keys = f.getKeys("section", true);
        Set<String> keys = f.getKeys("section.anothersection", true);
    }
}
```

## Removing a key
This removes a key and it's content. It also returns true/false

```java
class Example {
    public Example() {
        Files f = new Files(new FoundryConfig(plugin), plugin);
        
        f.load("example.yml");
        
        if (f.remove("an.example.key")) {
            // It's gone!
        } else {
            // Oh no, it's still here...
        }
    }
}
```

## Preset Files
Certain files are preset, this is a part of an old system from our [Essence](Essence.md) plugin, but you're welcome to use the same structure as well if it works for you.

These files and directory structure are not made automatically, but they are used by the functions in this section.

```
plugins
┣ ExampleOne
┃ ┣ data
┃ ┃ ┗ players
┃ ┃   ┣ f81d4fae-7dec-11d0-a765-00a0c91e6bf6.yml (Example)
┃ ┃   ┗ 96ef93b3-b5a6-4c80-94c7-c44e2449029f.yml (Example)
┃ ┗ config.yml
┗ ExampleTwo
```

### Accessing preset files
```java
class Example {
    public ExampleCommand(CommandSender cs) {
        if (CommandSender instanceof Player p) {
            Files f = new Files(new FoundryConfig(plugin), plugin);

            // If you have an instance of Player use this.
            f.load(f.playerDataFile(p));

            // Or if you have their UUID use this
            f.load(f.playerDataFile(p.getUniqueId()));
        } else {
            // The command sender isn't a player!
        }
    }
}
```