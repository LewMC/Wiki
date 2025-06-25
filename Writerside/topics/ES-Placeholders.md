# Placeholders

<warning>
    <strong>As of version 1.9.0, placeholders replaced Message Tags.</strong>
</warning>

Placeholders are used to replace text with pre-generated values set by Essence. You can use these placeholders to set
values that may change often such as versions. Placeholders are handled by Essence and do not require any other plugins
to work within Essence. However, if you'd like to use other plugin's placeholders in Essence, or Essence's in them -
you'll need to install PlaceholderAPI.

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
Placeholders work in:
- Chat messages (if [Essence Chat](ES-Chat.md) has not been disabled and Vault is installed)
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
- Language files (since 1.10.0)

### PlaceholderAPI
> PlaceholderAPI is an optional feature. Our placeholders will still work in our systems without it.

PlaceholderAPI is a system that allows for cross-compatability with other plugin's placeholders.

With PlaceholderAPI installed, our placeholders work in all the above areas and anywhere else with PlaceholderAPI
support, plus you can also use any placeholders from other plugins that also support PlaceholderAPI in these places in
Essence.

You don't need to install PlaceholderAPI to use placeholders, but if you do have it you can also use any other
placeholders supported by that plugin in these places too.

**You DO NOT need PlaceholderAPI if:**
* You are only using Essence's placeholders in Essence commands, files, or systems.

**You DO need PlaceholderAPI if:**
* You want to use Essence's placeholders in other plugins.
* You want to use other plugin's placeholders in Essence.
* You want to use PlaceholderAPI's built-in placeholders in Essence.

## Language Files
Language Files support the placeholder list above, and also use their own form of placeholders called arguments.

Arguments appear as a number inside curly braces, for example `{{1}}`, `{{2}}`.

**These should not be changed or removed.** These values are set by the function in Essence that causes that message 
to be sent. For example `Teleported to LewIsLost` appears as `Teleported to {{1}} in the language file.`

If you remove or change arguments, the messages will very likely be malformed. You can change any other part of the
language strings, add new things such as placeholders, but you should make a [custom language](ES-Language-Files.md#creating-a-new-language-file) as
it may be overwritten by an update.

If you accidentally break a language file, running `/es restore` will overwrite any changes you've made with our default
files.
