# Commands

## Main Command
This is the full list of commands included in the most recent version of Essence. Commands [can be disabled](ES-Disabling-Commands.md) by server administrators.

| Command           | Permission Required | Description                                                        | Usage                          | Console can run? |
|-------------------|---------------------|--------------------------------------------------------------------|--------------------------------|------------------|
| /essence /ess /es | None                | About essence. Add help onto the end to view help (e.g. /es help). | /es /es help /es help teleport | Yes              |

## Gamemode Commands
Wildcard permission: essence.gamemode.*

| Command                                                            | Permission Required                                       | Description                             | Usage                                                     | Console can run? |
|--------------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------|-----------------------------------------------------------|------------------|
| /gm survival /gamemode survival /gms                               | essence.gamemode.survival                                 | Change to survival mode                 | /gm survival /gamemode survival /gmc                      | No               |
| /gm survival <player> /gamemode survival <player> /gms <player>    | essence.gamemode.survival **and** essence.gamemode.other  | Change another player to survival mode  | /gm survival Notch /gamemode survival Notch /gms Notch    | Yes              |
| /gm creative /gamemode creative /gmc                               | essence.gamemode.creative                                 | Change to creative mode                 | /gm creative /gamemode creative /gmc                      | No               |
| /gm creative <player> /gamemode creative <player> /gmc <player>    | essence.gamemode.creative **and** essence.gamemode.other  | Change another player to creative mode  | /gm creative Notch /gamemode creative Notch /gmc Notch    | Yes              |
| /gm adventure /gamemode adventure /gma                             | essence.gamemode.adventure                                | Change to adventure mode                | /gm adventure /gamemode adventure /gma                    | No               |
| /gm adventure <player> /gamemode adventure <player> /gma <player>  | essence.gamemode.adventure **and** essence.gamemode.other | Change another player to adventure mode | /gm adventure Notch /gamemode adventure Notch /gma Notch  | Yes              |
| /gm spectator /gamemode spectator /gmsp                            | essence.gamemode.spectator                                | Change to spectator mode                | /gm spectator /gamemode spectator /gmsp                   | No               |
| /gm spectator <player> /gamemode spectator <player> /gmsp <player> | essence.gamemode.spectator **and** essence.gamemode.other | Change another player to spectator mode | /gm spectator Notch /gamemode spectator Notch /gmsp Notch | Yes              |

## Inventory Commands
Wildcard permission: essence.inventory.*

| Command                   | Permission Required           | Description               | Usage                     | Console can run? |
|---------------------------|-------------------------------|---------------------------|---------------------------|------------------|
| /anvil                    | essence.inventory.anvil       | Open an anvil.            | /anvil                    | No               |
| /cartography              | essence.inventory.cartography | Open a cartography table. | /cartography              | No               |
| /craft /workbench         | essence.inventory.craft       | Open a crafting table.    | /craft /workbench         | No               |
| /enderchest /echest       | essence.inventory.enderchest  | Open an ender chest.      | /enderchest /echest       | No               |
| /grindstone               | essence.inventory.grindstone  | Open a grindstone.        | /grindstone               | No               |
| /loom                     | essence.inventory.loom        | Open a loom.              | /loom                     | No               |
| /smithing                 | essence.inventory.smithing    | Open a smithing table.    | /smithing                 | No               |
| /stonecutter              | essence.inventory.stonecutter | Open a stonecutter.       | /stonecutter              | No               |
| /trash /disposal /garbage | essence.inventory.trash       | Open the disposal menu.   | /trash /disposal /garbage | No               |

## Kit Commands
Wildcard permission: essence.kits.*

| Command    | Permission Required                                                                         | Description | Usage | Console can run? |
|------------|---------------------------------------------------------------------------------------------|-------------|-------|------------------|
| /kit /kits | Per-kit permissions, or essence.kits.all, [see this page for more information](ES-Kits.md). | Get kits    | /kit  | No               |

## Teleportation Commands 

### General Teleportation
Wildcard permission: essence.teleport.*

<warning>
    <strong>/tpr is unavailable on Folia-based servers.</strong> We're working on bringing this feature back. <a href="https://github.com/LewMC/Essence/issues/63">Learn more</a>.
</warning>

| Command                               | Permission Required                                   | Description                                             | Usage               | Console can run? |
|---------------------------------------|-------------------------------------------------------|---------------------------------------------------------|---------------------|------------------|
| /teleport <x> <y> <z> /tp <x> <y> <z> | essence.teleport.coord                                | Teleport to a coordinate location in the world (x,y,z). | /tp 0 64 0          | No               |
| /teleport <name> /tp <name>           | essence.teleport.player                               | Teleport to another player.                             | /tp Notch           | No               |
| /tp <user> <x> <y> <z>                | essence.teleport.coord **and** essence.teleport.other | Teleport another player to set coordinates              | /tp Notch 0 64 0    | Yes              |
| /tpa <user>                           | essence.teleport.request.send                         | Sends a teleportation request to a user.                | /tpa Notch          | No               |
| /tpahere <user>                       | essence.teleport.request.here                         | Request a user to teleport to you.                      | /tpahere Notch      | No               |
| /tpaccept                             | essence.teleport.request.accept                       | Accept a teleport request.                              | /tpaccept           | No               |
| /tpdeny                               | essence.teleport.request.deny                         | Deny a teleport request.                                | /tpdeny             | No               |
| /tpcancel                             | essence.teleport.request.cancel                       | Cancel a teleport request that you've sent.             | /tpcancel           | No               |
| /tptoggle                             | essence.teleport.request.toggle                       | Toggle if players can send you teleportation requests.  | /tptoggle           | No               |
| /tpr /rtp /tprandom                   | essence.teleport.random                               | Teleport to a random location in the world.             | /tpr /rtp /tprandom | No               |
| /back                                 | essence.teleport.back                                 | Go back to your last location before teleporting.       | /back               | No               |

### Warp Commands
Wildcard permission: essence.warp.*

You can limit the number of warps a user can create by using `essence.warp.limit.X` - [Learn more](ES-Permissions.md#warp-and-home-creation-limits).

| Command         | Permission Required | Description               | Usage            | Console can run? |
|-----------------|---------------------|---------------------------|------------------|------------------|
| /warp           | essence.warp.list   | Get a list of warps       | /warp            | No               |
| /warp <name>    | essence.warp.use    | Teleport to a warp point. | /warp MyHouse    | No               |
| /setwarp <name> | essence.warp.create | Create a warp point.      | /setwarp MyHouse | No               |
| /delwarp <name> | essence.warp.delete | Delete a warp point.      | /delwarp MyHouse | No               |

### Home Commands
Wildcard permission: essence.home.*

You can limit the number of homes a user can create by using `essence.home.limit.X` or `essence.home.team.limit.X` - [Learn more](ES-Permissions.md#warp-and-home-creation-limits).

| Command          | Permission Required      | Description              | Usage            | Console can run? |
|------------------|--------------------------|--------------------------|------------------|------------------|
| /homes           | essence.home.list        | Get a list of homes      | /homes           | No               |
| /home <name>     | essence.home.use         | Teleport to a home.      | /home MyHouse    | No               |
| /sethome <name>  | essence.home.create      | Create a home.           | /sethome MyHouse | No               |
| /delhome <name>  | essence.home.delete      | Delete a home.           | /delhome MyHouse | No               |
| /thomes          | essence.home.team.list   | Get a list of team homes | /thomes          | No               |
| /thome <name>    | essence.home.team.use    | Teleport to a team home. | /thome Base      | No               |
| /setthome <name> | essence.home.team.create | Create a team home.      | /setthome Base   | No               |
| /delthome <name> | essence.home.team.delete | Delete a team home.      | /delthome Base   | No               |

### Spawn commands
Wildcard permission: essence.spawn.*

| Command                       | Permission Required                                        | Description                                     | Usage                                   | Console can run? |
|-------------------------------|------------------------------------------------------------|-------------------------------------------------|-----------------------------------------|------------------|
| /spawn /world                 | essence.spawn *All players have access to this by default* | Teleport to the current world's spawn           | /spawn /world                           | No               |
| /spawn <world> /world <world> | essence.spawn.other                                        | Teleport to another world's spawn               | /spawn world_nether /world world_nether | No               |
| /setspawn                     | essence.spawn.create                                       | Set the world's spawn to your current location. | /setspawn                               |                  |

## Stats Commands
Wildcard permission: essence.stats.* and essence.stats.other.*

| Command        | Permission Required      | Description                  | Usage       | Console can run? |
|----------------|--------------------------|------------------------------|-------------|------------------|
| /heal          | essence.stats.heal       | Heal yourself.               | /heal       | No               |
| /heal <player> | essence.stats.heal.other | Heal another player.         | /heal Notch | Yes              |
| /feed          | essence.stats.feed       | Feed yourself.               | /feed       | No               |
| /feed <player> | essence.stats.feed.other | Feed another player.         | /feed Notch | Yes              |
| /repair        | essence.stats.repair     | Repair the item in your hand | /repair     | No               |

## Chat Commands
Wildcard permission: essence.chat.*

| Command              | Permission Required    | Description                          | Usage                                    | Console can run? |
|----------------------|------------------------|--------------------------------------|------------------------------------------|------------------|
| /broadcast <message> | essence.chat.broadcast | Send a message to the entire server. | /broadcast This is an example broadcast. | Yes              |

## Economy Commands
Wildcard permission: essence.economy.*

> You must have [Vault](https://dev.bukkit.org/projects/vault) installed for these commands to function.

| Command              | Permission Required     | Description         | Usage          | Console can run? |
|----------------------|-------------------------|---------------------|----------------|------------------|
| /pay <user> <amount> | essence.economy.pay     | Pay another player. | /pay Notch 10  | No               |
| /balance /bal        | essence.economy.balance | View your balance.  | /balance / bal | No               |

## Team Commands
Wildcard permission: essence.team.*

> To use /team requests, accept, decline, kick, rule, and changeleader the player must have the permission to do so AND be the team leader.

| Command                                  | Permission Required        | Description                                     | Usage                              | Console can run? |
|------------------------------------------|----------------------------|-------------------------------------------------|------------------------------------|------------------|
| /team /group                             | essence.team.list          | Get a list of teams.                            | /team /group                       | No               |
| /team <name> /group <name>               | essence.team.list          | Get information of a specific team.             | /team Red /group Red               | No               |
| /team create <name> /group create <name> | essence.team.create        | Create a team.                                  | /team create Red /group create Red | No               |
| /team join <name> /group join <name>     | essence.team.join          | Join a team.                                    | /team join Red /group join Red     | No               |
| /team leave <name> /group leave <name>   | essence.team.join          | Leave a team.                                   | /team leave Red /group leave Red   | No               |
| /team requests                           | essence.team.manage        | View pending membership requests for your team. | /team requests                     | No               |
| /team accept <name>                      | essence.team.manage        | Accept a player's membership request.           | /team accept Notch                 | No               |
| /team decline <name>                     | essence.team.manage        | Decline a player's membership request.          | /team decline Notch                | No               |
| /team kick <name>                        | essence.team.manage        | Kick (remove) a player from your team.          | /team kick Notch                   | No               |
| /team changeleader <name>                | essence.team.manage        | Transfer leadership to another member.          | /team changeleader Notch           | No               |
| /team disband                            | essence.team.manage        | Disband your team (delete it).                  | /team disband                      | No               |
| /team rule <rule>                        | essence.team.manage        | View the value of a team rule.                  | /team rule                         | No               |
| /team rule <rule> <value>                | essence.team.manage        | Set the value of a team rule.                   |                                    | No               |
| Team home commands                       | See home commands section. |                                                 |                                    |                  |

## Player Information Commands
Wildcard permission: essence.playerinfo.*

| Command      | Permission Required        | Description                                     | Usage       | Console can run? |
|--------------|----------------------------|-------------------------------------------------|-------------|------------------|
| /seen <name> | essence.playerinfo.seen    | Displays the player's last login date and time. | /seen Notch | Yes              |
| /info <name> | essence.playerinfo.info    | Displays information about the player.          | /info Notch | Yes              |

<seealso>
    <category ref="es-commands">
        <a href="ES-Teams.md">Teams</a>
        <a href="ES-Kits.md">Kits</a>
        <a href="ES-Permissions.md">Permissions</a>
        <a href="ES-Disabling-Commands.md">Disabling Commands</a>
    </category>
</seealso>