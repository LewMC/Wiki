# Message Tags

Message Tags are used to replace text with pre-generated values set by Essence. You can use these tags to set values that may change often such as versions.

## config.yml
Message Tags supported in config.yml strings are shown below. These can be used in the MOTD, or join/leave messages.

| Tag                     | Description                                                  | Example             |
|-------------------------|--------------------------------------------------------------|---------------------|
| `{{essence-version}}`   | Gets the version of Essence the server is running.           | 1.4.0               |
| `{{minecraft-version}}` | Gets the version of Minecraft the server is running.         | 1.20.6              |
| `{{time}}`              | Gets the current time in format HH:MM:SS                     | 13:45:56            |
| `{{date}}`              | Gets the current date in format YYYY-MM-DD                   | 2024-05-19          |
| `{{datetime}}`          | Gets the current date and time in format YYYY-MM-DD HH:MM:SS | 2024-05-19 13:45:56 |
| `{{player}}`            | The player who initiated the message's username              | Notch               |

## Language Files

Language files use a different system for Message Tags, they appear as `{{1}}`, `{{2}}`, etc.
These values are set by the function in Essence that causes that message to be sent.

You should <u>not</u> change these values.