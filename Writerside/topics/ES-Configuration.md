# Configuration

## Configuration Values
| Key                                    | Description                                                                                                                                                                                                                                                                       | Accepted Values                                | Default Value                                                        |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|----------------------------------------------------------------------|
| update-check                           | This value defines if Essence should check for updates during startup. If this is enabled, the plugin will query [LewMC Services](LewMC-Services.md) to check for updates. The doesn't collect any data about you or your server.                                                 | true or false                                  | true                                                                 |
| console-prefix                         | This sets the prefix that console logs appear as, just for a bit of customisation! To change the in-game chat prefix please see Essence [Language Files](ES-Language-Files.md).                                                                                                   | Anything                                       | Essence                                                              |
| motd.enabled                           | This toggle decides if Essence should display the join message to players in chat when they log in. [More information](ES-MOTD.md).                                                                                                                                               | true or false                                  | true                                                                 |
| motd.message                           | A message displayed to players in chat when they log in. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                             | Multi-line string.                             | See example below.                                                   |
| chat.enabled                           | Should Essence process chat messages?                                                                                                                                                                                                                                             | true or false                                  | true                                                                 |
| chat.name-format                       | The format that chat messages should appear in. [Supports Placeholders](ES-Placeholders.md)                                                                                                                                                                                       | String.                                        | "%essence_combined_prefix% %essence_player%%essence_player_suffix%:" |
| chat.allow-message-formatting          | Should Essence process formatting codes (& codes) in chat messages?                                                                                                                                                                                                               | true or false                                  | false                                                                |
| broadcasts.first-join                  | The message broadcast in chat when a player joins for the first time. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                | String.                                        | "§a{{player}} joined the server for the first time!"                 |
| broadcasts.join                        | The message broadcast in chat when a player joins. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                                   | String.                                        | "§e{{player}} joined the server!"                                    |
| broadcasts.leave                       | The message broadcast in chat when a player leaves. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                                  | String.                                        | "§c{{player}} left the server!"                                      |
| spawn-kits                             | A list of kits the player should be given when they first join the server. Set to false to disable. Players must have the required permissions to access the kits. [Learn more about kits](ES-Kits.md).                                                                           | Any list of valid kits.                        | See example below.                                                   |
| economy.start-money                    | This is the amount of money players get when they first join the server. It should be a decimal number (e.g. 100.0, 40.99, 0.0)                                                                                                                                                   | Any decimal number                             | 100.0                                                                |
| economy.symbol                         | This value will be displayed in front of any monetary values shown in chat. Whilst we recommend sticking with standard symbols you can put anything here, such as "Coins" or whatever really.                                                                                     | Anything                                       | $                                                                    |
| teleportation.home.wait                | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                        | 3                                                                    |
| teleportation.home.cooldown            | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                        | 10                                                                   |
| teleportation.warp.wait                | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                        | 3                                                                    |
| teleportation.warp.cooldown            | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                        | 10                                                                   |
| teleportation.randomtp.cooldown        | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                        | 10                                                                   |
| teleportation.spawn.wait               | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                        | 3                                                                    |
| teleportation.spawn.cooldown           | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                        | 10                                                                   |
| teleportaion.spawn.main-spawn-world    | Sets the world that should be used as the main spawn. Players first joining the server will be placed on this world's spawnpoint. This can cause issues if you're using non-vanilla loaded world - [learn more](ES-Troubleshooting.md).                                           | Any valid world name.                          | world                                                                |
| teleportation.spawn.always-spawn       | Should players be sent to the main world's spawnpoint every time they join the server?                                                                                                                                                                                            | true or false                                  | false                                                                |
| teleportation.requests.cooldown        | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                        | 10                                                                   |
| teleportation.requests.default-enabled | Should teleportation requests be enabled by default for all users. This can be changed per-user using /tptoggle (permissions required).	                                                                                                                                          | true or false                                  | true                                                                 |
| teleportation.extended-toggle          | Should teleportation toggling also apply to the standard /teleport /tp commands? Not recommended.	                                                                                                                                                                                | true or false                                  | false                                                                |
| teleportation.move-to-cancel           | Should player movement cancel teleportation? 	                                                                                                                                                                                                                                    | true or false                                  | true                                                                 |
| language                               | This sets the language file that Essence will use for chat messages. Console log messages are not affected by this and are hard-coded. For more information please see [Language Files](ES-Language-Files.md).                                                                    | Any valid language code with an existing file. | en-gb                                                                |
| disabled-commands                      | This disables processing of certain commands in Essence, to add commands to the list you should create a new line and follow the format of the example. Please note: this does have limitations - for more information please see [Disabling Commands](ES-Disabling-Commands.md). | List of commands to disable (or blank).        | See example below.                                                   |
| disabled-commands-feedback             | If a user runs a disabled command, should they be told it's disabled? If set to false, nothing happens.                                                                                                                                                                           | true or false                                  | true                                                                 |
| playerdata.store-ip-address            | Decides if Essence should store player IP addresses in data files.                                                                                                                                                                                                                | true or false                                  | true                                                                 |
| verbose                                | Outputs additional information to the console, including file information. You should only enable this if you're having problems. Warning: Creates a LOT of console spam.                                                                                                         | true or false                                  | false                                                                |
| config-version                         | Please don't change this! It can mess with Essence's configuration updater, and if we change anything you'll be in for a whole load of red text in your server console.                                                                                                           | 1                                              | 1                                                                    |

## Example config.yml

```
# Generated by Essence 1.10.0-SNAPSHOT
# Need help? Visit wiki.lewmc.net
# Found a bug or want to request a feature? Open an issue at github.com/lewmc/essence

# UPDATE CHECKING - Should Essence query the server to check for updates?
update-check: true

# PREFIXES
console-prefix: Essence

# MOTD - This is displayed to users in chat when they join the server.
# You can use § colour codes here!
motd:
  enabled: true
  message: |-
    §2§lWelcome to the server!
    §aYou can change this message in Essence's config.yml

# BROADCASTS - These are some predefined broadcasts that fire at specific times.
broadcasts:
  first-join: §a%essence_player% joined the server for the first time!
  join: §e%essence_player% joined the server!
  leave: §c%essence_player% left the server!

# CHAT - You can use § colour codes here!
chat:
  enabled: true
  name-format: '%essence_combined_prefix% %essence_player%%essence_player_suffix%:'
  allow-message-formatting: false

# SPAWN KITS - Players are given these kits when they first join the server.
# Set to "false" to disable this feature.
spawn-kits:
- wooden-tools

# ECONOMY
economy:
  start-money: 100.0
  symbol: $

# TELEPORTATION
teleportation:
  home:
    wait: 3
    cooldown: 10
  warp:
    wait: 3
    cooldown: 10
  randomtp:
    cooldown: 60
  spawn:
    wait: 3
    cooldown: 10
    main-spawn-world: world
    always-spawn: false
  requests:
    cooldown: 10
    default-enabled: true
  extended-toggle: false
  move-to-cancel: true

# LANGUAGE - The file that will be used to display messages.
# Please ensure the file exists in the 'language' sub-folder before changing this value.
language: en-GB

# DISABLED COMMANDS - See https://wiki.lewmc.net/es-disabling-commands.html for help.
# PLEASE NOTE: This does not currently remove the command from /es help
disabled-commands:
- example

# Should disabled commands tell users they're disabled when they're executed?
disabled-commands-feedback: true

# PLAYERDATA - What types of player data to store
# This does not change what is already stored
playerdata:
  store-ip-address: true

# VERBOSE - Outputs more information to the console. If you're having issues, enable this. Creates a lot of console spam.
verbose: false

# Do not change this!
config-version: 2

```