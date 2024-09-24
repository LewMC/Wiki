# Changelogs

<warning>
<strong>You should always run the latest version of all software!</strong> That includes Kryptonite! Updating keeps your server free from bugs, exploits, and other potential issues. When you see the message - update!
</warning>

## 1.4.0
_2024-09-24_ - This version adds a GUI to KOS to allow administrators to select the profile that should be used in-game without having to access any configuration files. We've also added a new mob farm friendly profile.

| Added   | Administrators can now select a KOS profile without having to access any configuration files if they run the command in-game, new FarmFriendly [profile](KR-Profiles.md) to prevent breaking mob farms. |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                     |
| Changed | Updated bstats to version 3.1.0 for better Folia compatibility.                                                                                                                                         |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                                             |

## 1.3.0
_2024-06-06_ - This version adds support for Folia, adds KOS profiles, and warns server administrator is it detects plugins that may cause additional lag.

| Added   | [KOS Profiles](KR-Profiles.md) - Folia support - Warning messages if plugins that may cause additional lag are found. |
|---------|-----------------------------------------------------------------------------------------------------------------------|
| Removed | kos.yml file - use profiles instead.                                                                                  |
| Changed | Nothing was changed in this update.                                                                                   |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                           |

## 1.2.0
_2024-05-26_ - This version overhauls the Kryptonite Optimisation System and adds optimisations for Paper, Purpur, and Pufferfish.

| Added   | New kos.yml file that gives more fine-grain customisation of optimisations applied by KOS - 8 additional patches for Purpur servers - 8 additional patches for Pufferfish servers - 1 additional patch for Paper servers - Override pre-generated world protections is now possible in config.yml |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                                                                               |
| Changed | Moved some messages to server console to tidy up chat for in-game playersImproved error handling                                                                                                                                                                                                  |
| Fixed   | Fixed Spigot server detection.                                                                                                                                                                                                                                                                    |

## 1.1.2
_2024-05-25_ - Small patch that fixes compatability issues with Purpur servers.

| Added   | Nothing was added in this update                         |
|---------|----------------------------------------------------------|
| Removed | Nothing was removed in this update.                      |
| Changed | Nothing was changed in this update.                      |
| Fixed   | Error caused by unshaded dependencies on Purpur servers. |

## 1.1.1
_2024-05-22_ - This update patches some bugs found in 1.1.0.

| Added   | Nothing was added in this update                                                                                                                                             |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                          |
| Changed | Replaced automated checking with prompts due to file access issues.                                                                                                          |
| Fixed   | Fixed file not found error when Kryptonite attempted to read its configuration - Fixed update file missing error when Kryptonite attempted to update its configuration files |

## 1.1.0
_2024-05-21_ - This update added the [Exploit Database (EDB)](KR-Exploit-Database.md) to Kryptonite, alongside additions and changes to the [Kryptonite Optimisation System (KOS)](KR-Kryptonite-Optimisation-System.md).

| Added   | EDB Exploits: EDB-1 to EDB-10 (A and B) - sync-chunk-writes option added to KOS     |
|---------|-------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                 |
| Changed | The Kryptonite Optimisation System is now accessed through /kos instead of /kr run. |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                         |

## 1.0.0
_2024-05-18_ - Initial release of Kryptonite

| Added   | Support for Software: CraftBukkit, Spigot, Paper, Purpur (partial - runs as Paper), Pufferfish (partial - runs as Paper) - Support for Configs: server.properties, bukkit.yml, spigot.yml, paper-world-defaults.yml, paper-global.yml |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Removed | Nothing was removed in this update.                                                                                                                                                                                                   |
| Changed | Nothing was changed in this update.                                                                                                                                                                                                   |
| Fixed   | Nothing was fixed in this update, maybe nothing was broken?                                                                                                                                                                           |
