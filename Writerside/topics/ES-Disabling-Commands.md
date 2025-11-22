# Disabling Features
<warning>
    <strong>This feature is not recommended in versions of Essence below 1.10.0 due to heavy limitations.</strong>
    Please consider alternatives such as permissions.
</warning>

Disabling features makes it appear as though the features (commands or modules) do not exist at all. If you'd like to
disallow some users to use the features, or have an error message display instead of nothing happening at all, you
should use [permissions](ES-Permissions.md).

## Disabling Commands
To disable commands in Essence, you can add them to a list in the configuration file.

1. Open Essence's config.yml
2. Scroll to disabled-commands.
3. Add any commands you'd like to disable. Most codes are what you'd expect, but since some commands have aliases we've included the full list below.
4. Restart your server.

## Command List
Most command codes are what you'd expect, but since we use aliases for our commands, some codes may be different that
what you're used to.

| Commands and Aliases (A-Z) | disabled-commands code |
|----------------------------|------------------------|
| /anvil                     | anvil                  |
| /back                      | back                   |
| /bal                       | balance                |
| /balance                   | balance                |
| /bottom                    | bottom                 |
| /broadcast                 | broadcast              |
| /canceltp                  | tpcancel               |
| /cartography               | cartography            |
| /ci                        | clear                  |
| /cclear                    | confirmclear           |
| /clear                     | clear                  |
| /clearinventory            | clear                  |
| /confirmclear              | confirmclear           |
| /craft                     | craft                  |
| /delghome                  | delthome               |
| /delgrouphome              | delthome               |
| /delhome                   | delhome                |
| /delthome                  | delthome               |
| /delteamhome               | delthome               |
| /delwarp                   | delwarp                |
| /direction                 | direction              |
| /disposal                  | trash                  |
| /echest                    | enderchest             |
| /eco                       | eco                    |
| /enchant                   | enchant                |
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
| /give                      | give                   |
| /gma                       | gma                    |
| /gmc                       | gmc                    |
| /gms                       | gms                    |
| /gmsp                      | gmsp                   |
| /grindstone                | grindstone             |
| /grouphome                 | thome                  |
| /grouphomes                | thomes                 |
| /head                      | skull                  |
| /heal                      | heal                   |
| /home                      | home                   |
| /homes                     | homes                  |
| /i                         | give                   |
| /info                      | info                   |
| /invisible                 | invisible              |
| /item                      | give                   |
| /kit                       | kit                    |
| /list                      | list                   |
| /loom                      | loom                   |
| /msg                       | msg                    |
| /message                   | msg                    |
| /online                    | list                   |
| /pay                       | pay                    |
| /pinfo                     | info                   |
| /pseen                     | seen                   |
| /pm                        | msg                    |
| /ptime                     | ptime                  |
| /pweather                  | pweather               |
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
| /skull                     | skull                  |
| /smithing                  | smithing               |
| /spawn                     | spawn                  |
| /stonecutter               | stonecutter            |
| /sudo                      | sudo                   |
| /thome                     | thome                  |
| /teamhome                  | thome                  |
| /thomes                    | thomes                 |
| /teamhomes                 | thomes                 |
| /team                      | team                   |
| /teleport                  | tp                     |
| /time                      | time                   |
| /top                       | top                    |
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
| /weather                   | spawn                  |
| /workbench                 | craft                  |
| /wcreate                   | wcreate                |
| /wdelete                   | wdelete                |
| /world                     | world                  |
| /wtp                       | spawn                  |

## Disabling Modules
> Requires Essence 1.10.0 or newer.

To disable a module, set `enabled` to `false` under that module's section in Essence's configuration file.

This will disable all commands and features that fall under this module.

The 'core' module cannot be disabled.

## Limitations and Drawbacks
In Essence 1.10.1 and above, both of the below issues were fixed and there are currently no known limitations or 
drawbacks.

### Essence 1.10.0 and below
Disabling a command or module because you prefer another plugin's (or vanilla's)
alternative did not work. Spigot required Essence to register commands in the plugin.yml file, because of this the 
server still expected the command to work. This was fixed in Essence 1.10.1, and command disabling will now allow other
plugins commands to work instead of Essence's.

### Essence 1.6.0 and below
Essence will refuse to process the command, causing the default error message to appear in chat.

Here's an example with the `/tp` command disabled:

![es-disabling-commands.png](es-disabling-commands.png)

<seealso>
    <category ref="es-commands">
        <a href="ES-Commands.md">Commands</a>
        <a href="ES-Permissions.md">Permissions</a>
    </category>
</seealso>
