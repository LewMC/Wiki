# Changelogs

<warning>
<strong>You should always run the latest version of all software!</strong> That includes Essence! Updating keeps your server free from bugs, exploits, and other potential issues. When you see the message - update!
</warning>

## 1.6.0
_2024-07-XX_ - Essence 1.6.0 adds a whole host of new features including Vault integration.

| Added   | Essence can now be used as an economy provider for other plugins when [Vault](https://www.spigotmc.org/resources/vault.34315/) is installed. - Added /seen and /info commands. |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                            |
| Changed | Nothing was changed in this update.                                                                                                                                            |
| Fixed   | essence.* wildcard was not working correctly.                                                                                                                                  |

## 1.5.3
_2024-06-25_ - Essence 1.5.3 changes how the /home command is handled, and provides additional quality-of-life fixes and improvements.

| Added   | You can now limit the number of homes and warps a player can create by using permissions. [Learn more](ES-Permissions.md#warp-and-home-creation-limits).                                                                                              |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                   |
| Changed | /home will now list homes if there is no home named "home", instead of telling you it's missing.                                                                                                                                                      |
| Fixed   | /homes, /warps, and /thomes will now tell you if there's no homes set instead of displaying a blank list when homes/warps have been created in the past. - Fixes a bug where players would be occasionally teleported into the ground when they died. |

## 1.5.2
_2024-06-20_ - Essence 1.5.2 fixes exceptions in the /team command, teleportation not working as expected, and more.

| Added   | Nothing was added in this update.                                                                                                                                                                             |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                           |
| Changed | Teleportation can now handle more types of teleportation.                                                                                                                                                     |
| Fixed   | Exception when /team is ran by the console is now handled correctly. - Teleporting a player to a coordinate will now teleport that player instead of you. - Debug code left in accidentally has been removed. |

## 1.5.1
_2024-06-18_ - Essence 1.5.1 fixes players not respawning correctly and the /world command failing on non-vanilla generated worlds.

| Added   | Nothing was added in this update.                                                                                                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                              |
| Changed | Added better protections for detecting non-vanilla generated worlds or non-standard worlds.                                                                                                                                                                                                                      |
| Fixed   | [Issue #66](https://github.com/lewmc/essence/issues/65) - Players not respawning in beds with "close a file before one had been opened" error. - [Issue #64](https://github.com/lewmc/essence/issues/64) - Fixed bug where using the /world command on a non-vanilla world would cause IllegalArgumentException. |

## 1.5.0
_2024-06-18_ - Essence 1.5.0 adds team homes and tpr support.

| Added   | Re-added random teleportation - Added [team homes](ES-Teams.md)           |
|---------|---------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                       |
| Changed | Nothing was changed in this update.                                       |
| Fixed   | Fixed an issue where sometimes team files would not be created correctly. |

## 1.4.0
_2024-06-07_ - Essence 1.4.0 adds spawn, repair, kit, and teleportation request commands alongside support for Folia-based servers.

| Added   | Support for Folia-based servers - /spawn and /setspawn commands/repair command/kit command - /tpa, /tpaccept, /tpdeny, /tpcancel, /tptoggle commands for requesting teleportation |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Temporarily removed the random teleport command /tpr                                                                                                                              |
| Changed | Essence now requires Minecraft 1.20.4 or higher                                                                                                                                   |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                       |

## 1.3.2
_2024-02-03_ - This version is a hotfix for Essence 1.3.

| Added   | /garbage is now an alias for /trash - Essence will now check if it's running Bukkit, Spigot, or Paper and tell the console if it's not on Paper that some commands may not work.                                                                      |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                   |
| Changed | The plugin no longer disables itself when Essentials is installed, but instead warns the server console of the potential issues.                                                                                                                      |
| Fixed   | [Issue #33](https://github.com/lewmc/essence/issues/33) - Cooldown starts despite a failed /rtp request. - [Issue #37](https://github.com/lewmc/essence/issues/37) - Error occurs when a player hits another player (both were not on the same team). |

## 1.3.1
_2024-01-31_ - This version is a hotfix for Essence 1.3.

| Added   | Nothing was added in this update.                                                                                                                                                                                                                  |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                |
| Changed | Nothing was changed in this update.                                                                                                                                                                                                                |
| Fixed   | [Issue #28](https://github.com/lewmc/essence/issues/28) - TeleportUtil cooldown does not take into account the date. - [Issue #27](https://github.com/lewmc/essence/issues/27) - Apply cooldown after the teleporation countdown begins for /home. |

## 1.3.0
_2024-01-30_ - This version adds teleportation cooldowns, overhauls gamemode commands, and adds teams.

| Added   | /team command along with essence.team permissions. (See [Commands](ES-Commands.md)) - 1.19 support - More customizability of messages sent to player. See [this page for more information.](ES-Language-Files.md) - Option to [disable commands](ES-Disabling-Commands.md). Option for teleportation cooldowns. See [Essence Configuration](ES-Configuration.md). |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                               |
| Changed | Essence now requires Java 11. - General backend optimisations.                                                                                                                                                                                                                                                                                                    |
| Fixed   | [Issue #22](https://github.com/lewmc/essence/issues/22) - Player data can sometimes generate as a plugin config. - [Issue #18](https://github.com/lewmc/essence/issues/18) - Some auto-completion errors on /home.                                                                                                                                                |

## 1.2.0
_2024-01-26_ - This version adds random teleportation (/tpr command), fixes /back to work on death, full customisability of messages sent to players, and 1.19 support.

| Added   | /tprandom command along with essence.teleport.random permission. - 1.19 support. - Customisability of messages sent to player. See [this page for more information.](ES-Language-Files.md) |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Dropped 1.18 support.                                                                                                                                                                      |
| Changed | config.yml now has a language option for deciding which file to get messages from.                                                                                                         |
| Fixed   | /gm and /gamemode now work correctly                                                                                                                                                       |

## 1.1.0
_2024-01-19_ - This version adds economy commands and teleportation commands, as well as improving existing ones. Also includes bugfixes and quality-of-life improvements.

| Added   | Tab suggestions for /warp and /home. - /broadcast command along with essence.chat.* and essence.chat.broadcast permissions. - /back command along with essence.teleport.back permission.- /pay /bal commands along with essence.economy.*, essence.economy.pay, and essence.economy.bal permissions. - bStats - Update Checker - 1.18 and 1.19 support                                                                                                   |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Changed | /es, gamemode, and stats commands can now be ran from the console - /home and /sethome now have default values and will work without having to input a name. - Users will now be told if they don't have permissions even if a command is malformed.                                                                                                                                                                                                     |
| Fixed   | [Issue #6](https://github.com/lewmc/essence/issues/6) - Changing gamemode without permission causes error. - [Issue #4]((https://github.com/lewmc/essence/issues/4) - Running economy commands causes prefix to reset. - [Issue #3](https://github.com/lewmc/essence/issues/3) - Overwriting of homes and warps is possible. - [Issue #2](https://github.com/lewmc/essence/issues/2) - Deleting a home that doesn't exist shows success message in chat. |

## 1.0.0
_2024-01-17_ - The first version of Essence.

<warning>
This version contains a large number of known bugs which were fixed in later updates. We do not recommend running this version in a production environment.
</warning>

| Added   | Added commands essence, gamemode, gms, gmc, gma, gmsp, anvil, cartography, craft, enderchest, grindstone, loom, smithing, stonecutter, trash, tp, warp, setwarp, delwarp, home, sethome, delhome, heal, feed. |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                           |
| Changed | Nothing was changed in this update.                                                                                                                                                                           |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                                                   |
