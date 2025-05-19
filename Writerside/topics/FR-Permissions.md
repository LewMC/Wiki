# Permissions

Permissions is a system that handles permissions (does what it says on the tin!)

As with all classes, there's multiple ways to use it:

```java
class Example {
    public void functionWithSingleCheck(CommandSender cs) {
        if (new Permissions(cs).has("example.permission")) {
            // The user has the permission.
        } else {
            // The user does not have the permission.
        }
    }
    
    public void functionWithMultiCheck(CommandSender cs) {
        Permissions perms = new Permissions(cs);
        
        if (perms.has("example.permission")) {
            // The user has the permission.
        } else {
            // The user does not have the permission.
        }
        
        if (perms.has("example.permission.another")) {
            // The user has the permission.
        } else {
            // The user does not have the permission.
        }
    }
}
```

Type Player can be cast to CommandSender and vice-versa.