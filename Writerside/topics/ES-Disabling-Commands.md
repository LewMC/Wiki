# Disabling Commands
<warning>
<strong>This feature is not recommended in versions of Essence below 1.6.1 due to console spam.</strong> Please consider alternatives such as permissions.
</warning>

To disable commands in Essence, you can add them to a list in the configuration file.

1. Open Essence's config.yml
2. Scroll to disabled-commands.
3. Add any commands you'd like to disable. Most codes are what you'd expect, but since some commands have aliases we've included the full list below.
4. Restart your server or run `/es reload`.

Commands will not execute or appear in /es help, but may still appear in /help, /?, and autocomplete menus.

## Command Feedback
By default, when a user executes a disabled command they will receive a message informing them that a command is disabled.

If you'd like nothing to happen, no message or feedback, you should set `disabled-commands-feedback` to `false` in config.yml

If you'd like the default error message to appear instead, you can enable `verbose` in `config.yml`, but this may create additional console spam due to extensive logging whist this mode is enabled.

## Command List
Most command codes are what you'd expect, but since we use aliases for our commands, some codes may be different that what you're used to.

| Commands and Aliases (A-Z) | disabled-commands code |
|----------------------------|------------------------|
| /anvil                     | anvil                  |
| /back                      | back                   |
| /bal                       | balance                |
| /balance                   | balance                |
| /broadcast                 | broadcast              |
| /canceltp                  | tpcancel               |
| /cartography               | cartography            |
| /craft                     | craft                  |
| /delghome                  | delthome               |
| /delgrouphome              | delthome               |
| /delhome                   | delhome                |
| /delthome                  | delthome               |
| /delteamhome               | delthome               |
| /delwarp                   | delwarp                |
| /disposal                  | trash                  |
| /echest                    | enderchest             |
| /enderchest                | enderchest             |
| /es                        | essence                |
| /ess                       | essence                |
| /essence                   | essence                |
| /feed                      | feed                   |
| /fix                       | repair                 |
| /gamemode                  | gamemode               |
| /garbage                   | trash                  |
| /ghome                     | thome                  |
| /ghomes                    | thomes                 |
| /gma                       | gma                    |
| /gmc                       | gmc                    |
| /gms                       | gms                    |
| /gmsp                      | gmsp                   |
| /grindstone                | grindstone             |
| /grouphome                 | thome                  |
| /grouphomes                | thomes                 |
| /heal                      | heal                   |
| /home                      | home                   |
| /homes                     | homes                  |
| /info                      | info                   |
| /invisible                 | invisible              |
| /kit                       | kit                    |
| /loom                      | loom                   |
| /msg                       | msg                    |
| /message                   | msg                    |
| /pay                       | pay                    |
| /pinfo                     | info                   |
| /pseen                     | seen                   |
| /pm                        | msg                    |
| /r                         | reply                  |
| /repair                    | repair                 |
| /reply                     | reply                  |
| /rtp                       | tprandom               |
| /rules                     | rules                  |
| /seen                      | seen                   |
| /setghome                  | setthome               |
| /setgrouphome              | setthome               |
| /sethome                   | sethome                |
| /setspawn                  | setspawn               |
| /setthome                  | setthome               |
| /setteamhome               | setthome               |
| /setwarp                   | setwarp                |
| /smithing                  | smithing               |
| /spawn                     | spawn                  |
| /stonecutter               | stonecutter            |
| /thome                     | thome                  |
| /teamhome                  | thome                  |
| /thomes                    | thomes                 |
| /teamhomes                 | thomes                 |
| /team                      | team                   |
| /teleport                  | tp                     |
| /tp                        | tp                     |
| /tpa                       | tpa                    |
| /tpaccept                  | tpaccept               |
| /tpahere                   | tpahere                |
| /tpcancel                  | tpcancel               |
| /tpdeny                    | tpdeny                 |
| /tpdecline                 | tpdeny                 |
| /tpr                       | tprandom               |
| /tprandom                  | tprandom               |
| /tprequest                 | tpa                    |
| /tptoggle                  | tptoggle               |
| /toggletp                  | tptoggle               |
| /trash                     | trash                  |
| /v                         | invisible              |
| /visible                   | invisible              |
| /warp                      | warp                   |
| /warps                     | warps                  |
| /workbench                 | craft                  |
| /world                     | spawn                  |

## Limitations and Drawbacks
If you're looking to disable a command because you prefer another plugin's (or vanilla's) alternative, this system likely won't work for you.
Spigot requires Essence to register commands in the plugin.yml file, because of this the server still expects the command to work.

In **Essence 1.6.0 and below**, Essence will refuse to process the command, causing the default error message to appear in chat.
Here's an example with the `/tp` command disabled:

![es-disabling-commands.png](es-disabling-commands.png)

In **Essence 1.6.1 and above**, this will only happen if `verbose` is set to `true` in Essence's config.yml, otherwise by default the user will receive an error message. [Learn more](#command-feedback).

If you want to use a vanilla command, you can append minecraft: to it. For example: /minecraft:teleport

## Alternatives
Permissions! Essence has a robust permissions system - simply disallow players from using the commands. This gives them an error message instead of it appearing as though the command doesn't work at all.

<seealso>
    <category ref="es-commands">
        <a href="ES-Commands.md">Commands</a>
        <a href="ES-Permissions.md">Permissions</a>
    </category>
</seealso>
