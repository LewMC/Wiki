# Disabling Commands

<warning>
    <strong>This feature is not recommended. Please consider alternatives such as permissions.</strong>
    This does not remove the commands from /help or /es help at this time, it also does not prevent the server from recognising they exist.
</warning>

To disable commands in Essence, you can add them to a list in the configuration file.

1. Open Essence's config.yml
2. Scroll to disabled-commands.
3. Add any commands you'd like to disable. Most codes are what you'd expect, but since some commands have aliases we've included the full list below.
4. Restart your server

## Limitations and Drawbacks
If you're looking to disable a command because you prefer another plugin's (or vanilla's) alternative, this system likely won't work for you. Spigot requires Essence to register commands in the plugin.yml file, because of this the server still expects the command to work. Since Essence has disabled the command it will refuse to process it, causing the default error message to appear in chat. Here's an example with the /tp command disabled:

![es-disabling-commands.png](es-disabling-commands.png)

If you want to use a vanilla command, you can append minecraft: to it. For example: /minecraft:teleport

## Alternatives
Permissions! Essence has a robust permissions system - simply disallow players from using the commands. This gives them an error message instead of it appearing as though the command doesn't work at all.

<seealso>
    <category ref="es-commands">
        <a href="ES-Commands.md">Commands</a>
        <a href="ES-Permissions.md">Permissions</a>
    </category>
</seealso>