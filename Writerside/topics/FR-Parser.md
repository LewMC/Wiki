# Parser

## Extracting flags from string args
Extracts CLI-style flags from an array of strings (like the ones used in MC commands).
For example: `-g exampleFlag` will map to flags.get("g");

```java
class ExampleCommand {
    public void ExampleFunction(String[] args) {
        Parser parse = new Parser();
        
        Map<String, String> flags = parse.getFlags(args);
    }
}
```

## Checking if a variable is numeric
```java
class Example {
    public ExamplePlugin plugin;
    
    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void ExampleFunction() {
        Parser parse = new Parser();

        parse.isNumeric("1"); // true
        parse.isNumeric("1.7"); // true
        parse.isNumeric(1); // true
        parse.isNumeric(1.7); // true

        parse.isNumeric("hello"); // false
        parse.isNumeric(true); // false
    }
    
    public void ExampleShorthand() {
        new Parser().isNumeric("1"); // true
        new Parser().isNumeric("a"); // false
    }
}
```