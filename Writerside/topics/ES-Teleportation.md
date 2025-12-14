# Teleportation
<warning>
Users will need to have the <a href="ES-Commands.md">correct permissions</a> to be able to access these features.
</warning>

There are a number of different types of teleportation in Essence.
These include a vanilla-like teleport system and a teleport request system.

## Standard Teleportation
> Since 1.10.0 players with the `essence.teleport.offline` permission can now teleport to offline players. This is included in the wildcard.

Essence's teleportation system works very similar to the vanilla system with a few tweaks.

With this command, you can replace &lt;user> with either a player's username or a query selector. These are @a, @s, and @p.
@a targets all players, @p targets the nearest player to you, and @s targets the entity executing the command (that's you!)

Giving a player the `essence.teleport.*` permission gives them access to every command listed below and every command in the teleport requests section.

| Command                                                 | Permission Required                                      | Description                                             |
|---------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------|
| /teleport &lt;x> &lt;y> &lt;z> /tp &lt;x> &lt;y> &lt;z> | essence.teleport.coord                                   | Teleport to a coordinate location in the world (x,y,z). |
| /tp &lt;user> &lt;x> &lt;y> &lt;z>                      | essence.teleport.coord **and** essence.teleport.other    | Teleport another player to set coordinates              |
| /teleport &lt;user> /tp &lt;user>                       | essence.teleport.player                                  | Teleport to another player.                             |
| /teleport &lt;user> /tp &lt;user> (User is offline)     | essence.teleport.player **and** essence.teleport.offline | Teleport to an offline player.                          |
| /teleport &lt;user> &lt;user> /tp &lt;user> &lt;user>   | essence.teleport.player **and** essence.teleport.other   | Teleport a player to another player.                    |

If you're new to server administration and are not sure who to give these permissions to, we recommend giving them to administrators.

This type of teleportation can be toggled per-player (not default). If a player has teleportation toggled off, other players cannot send them requests unless they have permissions to override it. For more information, see the "Toggling Teleportation" section below.

## Teleport Requests

Teleport requests are a system of teleportation that allows users to ask other users if they'd like to be teleported.
For example: User 1 requests to teleport to User 2, if User 2 accepts the request the teleport completes. Otherwise, a message is sent to User 1 informing them it was declined.

Giving a player the `essence.teleport.request.*` permission gives them access to every command listed below.

| Command            | Permission Required             | Description                                 |
|--------------------|---------------------------------|---------------------------------------------|
| /tpa &lt;user>     | essence.teleport.request.send   | Sends a teleportation request to a user.    |
| /tpahere &lt;user> | essence.teleport.request.here   | Request a user to teleport to you.          |
| /tpaccept          | essence.teleport.request.accept | Accept a teleport request.                  |
| /tpdeny            | essence.teleport.request.deny   | Deny a teleport request.                    |
| /tpcancel          | essence.teleport.request.cancel | Cancel a teleport request that you've sent. |

If you're new to server administration and are not sure who to give these permissions to, we recommend giving them to players and administrators.

This type of teleportation can be toggled per-player by default. If a player has teleportation toggled off, other players cannot send them requests unless they have permissions to override it. For more information, see the "Toggling Teleportation" section below.

## Toggling Teleportation
Players can toggle if they'd like to receive teleportation requests by using `/tptoggle`.
Players must have the `essence.teleport.request.toggle` permission to be able to do this.

Players will teleportation disabled cannot be sent teleportation requests.

By default, teleportation toggling only applies to teleport requests. We recommend this setup for most servers.

If the `teleportation.extended-toggle` value is enabled in the configuration, this also applies to the standard /tp command as well.
Players with the `essence.essence.bypass.extendedteleporttoggle` can bypass this for the /tp command, but not the /tprequest command.

## Random Teleportation
/tpr allows players to teleport randomly anywhere within the world border. It requires the `essence.teleport.random` permission.

This command can not teleport other players.

## Going back
Essence will remember a player's location before they teleported, if a player has the `essence.teleport.back` permission they can use the /back command to return there at any time.

When a player dies, this will be overwritten by their death location.

## Homes
Homes serve as personal warps for players or teams.
Only the player (or players in the team if it's a team home) can see and teleport to the homes.

Giving a player the `essence.home.*` permission gives them access to every command listed below.

| Command             | Permission Required      | Description              |
|---------------------|--------------------------|--------------------------|
| /homes              | essence.home.list        | Get a list of homes      |
| /home &lt;name>     | essence.home.use         | Teleport to a home.      |
| /sethome &lt;name>  | essence.home.create      | Create a home.           |
| /delhome &lt;name>  | essence.home.delete      | Delete a home.           |
| /thomes             | essence.home.team.list   | Get a list of team homes |
| /thome &lt;name>    | essence.home.team.use    | Teleport to a team home. |
| /setthome &lt;name> | essence.home.team.create | Create a team home.      |
| /delthome &lt;name> | essence.home.team.delete | Delete a team home.      |


## Warps
Warps are public teleportation locations. Warps are not per-player or private, if you'd like this you may prefer the home command.

Giving a player the `essence.warp.*` permission gives them access to every command listed below.

| Command            | Permission Required | Description               |
|--------------------|---------------------|---------------------------|
| /warp              | essence.warp.list   | Get a list of warps       |
| /warp &lt;name>    | essence.warp.use    | Teleport to a warp point. |
| /setwarp &lt;name> | essence.warp.create | Create a warp point.      |
| /delwarp &lt;name> | essence.warp.delete | Delete a warp point.      |

You can delete warps you've made with `essence.warp.delete`, to delete warps created by other players you will also need
`essence.warp.delete.other`


## Spawns
Spawns are the start place of your world. When players join, this is where they'll be placed. When they die without a bed, this is where they'll go.

Giving a player the `essence.spawn.*` permission gives them access to every command listed below.

| Command                             | Permission Required                                        | Description                                     |
|-------------------------------------|------------------------------------------------------------|-------------------------------------------------|
| /spawn /world                       | essence.spawn *All players have access to this by default* | Teleport to the current world's spawn           |
| /spawn &lt;world> /world &lt;world> | essence.spawn.other                                        | Teleport to another world's spawn               |
| /setspawn                           | essence.spawn.create                                       | Set the world's spawn to your current location. |

To make players always join the server at your main world's spawn, set `main-world-spawn` in the [configuration](ES-Configuration.md) to the name of your main world
and set `always-spawn` to `true`.

## Cooldowns and Delays
Teleporting has its setbacks, you've gotta wait!

Cooldowns are the time between teleporting that players must wait before they can teleport again.

For example: Player A goes to /home base and teleports there, then /home mine 2 seconds later, but they're told to wait 8 seconds before they can go.

Delays are the time players must wait after sending the command before they're actually teleported.
This gives players a chance to cancel the teleportation before it occurs.

For example: Player A goes to /home base but has to wait 3 seconds, they move their player to cancel the teleportation within that time and do not go.

You can change these values in the [configuration](ES-Configuration.md). To disable these features set the time to 0.