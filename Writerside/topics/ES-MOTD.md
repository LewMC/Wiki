# MOTD

The MOTD ("Message of the Day") is a message that appears when a player logs into your server. It can be toggled and managed in the [Configuration](ES-Configuration.md).

## Tags
Tags are used to replace text with pre-generated values set by Essence. You can use these tags to set values that may change often such as versions.

| Tag                     | Description                                                  | Example             |
|-------------------------|--------------------------------------------------------------|---------------------|
| `{{essence-version}}`   | Get's the version of Essence the server is running.          | 1.4.0               |
| `{{minecraft-version}}` | Get's the version of Minecraft the server is running.        | 1.20.6              |
| `{{time}}`              | Gets the current time in format HH:MM:SS                     | 13:45:56            |
| `{{date}}`              | Gets the current date in format YYYY-MM-DD                   | 2024-05-19          |
| `{{datetime}}`          | Gets the current date and time in format YYYY-MM-DD HH:MM:SS | 2024-05-19 13:45:56 |