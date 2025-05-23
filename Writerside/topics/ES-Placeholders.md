# Placeholders

<warning>
    <strong>As of version 1.9.0, placeholders replaced Message Tags.</strong>
</warning>

Placeholders are used to replace text with pre-generated values set by Essence.
You can use these tags to set values that may change often such as versions.

You can use Essence placeholders with or without PlaceholderAPI installed.

## Placeholder list
| Placeholder                            | Description                                                  | Example               |
|----------------------------------------|--------------------------------------------------------------|-----------------------|
| `%essence_version%`                    | Gets the version of Essence the server is running.           | `1.9.0`               |
| `%essence_minecraft_version%`          | Gets the version of Minecraft the server is running.         | `1.21.5`              |
| `%essence_time%`                       | Gets the current time in format HH:MM:SS                     | `12:50:19`            |
| `%essence_date%`                       | Gets the current date in format YYYY-MM-DD                   | `2025-05-18`          |
| `%essence_datetime%`                   | Gets the current date and time in format YYYY-MM-DD HH:MM:SS | `2025-05-18 12:50:19` |
| `%essence_player%`                     | The player who initiated the message's displayname           | `Lew`                 |
| `%essence_username%`                   | The player who initiated the message's username              | `LewIsLost`           |
| `%essence_team%` `%essence_team_name%` | The player's team's name.                                    | `BlueTeam`            |
| `%essence_team_leader%`                | The player's team's name.                                    | `LewIsLost`           |
| `%essence_team_prefix%`                | The player's team's prefix.                                  | `[BlueTeam]`          |
| `%essence_combined_prefix%`            | The player's combined prefix.^1                              | `[Admin][BlueTeam]`   |
| `%essence_player_prefix%`              | The player's prefix.^2                                       | `[Admin]`             |
| `%essence_player_suffix%`              | The player's suffix.                                         | `the awesome`         |
| `%essence_balance%`                    | The player's balance.                                        | `$50`                 |

^1 This feature will work but may be limited without Vault and a permissions plugin (we recommend LuckPerms).

^2 Requires Vault and a permissions plugin (we recommend LuckPerms).

## Where can I use placeholders?
You don't need to install PlaceholderAPI to use placeholders, but if you do have it you can also use any other placeholders supported by that plugin in these places too.

Without PlaceholderAPI installed, these placeholders work in:
- Standard chat messages (if [Essence Chat](ES-Chat.md) has not been disabled)
- config.yml
  - chat.name-format
  - motd.message
  - broadcasts.first-join
  - broadcasts.join
  - broadcasts.leave
- rules.txt
- Some of Essence's commands
  - /broadcast
  - /msg
  - /r

With PlaceholderAPI installed, these placeholders work in all the above areas plus anywhere else with PlaceholderAPI support.

## Language Files
Language files use a different system for Placeholders, they appear as `{{1}}`, `{{2}}`, etc.
These values are set by the function in Essence that causes that message to be sent.

You should <u>not</u> change these values.

Language files do not parse placeholders.
