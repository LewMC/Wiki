# Commands

> See also: [Permissions](ES-Permissions.md)

## Main Command
This is the full list of commands included in the most recent version of Essence. Commands [can be disabled](ES-Disabling-Commands.md) by server administrators.

| Command           | Permission Required   | Description                                                 | Usage                 | Console can run? |
|-------------------|-----------------------|-------------------------------------------------------------|-----------------------|------------------|
| /essence /ess /es | None                  | About essence.                                              | /essence /ess /es     | Yes              |
| /es help          | None                  | Help with Essence.                                          | /es help              | Yes              |
| /es import        | essence.admin.import  | Imports data from other plugins.                            | /es import Essentials | Yes              |
| /es reload        | essence.admin.reload  | Reloads Essence's configuration.                            | /es reload            | Yes              |
| /es restore       | essence.admin.restore | Restores Essence's files (note: overwrites language files). | /es restore           | Yes              |

## Gamemode Commands
Wildcard permission: essence.gamemode.*

| Command                                                                     | Permission Required                                       | Description                             | Usage                                                     | Console can run? |
|-----------------------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------|-----------------------------------------------------------|------------------|
| /gm survival /gamemode survival /gms                                        | essence.gamemode.survival                                 | Change to survival mode                 | /gm survival /gamemode survival /gmc                      | No               |
| /gm survival &lt;player> /gamemode survival &lt;player> /gms &lt;player>    | essence.gamemode.survival **and** essence.gamemode.other  | Change another player to survival mode  | /gm survival Notch /gamemode survival Notch /gms Notch    | Yes              |
| /gm creative /gamemode creative /gmc                                        | essence.gamemode.creative                                 | Change to creative mode                 | /gm creative /gamemode creative /gmc                      | No               |
| /gm creative &lt;player> /gamemode creative &lt;player> /gmc &lt;player>    | essence.gamemode.creative **and** essence.gamemode.other  | Change another player to creative mode  | /gm creative Notch /gamemode creative Notch /gmc Notch    | Yes              |
| /gm adventure /gamemode adventure /gma                                      | essence.gamemode.adventure                                | Change to adventure mode                | /gm adventure /gamemode adventure /gma                    | No               |
| /gm adventure &lt;player> /gamemode adventure &lt;player> /gma &lt;player>  | essence.gamemode.adventure **and** essence.gamemode.other | Change another player to adventure mode | /gm adventure Notch /gamemode adventure Notch /gma Notch  | Yes              |
| /gm spectator /gamemode spectator /gmsp                                     | essence.gamemode.spectator                                | Change to spectator mode                | /gm spectator /gamemode spectator /gmsp                   | No               |
| /gm spectator &lt;player> /gamemode spectator &lt;player> /gmsp &lt;player> | essence.gamemode.spectator **and** essence.gamemode.other | Change another player to spectator mode | /gm spectator Notch /gamemode spectator Notch /gmsp Notch | Yes              |

## Inventory Commands
Wildcard permission: essence.inventory.*

| Command                   | Permission Required                                         | Description               | Usage                                | Console can run? |
|---------------------------|-------------------------------------------------------------|---------------------------|--------------------------------------|------------------|
| /anvil                    | essence.inventory.anvil                                     | Open an anvil.            | /anvil                               | No               |
| /cartography              | essence.inventory.cartography                               | Open a cartography table. | /cartography                         | No               |
| /craft /workbench         | essence.inventory.craft                                     | Open a crafting table.    | /craft /workbench                    | No               |
| /enderchest /echest       | essence.inventory.enderchest                                | Open an ender chest.      | /enderchest /echest                  | No               |
| /grindstone               | essence.inventory.grindstone                                | Open a grindstone.        | /grindstone                          | No               |
| /loom                     | essence.inventory.loom                                      | Open a loom.              | /loom                                | No               |
| /smithing                 | essence.inventory.smithing                                  | Open a smithing table.    | /smithing                            | No               |
| /stonecutter              | essence.inventory.stonecutter                               | Open a stonecutter.       | /stonecutter                         | No               |
| /trash /disposal /garbage | essence.inventory.trash                                     | Open the disposal menu.   | /trash /disposal /garbage            | No               |
| /give /item /i            | essence.inventory.give                                      | Open the disposal menu.   | See [/give command](ES-Inventory.md) | No               |
| /give /item /i            | essence.inventory.give.other **and** essence.inventory.give | Open the disposal menu.   | See [/give command](ES-Inventory.md) | No               |

## Kit Commands
Wildcard permission: essence.kits.*

| Command    | Permission Required                                                                         | Description | Usage | Console can run? |
|------------|---------------------------------------------------------------------------------------------|-------------|-------|------------------|
| /kit /kits | Per-kit permissions, or essence.kits.all, [see this page for more information](ES-Kits.md). | Get kits    | /kit  | No               |

## Teleportation Commands 

### General Teleportation
Wildcard permission: essence.teleport.*

> Folia-based Servers: /tpr requires version 1.8.1 or higher to work.

Since version 1.8.1 you can now use @p, @a, and @s in /teleport and /tp commands.

| Command                                                 | Permission Required                                    | Description                                                    | Usage               | Console can run? |
|---------------------------------------------------------|--------------------------------------------------------|----------------------------------------------------------------|---------------------|------------------|
| /teleport &lt;x> &lt;y> &lt;z> /tp &lt;x> &lt;y> &lt;z> | essence.teleport.coord                                 | Teleport to a coordinate location in the world (x,y,z).        | /tp 0 64 0          | No               |
| /tp &lt;user> &lt;x> &lt;y> &lt;z>                      | essence.teleport.coord **and** essence.teleport.other  | Teleport another player to set coordinates                     | /tp Notch 0 64 0    | Yes              |
| /teleport &lt;user> /tp &lt;user>                       | essence.teleport.player                                | Teleport to another player.                                    | /tp Notch           | No               |
| /teleport &lt;user> &lt;user> /tp &lt;user> &lt;user>   | essence.teleport.player **and** essence.teleport.other | Teleport a player to another player.                           | /tp LewIsLost Notch | No               |
| /tpa &lt;user>                                          | essence.teleport.request.send                          | Sends a teleportation request to a user.                       | /tpa Notch          | No               |
| /tpahere &lt;user>                                      | essence.teleport.request.here                          | Request a user to teleport to you.                             | /tpahere Notch      | No               |
| /tpaccept                                               | essence.teleport.request.accept                        | Accept a teleport request.                                     | /tpaccept           | No               |
| /tpdeny                                                 | essence.teleport.request.deny                          | Deny a teleport request.                                       | /tpdeny             | No               |
| /tpcancel                                               | essence.teleport.request.cancel                        | Cancel a teleport request that you've sent.                    | /tpcancel           | No               |
| /tptoggle                                               | essence.teleport.request.toggle                        | Toggle if players can send you teleportation requests.         | /tptoggle           | No               |
| /tpr /rtp /tprandom                                     | essence.teleport.random                                | Teleport to a random location in the world.                    | /tpr /rtp /tprandom | No               |
| /back                                                   | essence.teleport.back                                  | Go back to your last location before teleporting.              | /back               | No               |
| /top                                                    | essence.teleport.top                                   | Teleports you to the highest available block at your position. | /top                | Yes              |
| /top &lt;username>                                      | essence.teleport.top **and** essence.teleport.other    | Teleports you to the highest available block at your position. | /top                | Yes              |
| /bottom                                                 | essence.teleport.bottom                                | Teleports you to the lowest available block at your position.  | /bottom             | Yes              |
| /bottom &lt;username>                                   | essence.teleport.bottom **and** essence.teleport.other | Teleports you to the lowest available block at your position.  | /bottom             | Yes              |

### Warp Commands
Wildcard permission: essence.warp.*

You can limit the number of warps a user can create by using `essence.warp.limit.X` - [Learn more](ES-Permissions.md#warp-and-home-creation-limits).

| Command            | Permission Required | Description               | Usage            | Console can run? |
|--------------------|---------------------|---------------------------|------------------|------------------|
| /warps             | essence.warp.list   | Get a list of warps       | /warps           | Yes              |
| /warp &lt;name>    | essence.warp.use    | Teleport to a warp point. | /warp MyHouse    | No               |
| /setwarp &lt;name> | essence.warp.create | Create a warp point.      | /setwarp MyHouse | No               |
| /delwarp &lt;name> | essence.warp.delete | Delete a warp point.      | /delwarp MyHouse | No               |

### Home Commands
Wildcard permission: essence.home.*

You can limit the number of homes a user can create by using `essence.home.limit.X` or `essence.home.team.limit.X` - [Learn more](ES-Permissions.md#warp-and-home-creation-limits).

| Command             | Permission Required      | Description              | Usage            | Console can run? |
|---------------------|--------------------------|--------------------------|------------------|------------------|
| /homes              | essence.home.list        | Get a list of homes      | /homes           | No               |
| /home &lt;name>     | essence.home.use         | Teleport to a home.      | /home MyHouse    | No               |
| /sethome &lt;name>  | essence.home.create      | Create a home.           | /sethome MyHouse | No               |
| /delhome &lt;name>  | essence.home.delete      | Delete a home.           | /delhome MyHouse | No               |
| /thomes             | essence.home.team.list   | Get a list of team homes | /thomes          | No               |
| /thome &lt;name>    | essence.home.team.use    | Teleport to a team home. | /thome Base      | No               |
| /setthome &lt;name> | essence.home.team.create | Create a team home.      | /setthome Base   | No               |
| /delthome &lt;name> | essence.home.team.delete | Delete a team home.      | /delthome Base   | No               |

### Spawn commands
Wildcard permission: essence.spawn.*

| Command                             | Permission Required                                        | Description                                     | Usage                   | Console can run? |
|-------------------------------------|------------------------------------------------------------|-------------------------------------------------|-------------------------|------------------|
| /spawn /world                       | essence.spawn *All players have access to this by default* | Teleport to the current world's spawn           | /spawn                  | No               |
| /spawn &lt;world> /world &lt;world> | essence.spawn.other                                        | Teleport to another world's spawn               | /spawn world_the_nether | No               |
| /setspawn                           | essence.spawn.create                                       | Set the world's spawn to your current location. | /setspawn               | No               |

## Stats Commands
Wildcard permission: essence.stats.* and essence.stats.other.*

| Command           | Permission Required      | Description                  | Usage       | Console can run? |
|-------------------|--------------------------|------------------------------|-------------|------------------|
| /heal             | essence.stats.heal       | Heal yourself.               | /heal       | No               |
| /heal &lt;player> | essence.stats.heal.other | Heal another player.         | /heal Notch | Yes              |
| /feed             | essence.stats.feed       | Feed yourself.               | /feed       | No               |
| /feed &lt;player> | essence.stats.feed.other | Feed another player.         | /feed Notch | Yes              |
| /repair           | essence.stats.repair     | Repair the item in your hand | /repair     | No               |

## Chat Commands
Wildcard permission: essence.chat.*

| Command                             | Permission Required                                 | Description                                            | Usage                                    | Console can run? |
|-------------------------------------|-----------------------------------------------------|--------------------------------------------------------|------------------------------------------|------------------|
| /broadcast &lt;message>             | essence.chat.broadcast                              | Send a message to the entire server.                   | /broadcast This is an example broadcast. | Yes              |
| /msg &lt;name> &lt;message>         | essence.chat.msg                                    | Send a message to a specific user.                     | /msg Notch Hello there!                  | Yes              |
| /reply &lt;message> /r &lt;message> | essence.chat.reply                                  | Reply to the last user who sent you a private message. | /r Hey back to you!                      | Yes              |
| /nick &lt;name>                     | essence.chat.nick.self                              | Change your own username.                              | /nick Lew                                | No               |
| /nick &lt;username> &lt;name>       | essence.chat.nick.other and essence.chat.nick.other | Change yours or someone else's username.               | /nick LewIsFound Lew                     | Yes              |

## Economy Commands
Wildcard permission: essence.economy.*

> You must have [Vault](https://dev.bukkit.org/projects/vault) installed for these commands to function.

| Command                    | Permission Required     | Description         | Usage          | Console can run? |
|----------------------------|-------------------------|---------------------|----------------|------------------|
| /pay &lt;user> &lt;amount> | essence.economy.pay     | Pay another player. | /pay Notch 10  | Yes              |
| /balance /bal              | essence.economy.balance | View your balance.  | /balance / bal | Yes              |

## Team Commands
Wildcard permission: essence.team.*

> To use /team requests, accept, decline, kick, rule, and changeleader the player must have the permission to do so AND be the team leader.

| Command                                        | Permission Required        | Description                                     | Usage                               | Console can run? |
|------------------------------------------------|----------------------------|-------------------------------------------------|-------------------------------------|------------------|
| /team /group                                   | essence.team.list          | Get a list of teams.                            | /team /group                        | No               |
| /team &lt;name> /group &lt;name>               | essence.team.list          | Get information of a specific team.             | /team Red /group Red                | No               |
| /team create &lt;name> /group create &lt;name> | essence.team.create        | Create a team.                                  | /team create Red /group create Red  | No               |
| /team join &lt;name> /group join &lt;name>     | essence.team.join          | Join a team.                                    | /team join Red /group join Red      | No               |
| /team leave &lt;name> /group leave &lt;name>   | essence.team.join          | Leave a team.                                   | /team leave Red /group leave Red    | No               |
| /team requests                                 | essence.team.manage        | View pending membership requests for your team. | /team requests                      | No               |
| /team accept &lt;name>                         | essence.team.manage        | Accept a player's membership request.           | /team accept Notch                  | No               |
| /team decline &lt;name>                        | essence.team.manage        | Decline a player's membership request.          | /team decline Notch                 | No               |
| /team kick &lt;name>                           | essence.team.manage        | Kick (remove) a player from your team.          | /team kick Notch                    | No               |
| /team changeleader &lt;name>                   | essence.team.manage        | Transfer leadership to another member.          | /team changeleader Notch            | No               |
| /team disband                                  | essence.team.manage        | Disband your team (delete it).                  | /team disband                       | No               |
| /team rule &lt;rule>                           | essence.team.manage        | View the value of a team rule.                  | /team rule                          | No               |
| /team rule &lt;rule> &lt;value>                | essence.team.manage        | Set the value of a team rule.                   | /team rule allow-friendly-fire true | No               |
| Team home commands                             | See home commands section. |                                                 |                                     |                  |

## Administration Commands
Wildcard permission: essence.admin.*

| Command                          | Permission Required                                                     | Description                                     | Usage                     | Console can run? |
|----------------------------------|-------------------------------------------------------------------------|-------------------------------------------------|---------------------------|------------------|
| /seen &lt;name>                  | essence.admin.seen                                                      | Displays the player's last login date and time. | /seen Notch               | Yes              |
| /info &lt;name> /pinfo &lt;name> | essence.admin.info (plus essence.admin.info.viewip to see IP addresses) | Displays information about the player.          | /info Notch /pinfo Notch  | Yes              |
| /es reload                       | essence.admin.reload                                                    | Reloads Essence's configuration.                | /es reload                | Yes              |
| /invisible                       | essence.admin.invisible                                                 | Toggles if you're visible to other players.     | /invisible                | Yes              |
| /visible                         | essence.admin.invisible                                                 | Toggles if you're visible to other players.     | /visible                  | Yes              |
| /v                               | essence.admin.invisible                                                 | Toggles if you're visible to other players.     | /v                        | Yes              |
| /sudo &lt;username> &lt;command> | essence.admin.sudo                                                      | Runs a command as another player.               | /sudo Notch weather clear | Yes              |

## Environment Commands
Wildcard permission: essence.environment.*

> See [this page](ES-Time-and-Weather.md) for more information. Console usage for these commands may be different.

| Command                      | Permission Required              | Description                 | Usage           | Console can run? |
|------------------------------|----------------------------------|-----------------------------|-----------------|------------------|
| /time                        | essence.environment.time         | Checks the server time.     | /time           | Yes              |
| /time &lt;time>              | essence.environment.time.set     | Sets the server time.       | /time day       | Yes              |
| /weather                     | essence.environment.weather      | Checks the server weather.  | /weather        | Yes              |
| /weather &lt;weather>        | essence.environment.weather.set  | Sets the server weather.    | /weather clear  | Yes              |
| /ptime                       | essence.environment.ptime        | Checks your player time.    | /ptime          | No               |
| /ptime &lt;time/reset>       | essence.environment.ptime.set    | Sets your player time.      | /ptime day      | No               |
| /pweather                    | essence.environment.pweather     | Checks your player weather. | /pweather       | No               |
| /pweather &lt;weather/reset> | essence.environment.pweather.set | Sets your player weather.   | /pweather clear | No               |

## Miscellaneous Commands
Wildcard permission: None

| Command                    | Permission Required  | Description            | Usage  | Console can run? |
|----------------------------|----------------------|------------------------|--------|------------------|
| /rules                     | essence.rules        | View the server rules. | /rules | Yes              |

<seealso>
    <category ref="es-commands">
        <a href="ES-Teams.md">Teams</a>
        <a href="ES-Kits.md">Kits</a>
        <a href="ES-Permissions.md">Permissions</a>
        <a href="ES-Disabling-Commands.md">Disabling Commands</a>
    </category>
</seealso>
