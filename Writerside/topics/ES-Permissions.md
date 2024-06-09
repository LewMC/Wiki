# Permissions

You need to give your players permission to access certain commands. By default, all Essence commands are restricted to players with permissions. You can use a permission system such as LuckPerms (highly recommended) to give players these permissions. Server operators ("ops") can access every Essence command without requiring permissions.

Permissions are listed in the tables on the [commands page](ES-Commands.md).

### Wildcards vs Granular
Essence uses Wildcard permissions for some commands. The wildcard permission can be used if you'd like to give users access to all commands in that section, it makes writing permissions a whole lot faster! Wildcard permissions are shows at the top of each section. They look like this:
essence.gamemode.*
If you use wildcard permissions, you don't need to give players other permissions from that section. For example if you use essence.gamemode.* you don't need to also use essence.gamemode.survival as that permission is included in the wildcard.

Alternatively, you can use granular permissions if there are only certain commands in a section you'd like players to be able to use. They look like this:
essence.gamemode.survival

<seealso>
    <category ref="es-commands">
        <a href="ES-Commands.md">Commands</a>
        <a href="ES-Disabling-Commands.md">Disabling Commands</a>
    </category>
</seealso>