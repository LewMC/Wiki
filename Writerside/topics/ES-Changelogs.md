# Changelogs

<warning>
    <strong>You should always run the latest version of all software!</strong> 
    That includes Essence! Updating keeps your server free from bugs, exploits, and other potential issues. When you see the message – update!
</warning>

## 1.12.0

_2026-01-XX_ – Essence 1.12.1 fixes a bug with the auto complete causing console spam for world/spawn teleportation.

**As of 1.12.0, Essence no longer supports CraftBukkit
or Spigot servers.**

| Added   | You can now add enchantments and multiple of the same item to kits. You can now set walking and flying speeds independently of one-another [more info](ES-Stats.md).                                                                                      |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                       |
| Changed | Essence no longer supports CraftBukkit or Spigot. [More information](ES-System-Requirements.md). The kits file now works differently, it will be migrated automatically. See [](ES-Kits.md) for more information.                                         |
| Fixed   | [#349](https://github.com/LewMC/Essence/issues/349) Pre 1.11.0 player data is not being migrated properly/at all, [#350](https://github.com/LewMC/Essence/issues/350) IP is not stored in Essence player data despite Advanced Player Data being enabled, |

## 1.11.1

_2025-12-15_ – Essence 1.11.1 fixes a bug with the auto complete causing console spam for world/spawn teleportation.

| Added   | Nothing was added in this update.                                                             |
|---------|-----------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                           |
| Changed | Nothing was changed in this update.                                                           |
| Fixed   | [#343](https://github.com/LewMC/Essence/issues/343) Tab Complete on /spawn generates an error |

## 1.11.0

_2025-12-14_ – Essence 1.11.0 adds over 15 new commands and changes how player data is handled for a faster, smoother experience on larger servers.
Huge thanks to KadTheHunter on GitHub for their extensive contributions to this update!

| Added   | /eco, /top, /bottom, /ascend, /descend, /direction, /burn, /extinguish, /god, /skull, /give, /sudo, /near, /invsee, /ignore, /list, /clear, /confirmclear, and /recipe commands. Adds alias /eat to /feed. Add [world management module](ES-Worlds.md), accessed using /world.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Changed | The way Essence configures forced spawning has changed, you may need to reconfigure this feature if you use it. Essence should now be more stable and reliable with concurrent user interactions (Folia), /tp now supports relative coordinates (for example ~5), /delwarp now has an other permission to delete other player's created warps, /feed now fills saturation and exhaustion as well as food and no longer requires a username input. The `disabled-commands.list` config value was moved to `disabled-commands`, your server will update the config automatically on startup. Spawns moved into `worlds.yml`, your server will automatically move them on startup. If `always-spawn` is enabled, `/spawn` will now follow it. |
| Fixed   | [#286](https://github.com/LewMC/Essence/issues/286) /time set appears incorrectly, [#288](https://github.com/LewMC/Essence/issues/288) /back not covering deaths, [#300](https://github.com/LewMC/Essence/issues/300) players are not always added to teams they create, [#312](https://github.com/LewMC/Essence/issues/312) MOTD can no longer be disabled, [#324](https://github.com/LewMC/Essence/issues/324) Disabling the economy module does not disable the vault connector, [#331](https://github.com/LewMC/Essence/issues/331) Respawning at bed location even if bed was destroyed.                                                                                                                                              |

## 1.10.2
_2025-08-29_ – Essence 1.10.2 fixes a config-breaking bug from the previous version.

| Added   | Nothing was added in this update.                                                                                                                                                          |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                        |
| Changed | Nothing was changed in this update.                                                                                                                                                        |
| Fixed   | [#257](https://github.com/LewMC/Essence/issues/257) Essence 1.10.1-SNAPSHOT encounters an error when generating a fresh config (not fixed for servers where the config does not yet exist) |

## 1.10.1
_2025-08-29_ – Essence 1.10.1 improves data importing & command disabling, and fixes a number of bugs.

_This version has been recalled due to a breaking bug or other serious issue. Please update to the next available version. We apologise for any inconvenience caused.
If your server was affected and you need assistance, please contact us at lewmc.net/help_

| Added   | Nothing was added in this update.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | `disabled-commands` no longer provide feedback, and the config option was therefore removed. If you require command feedback, use permissions instead.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Changed | Importing data from Essentials should now be more robust and more likely to be successful. We've moved our commands to Foundry's new runtimeCommand feature, which means that disabling commands (or modules) will now *fully* disable them, no feedback at all, it's like they never even existed! Config value economy.mode can no longer be 'OFF', set economy.enabled to false instead (does the same thing). We've also moved to a new configuration system, so /es reload should be much more reliable now. Disabling `manage-chat` will disable nicknames and /nick, allowing other nicknames plugins to take over. |
| Fixed   | [#243](https://github.com/LewMC/Essence/issues/243) home limits were [#254](https://github.com/LewMC/Essence/issues/254) configuration values for manage-chat were ignored. [#256](https://github.com/LewMC/Essence/issues/256) /pinfo does not read player data correctly/at all [#257](https://github.com/LewMC/Essence/issues/257) Essence 1.10.1-SNAPSHOT encounters an error when generating a fresh config                                                                                                                                                                                                           |


## 1.10.0
_2025-08-04_ – Essence 1.10.0 adds new environment commands, modules, player stat modifiers, and contains a number of bug fixes and tweaks.

| Added   | Added new /es restore command that restores Essence's files. User IP addresses now appear in /info (requires extra permission node and can be toggled in config). Added support for [placeholders](ES-Placeholders.md) in language files. Added new [Environment module](ES-Time-and-Weather.md) which adds time, weather, ptime, and pweather commands. You can now [teleport to offline players](ES-Teleportation.md). Added /fly and /speed to the [stats module](ES-Stats.md). Added modules which can be [disabled](ES-Disabling-Commands.md). |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Unused commons-io dependency (replaced with Foundry), reducing jarfile size by over 300kB. Unused "console-prefix" config value.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Changed | The "Move to cancel teleport" system can now be toggled in the config. Essence now uses Foundry under the hood to manage many common features it shares with our other plugins. If you experience any issues please let us know.                                                                                                                                                                                                                                                                                                                    |
| Fixed   | [Issue #220 Console spam when players join](https://github.com/LewMC/Essence/issues/220) - [Issue #224 /back location is updated even if teleportation is cancelled.](https://github.com/LewMC/Essence/issues/224)                                                                                                                                                                                                                                                                                                                                  |

## 1.9.0
_2025-05-18_ – Essence 1.9.0 adds extended teleport toggling, PlaceholderAPI support, and a whole host of new features for chat.

| Added   | [Extended teleport toggles](https://github.com/LewMC/Essence/issues/145), PlaceholderAPI support alongside [new placeholders and new places where they can be used](ES-Placeholders.md), Teams prefix and chat formatting, and display name (nickname) changing.                                                                                                                                                                                       |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Changed | Team names must now be shorter than 12 characters (only applies to new teams). Placeholders have replaced Message Tags and their values have changed in this update, your old tags will continue to work until Essence 1.10, so please [updating them to the new values](ES-Placeholders.md). Essence will automatically update your join/leave messages and MOTD. Updates config-version to 2, heavily advise against downgrading below this version. |
| Fixed   | /back command is now working correctly.                                                                                                                                                                                                                                                                                                                                                                                                                |

## 1.8.1
_2025-05-17_ – Essence 1.8.1 re-adds support for /tpr on Folia and adds the use of @ selectors in /tp commands – huge thanks to @x1aoren!

_This version has a known issue with the /back command due to a rewrite of the teleportation system. A fix was released in v1.9.0_

| Added   | @ selectors in /tp commands.                                                   |
|---------|--------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                            |
| Changed | Nothing was changed in this update.                                            |
| Fixed   | /tpr now works correctly on Folia-based servers.                               |

## 1.8.0
_2025-05-16_ – Essence 1.8.0 adds new permissions and restrictions, new language options, and commands to make you go invisible!

_This version has a known issue with the /back command due to a rewrite of the teleportation system. A fix was released in v1.9.0_

| Added   | Spanish (full) and Korean (partial) translations, the ability to bypass teleportation cooldowns and delays, the ability to restrict how many times players can claim kits, commands to toggle invisibility!                                      |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                              |
| Changed | Updated FoliaLib to version 0.4.3 - Updated jetbrains:annotations to version 25.0.0 - Updated maven-javadoc-plugin to version 3.10.0 - When importing from Essentials, more information is given as to why a specific operation may have failed. |
| Fixed   | The /r command no longer ignores the first word after it - When importing data from Essentials, the horribly long error message when there are no spawns has been fixed.                                                                         |

## 1.7.2
_2024-09-23_ – Essence 1.7.2 updates libraries used by Essence to add greater compatability with Folia.

| Added   | Nothing was added in this update.                                              |
|---------|--------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                            |
| Changed | Updated bstats-bukkit to version 3.1.0 - Updated commons-io to version 2.17.0. |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                    |

## 1.7.1
_2024-08-06_ – Essence 1.7.1 is a hotfix for v1.7.0, fixing issues when players respawn if they've set a respawn location bed.

| Added   | Nothing was added in this update.                                                                                                                                                                                    |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                  |
| Changed | Nothing was changed in this update.                                                                                                                                                                                  |
| Fixed   | [Issue #145](https://github.com/LewMC/Essence/issues/145) - Fixes an exception when players would teleport to their set respawn bed location using /spawn, /world, or by respawning after death or dimension change. |

## 1.7.0
_2024-07-22_ – Essence 1.7.0 adds some quality-of-life features, changes how teleportation and command disabling work, and allows importing of data from other plugins.

| Added   | Custom player joining and leaving messages - The ~ operator is now supported on /tp commands. - Importing homes, warps, and spawns from EssentialsX.                                                                                                                                                                                                                      |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                                       |
| Changed | Changed to new functions internally that should speed up processing of chat messages. - Command disabling will now remove the command from /es help and will no longer send the default error message if `verbose` is set to `false` in config.yml. [Learn more](ES-Disabling-Commands.md) - Permissions can now fallback to Bukkit if Essence couldn't determine access. |
| Fixed   | Fixing not having permissions causing default error message to appear. - Added missing /kit and team home commands to /es help.                                                                                                                                                                                                                                           |

## 1.6.0
_2024-07-01_ – Essence 1.6.0 adds a whole host of new features including Private Messaging, new Language support, and Vault integration.

| Added   | Essence can now be used as an economy provider for other plugins when [Vault](https://www.spigotmc.org/resources/vault.34315/) is installed. - Added /es reload, /msg, /reply, /rules, /seen, and /info commands. - Added Simplified Chinese (zh-CN) translation, very limited French (fr-FR) translation. |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                        |
| Changed | /broadcast now appears in /es help.                                                                                                                                                                                                                                                                        |
| Fixed   | essence.* wildcard was not working correctly. - Fixed some aliases being incorrect.                                                                                                                                                                                                                        |

## 1.5.3
_2024-06-25_ – Essence 1.5.3 changes how the /home command is handled and provides additional quality-of-life fixes and improvements.

| Added   | You can now limit the number of homes and warps a player can create by using permissions. [Learn more](ES-Permissions.md#warp-and-home-creation-limits).                                                                                              |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                   |
| Changed | /home will now list homes if there is no home named "home", instead of telling you it's missing.                                                                                                                                                      |
| Fixed   | /homes, /warps, and /thomes will now tell you if there's no homes set instead of displaying a blank list when homes/warps have been created in the past. - Fixes a bug where players would be occasionally teleported into the ground when they died. |

## 1.5.2
_2024-06-20_ – Essence 1.5.2 fixes exceptions in the /team command, teleportation not working as expected, and more.

| Added   | Nothing was added in this update.                                                                                                                                                                             |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                           |
| Changed | Teleportation can now handle more types of teleportation.                                                                                                                                                     |
| Fixed   | Exception when /team is ran by the console is now handled correctly. - Teleporting a player to a coordinate will now teleport that player instead of you. - Debug code left in accidentally has been removed. |

## 1.5.1
_2024-06-18_ – Essence 1.5.1 fixes players not respawning correctly and the /world command failing on non-vanilla generated worlds.

| Added   | Nothing was added in this update.                                                                                                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                              |
| Changed | Added better protections for detecting non-vanilla generated worlds or non-standard worlds.                                                                                                                                                                                                                      |
| Fixed   | [Issue #66](https://github.com/lewmc/essence/issues/65) - Players not respawning in beds with "close a file before one had been opened" error. - [Issue #64](https://github.com/lewmc/essence/issues/64) - Fixed bug where using the /world command on a non-vanilla world would cause IllegalArgumentException. |

## 1.5.0
_2024-06-18_ – Essence 1.5.0 adds team homes and tpr support.

| Added   | Re-added random teleportation - Added [team homes](ES-Teams.md)           |
|---------|---------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                       |
| Changed | Nothing was changed in this update.                                       |
| Fixed   | Fixed an issue where sometimes team files would not be created correctly. |

## 1.4.0
_2024-06-07_ – Essence 1.4.0 adds spawn, repair, kit, and teleportation request commands alongside support for Folia-based servers.

| Added   | Support for Folia-based servers - /spawn and /setspawn commands/repair command/kit command - /tpa, /tpaccept, /tpdeny, /tpcancel, /tptoggle commands for requesting teleportation |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Temporarily removed the random teleport command /tpr                                                                                                                              |
| Changed | Essence now requires Minecraft 1.20.4 or higher                                                                                                                                   |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                       |

## 1.3.2
_2024-02-03_ – This version is a hotfix for Essence 1.3.

| Added   | /garbage is now an alias for /trash - Essence will now check if it's running Bukkit, Spigot, or Paper and tell the console if it's not on Paper that some commands may not work.                                                                      |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                   |
| Changed | The plugin no longer disables itself when Essentials is installed, but instead warns the server console of the potential issues.                                                                                                                      |
| Fixed   | [Issue #33](https://github.com/lewmc/essence/issues/33) - Cooldown starts despite a failed /rtp request. - [Issue #37](https://github.com/lewmc/essence/issues/37) - Error occurs when a player hits another player (both were not on the same team). |

## 1.3.1
_2024-01-31_ – This version is a hotfix for Essence 1.3.

| Added   | Nothing was added in this update.                                                                                                                                                                                                                  |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                |
| Changed | Nothing was changed in this update.                                                                                                                                                                                                                |
| Fixed   | [Issue #28](https://github.com/lewmc/essence/issues/28) - TeleportUtil cooldown does not take into account the date. - [Issue #27](https://github.com/lewmc/essence/issues/27) - Apply cooldown after the teleporation countdown begins for /home. |

## 1.3.0
_2024-01-30_ – This version adds teleportation cooldowns, overhauls gamemode commands, and adds teams.

| Added   | /team command along with essence.team permissions. (See [](ES-Commands.md)) - 1.19 support - More customizability of messages sent to player. See [this page for more information.](ES-Language-Files.md) - Option to [disable commands](ES-Disabling-Commands.md). Option for teleportation cooldowns. See [Essence Configuration](ES-Configuration.md). |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                       |
| Changed | Essence now requires Java 11. - General backend optimisations.                                                                                                                                                                                                                                                                                            |
| Fixed   | [Issue #22](https://github.com/lewmc/essence/issues/22) - Player data can sometimes generate as a plugin config. - [Issue #18](https://github.com/lewmc/essence/issues/18) - Some auto-completion errors on /home.                                                                                                                                        |

## 1.2.0
_2024-01-26_ – This version adds random teleportation (/tpr command), fixes /back to work on death, full customisability of messages sent to players, and 1.19 support.

| Added   | /tprandom command along with essence.teleport.random permission. - 1.19 support. - Customisability of messages sent to player. See [this page for more information.](ES-Language-Files.md) |
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Dropped 1.18 support.                                                                                                                                                                      |
| Changed | config.yml now has a language option for deciding which file to get messages from.                                                                                                         |
| Fixed   | /gm and /gamemode now work correctly                                                                                                                                                       |

## 1.1.0
_2024-01-19_ – This version adds economic commands and teleportation commands, as well as improving existing ones. Also includes bugfixes and quality-of-life improvements.

| Added   | Tab suggestions for /warp and /home. - /broadcast command along with essence.chat.* and essence.chat.broadcast permissions. - /back command along with essence.teleport.back permission.- /pay /bal commands along with essence.economy.*, essence.economy.pay, and essence.economy.bal permissions. - bStats - Update Checker - 1.18 and 1.19 support                                                                                                   |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Changed | /es, gamemode, and stats commands can now be ran from the console - /home and /sethome now have default values and will work without having to input a name. - Users will now be told if they don't have permissions even if a command is malformed.                                                                                                                                                                                                     |
| Fixed   | [Issue #6](https://github.com/lewmc/essence/issues/6) - Changing gamemode without permission causes error. - [Issue #4]((https://github.com/lewmc/essence/issues/4) - Running economy commands causes prefix to reset. - [Issue #3](https://github.com/lewmc/essence/issues/3) - Overwriting of homes and warps is possible. - [Issue #2](https://github.com/lewmc/essence/issues/2) - Deleting a home that doesn't exist shows success message in chat. |

## 1.0.0
_2024-01-17_ – The first version of Essence.

<warning>
This version contains a large number of known bugs which were fixed in later updates. We do not recommend running this version in a production environment.
</warning>

| Added   | Added commands essence, gamemode, gms, gmc, gma, gmsp, anvil, cartography, craft, enderchest, grindstone, loom, smithing, stonecutter, trash, tp, warp, setwarp, delwarp, home, sethome, delhome, heal, feed. |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                           |
| Changed | Nothing was changed in this update.                                                                                                                                                                           |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                                                   |
