# Getting Started
> This section only applies to plugin developers. If you're a user, please check with the plugin developer if you need to download Foundry as it may be included in the plugin already.

There's two ways to include Foundry in your plugin, both with pros and cons.

| Compiling with      | Compiling without  |
|---------------------|--------------------|
| ❌ Larger Jarfile    | ✅ Smaller Jarfile  |
| ✅ Easier for Admins | ❌Harder for Admins |

## Compiling with Foundry
Compiling with Foundry means that Foundry is 

Add LewMC as a repository:
```xml
<repositories>
    <repository>
        <id>lewmc</id>
        <name>LewMC Repository</name>
        <url>https://repo.lewmc.net/releases</url>
    </repository>
</repositories>
```

Then add it as a dependency:
```xml
<dependencies>
    <dependency>
        <groupId>net.lewmc</groupId>
        <artifactId>foundry</artifactId>
        <version>1.0.0</version>
        <scope>compile</scope>
    </dependency>
</dependencies>
```
Note the scope is `compile`, this downloads Foundry and adds it to your plugin. 

You should also shade Foundry, so that it doesn't conflict with any other plugins:
```xml
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-shade-plugin</artifactId>
            <version>3.6.0</version>
            <configuration>
                <relocations>
                    <relocation>
                        <pattern>net.lewmc.foundry</pattern>
                        <shadedPattern>com.example.foundry</shadedPattern>
                    </relocation>
                </relocations>
            </configuration>
            <executions>
                <execution>
                    <phase>package</phase>
                    <goals>
                        <goal>shade</goal>
                    </goals>
                </execution>
            </executions>
        </plugin>
```
Add this to your &lt;plugins> section.

## Compiling without Foundry
<warning>
This currently does not work. Please use the previous method or wait for this method to become available.
</warning>

Add LewMC as a repository:
```xml
<repositories>
    <repository>
        <id>lewmc</id>
        <name>LewMC Repository</name>
        <url>https://repo.lewmc.net/releases</url>
    </repository>
</repositories>
```

Then add it as a dependency:
```xml
<dependencies>
    <dependency>
        <groupId>net.lewmc</groupId>
        <artifactId>foundry</artifactId>
        <version>1.0.0</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```
Note the scope is `provided`, this downloads Foundry and adds it to your plugin.

You don't need to shade the plugin using this method.

You'll now have access to Foundry methods, but you'll need to tell users to [download the Foundry plugin](Foundry.md).