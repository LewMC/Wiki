# Validation

## Checking if a variable is numeric
```java
class Example {
    public ExamplePlugin plugin;
    
    public Example(ExamplePlugin plugin) {
        this.plugin = plugin;
    }
    
    public void ExampleFunction() {
        Validation val = new Validation();
        
        val.isNumeric("1"); // true
        val.isNumeric("1.7"); // true
        val.isNumeric(1); // true
        val.isNumeric(1.7); // true
        
        val.isNumeric("hello"); // false
        val.isNumeric(true); // false
    }
    
    public void ExampleShorthand() {
        new Validation().isNumeric("1"); // true
        new Validation().isNumeric("a"); // false
    }
}
```