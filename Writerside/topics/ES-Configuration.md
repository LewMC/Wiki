# Configuration
> This Wiki page is for the configuration in version 1.11.0 or later (Config V4). Earlier versions may have a different layout.

## Configuration Values
| Key                                      | Description                                                                                                                                                                                                                                                                       | Accepted Values                                                                                                                                                                                 | Default Value                                                        |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| admin.enabled                            | Enables the admin module.                                                                                                                                                                                                                                                         | true or false                                                                                                                                                                                   | true                                                                 |
| chat.enabled                             | Enables the chat module.                                                                                                                                                                                                                                                          | true or false                                                                                                                                                                                   | true                                                                 |
| chat.manage-chat                         | Can Essence manage the server's chat? When set to `false`, /nick is disabled.                                                                                                                                                                                                     | true or false                                                                                                                                                                                   | true                                                                 |
| chat.name-format                         | The format that chat messages should appear in. [Supports Placeholders](ES-Placeholders.md)                                                                                                                                                                                       | String.                                                                                                                                                                                         | "%essence_combined_prefix% %essence_player%%essence_player_suffix%:" |
| chat.allow-message-formatting            | Should Essence process formatting codes (& codes) in chat messages?                                                                                                                                                                                                               | true or false                                                                                                                                                                                   | false                                                                |
| chat.broadcasts.first-join               | The message broadcast in chat when a player joins for the first time. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                | String.                                                                                                                                                                                         | "§a{{player}} joined the server for the first time!"                 |
| chat.broadcasts.join                     | The message broadcast in chat when a player joins. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                                   | String.                                                                                                                                                                                         | "§e{{player}} joined the server!"                                    |
| chat.broadcasts.leave                    | The message broadcast in chat when a player leaves. [Supports Placeholders](ES-Placeholders.md).                                                                                                                                                                                  | String.                                                                                                                                                                                         | "§c{{player}} left the server!"                                      |
| chat.motd                                | A message displayed to players in chat when they log in. [Supports Placeholders](ES-Placeholders.md). Set to 'false' to disable.                                                                                                                                                  | Multi-line string.                                                                                                                                                                              | See example below.                                                   |
| economy.enabled                          | Enables the economy module.                                                                                                                                                                                                                                                       | true or false                                                                                                                                                                                   | true                                                                 |
| economy.mode                             | This is the mode that Essence will run its economy in. Most players should not change this. This config value is useful if you'd like to use another economy provider or to disable Essence's economy altogether. See [the economy page](ES-Economy.md) for more information.     | **'VAULT'** default mode - sets up Essence as the server's economy provider.<br><br>**'ESSENCE'** Tells Essence to keep its economy to itself.<br><br>To disable economy use `economy.enabled`. | 'VAULT'                                                              |
| economy.start-money                      | This is the amount of money players get when they first join the server. It should be a decimal number (e.g. 100.0, 40.99, 0.0)                                                                                                                                                   | Any decimal number                                                                                                                                                                              | 100.0                                                                |
| economy.symbol                           | This value will be displayed in front of any monetary values shown in chat. Whilst we recommend sticking with standard symbols you can put anything here, such as "Coins" or whatever really.                                                                                     | Anything                                                                                                                                                                                        | $                                                                    |
| environment.enabled                      | Enables the environment module.                                                                                                                                                                                                                                                   | true or false                                                                                                                                                                                   | true                                                                 |
| gamemode.enabled                         | Enables the gamemode module.                                                                                                                                                                                                                                                      | true or false                                                                                                                                                                                   | true                                                                 |
| inventory.enabled                        | Enables the inventory module.                                                                                                                                                                                                                                                     | true or false                                                                                                                                                                                   | true                                                                 |
| kit.enabled                              | Enables the kit module.                                                                                                                                                                                                                                                           | true or false                                                                                                                                                                                   | true                                                                 |
| kit.spawn-kits                           | A list of kits the player should be given when they first join the server. Set to false to disable. Players must have the required permissions to access the kits. [Learn more about kits](ES-Kits.md).                                                                           | Any list of valid kits.                                                                                                                                                                         | See example below.                                                   |
| stats.enabled                            | Enables the stats module.                                                                                                                                                                                                                                                         | true or false                                                                                                                                                                                   | true                                                                 |
| team.enabled                             | Enables the team module.                                                                                                                                                                                                                                                          | true or false                                                                                                                                                                                   | true                                                                 |
| teleportation.enabled                    | Enables the teleportation module.                                                                                                                                                                                                                                                 | true or false                                                                                                                                                                                   | true                                                                 |
| teleportation.back.wait                  | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.top.wait                   | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.bottom.wait                | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.home.wait                  | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.home.cooldown              | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                                                                                                                                                                         | 10                                                                   |
| teleportation.warp.wait                  | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.warp.cooldown              | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                                                                                                                                                                         | 10                                                                   |
| teleportation.randomtp.cooldown          | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                                                                                                                                                                         | 10                                                                   |
| teleportation.spawn.wait                 | The amount of time (in seconds) the player should have to wait for after sending the command before they're teleported. To disable this feature set this value to 0.	                                                                                                             | Integer                                                                                                                                                                                         | 3                                                                    |
| teleportation.spawn.cooldown             | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                                                                                                                                                                         | 10                                                                   |
| teleportation.spawn.global-spawn.enabled | Should the spawn be global? (e.g. a single spawn for all worlds within a single world). See [Global Spawn / Lobby World](ES-Teleportation.md#spawns).                                                                                                                             | Any valid world name.                                                                                                                                                                           | world                                                                |
| teleportation.spawn.global-spawn.world   | Sets the world that should be used as the global spawn. This can cause issues if you're using non-loaded world - [learn more](ES-Troubleshooting.md).                                                                                                                             | Any valid world name.                                                                                                                                                                           | world                                                                |
| teleportation.spawn.force-spawn.on-join  | Should players be sent to the main world's spawnpoint every time they join the server?                                                                                                                                                                                            | true or false                                                                                                                                                                                   | false                                                                |
| teleportation.spawn.force-spawn.on-death | Should players be sent to the main world's spawnpoint every time they die?                                                                                                                                                                                                        | true or false                                                                                                                                                                                   | false                                                                |
| teleportation.requests.cooldown          | The amount of time (in seconds) the player should have to wait for to teleport since they last teleported. To disable this feature set this value to 0.	                                                                                                                          | Integer                                                                                                                                                                                         | 10                                                                   |
| teleportation.requests.default-enabled   | Should teleportation requests be enabled by default for all users. This can be changed per-user using /tptoggle (permissions required).	                                                                                                                                          | true or false                                                                                                                                                                                   | true                                                                 |
| teleportation.extended-toggle            | Should teleportation toggling also apply to the standard /teleport /tp commands? Not recommended.	                                                                                                                                                                                | true or false                                                                                                                                                                                   | false                                                                |
| teleportation.move-to-cancel             | Should player movement cancel teleportation? 	                                                                                                                                                                                                                                    | true or false                                                                                                                                                                                   | true                                                                 |
| language                                 | This sets the language file that Essence will use for chat messages. Console log messages are not affected by this and are hard-coded. For more information please see [Language Files](ES-Language-Files.md).                                                                    | Any valid language code with an existing file.                                                                                                                                                  | en-gb                                                                |
| disabled-commands                        | This disables processing of certain commands in Essence, to add commands to the list you should create a new line and follow the format of the example. Please note: this does have limitations - for more information please see [Disabling Commands](ES-Disabling-Commands.md). | List of commands to disable (or blank).                                                                                                                                                         | See example below.                                                   |
| item-blacklist                           | This disables processing of certain items in Essence, to add items to the list you should create a new line and follow the format of the example.                                                                                                                                 | List of items to blacklist (or blank).                                                                                                                                                          | See example below.                                                   |
| advanced.playerdata.store-ip-address     | Decides if Essence should store player IP addresses in data files.                                                                                                                                                                                                                | true or false                                                                                                                                                                                   | true                                                                 |
| advanced.update-check                    | This value defines if Essence should check for updates during startup. If this is enabled, the plugin will query [LewMC Services](LewMC-Services.md) to check for updates. The doesn't collect any data about you or your server.                                                 | true or false                                                                                                                                                                                   | true                                                                 |
| advanced.verbose                         | Outputs additional information to the console, including file information. You should only enable this if you're having problems. Warning: Creates a LOT of console spam.                                                                                                         | true or false                                                                                                                                                                                   | false                                                                |
| config-version                           | Please don't change this! It can mess with Essence's configuration updater, and if we change anything you'll be in for a whole load of red text in your server console.                                                                                                           | Do not change this value, it can mess up the config in later versions!                                                                                                                          | 3                                                                    |

If your configuration values are set to invalid values, Essence will reset them to their default and inform you in the console's logs.

## Example config.yml

```
# Generated by Essence 1.11.0
# Need help? Visit wiki.lewmc.net
# Found a bug or want to request a feature? Open an issue at github.com/lewmc/essence

# ADMIN MODULE
admin:
  enabled: true

# CHAT MODULE
chat:
  enabled: true
  name-format: "%essence_combined_prefix% %essence_player%%essence_player_suffix%:"
  allow-message-formatting: false
  broadcasts:
    first-join: "§a%essence_player% joined the server for the first time!"
    join: "§e%essence_player% joined the server!"
    leave: "§c%essence_player% left the server!"
  motd: |-
    §2§lWelcome to the server!
    §aYou can change this message in Essence's config.yml
  manage-chat: true

# ECONOMY MODULE
economy:
  enabled: true
  mode: VAULT
  start-money: 100.0
  symbol: $

# ENVIRONMENT MODULE
environment:
  enabled: true

# GAMEMODE MODULE
gamemode:
  enabled: true

# INVENTORY MODULE
inventory:
  enabled: true

# KIT MODULE
kit:
  enabled: true
  spawn-kits:
    - wooden-tools

# STATS MODULE
stats:
  enabled: true

# TEAM MODULE
team:
  enabled: true

# TELEPORTATION MODULE
teleportation:
  enabled: true
  back:
    wait: 3
  top:
    wait: 3
  bottom:
    wait: 3
  ascend:
    wait: 3
  descend:
    wait: 3
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
    global-spawn:
      enabled: false
      world: world
    force-spawn:
      on-join: false
      on-death: false
  near:
    default-radius: 200
    max-radius: 50000
  requests:
    cooldown: 10
    default-enabled: true
  extended-toggle: false
  move-to-cancel: true

world:
  enabled: true

# LANGUAGE - The file that will be used to display messages.
# Please ensure the file exists in the 'language' sub-folder before changing this value.
language: en-GB

# DISABLED COMMANDS
# Allows you to disable specific commands.
disabled-commands:
  - example

# ITEM BLACKLIST
# Items that cannot be /given
item-blacklist:
  - example

# ADVANCED SETTINGS
# These settings should usually be left alone. Only change them if you know what you're doing.
advanced:
  playerdata:
    store-ip-address: true
  update-check: true
  verbose: false

# Do not change this!
config-version: 4
