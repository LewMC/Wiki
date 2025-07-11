# Chat

<warning>
    <strong>Vault is required for Essence to be able to modify chat messages.</strong>
    Essence Chat private messages and broadcasts will work without Vault, but any features covering normal chat messages
    will not be active.
</warning>

Since 1.9.0, Essence can modify how chat works by adding prefixes and allowing players to use message formatting.

By default, uncoloured rank and team prefixes will appear, but you can change this if you'd like.

## Vault
Vault is a plugin that helps us manage chat messages. Some features may require it to work correctly.

| Feature                 | Vault required |
|-------------------------|----------------|
| Prefixes                | ✅              |
| Suffixes                | ✅              |
| Name formats            | ✅              |
| Message formatting      | ✅              |
| Nicknames               | ✅              |
| Private messages        | ❌              |
| Private message replies | ❌              |
| Broadcasts              | ❌              |

## Configuration
```
chat:
  enabled: true
  name-format: "%essence_combined_prefix% %essence_player%";
  allow-message-formatting: false
```

### enabled
`enabled` decides if Essence will handle chat messages. If you're using another chat plugin you'll probably want to disable this.

### name-format
`name-format` shows how the player's name will appear in chat.
For example the default format as shown in the above example configuration may show:

```
[Admin][Blue Team] LewIsLost: Hello!
[Default][Red Team] LewIsFound: Hi there, how are you?
```

You can use colour codes here with the `§` symbol, not the `&` symbol. For example the `name-format` value:

`§6%essence_combined_prefix% %essence_player%:§r`

will appear in chat as:

![ES-Chat colour codes.png](ES-Chat colour codes.png)

§r resets the formatting back to normal, or you can use another colour/style for chat messages, it's up to you! To have no colours, simply remove any § symbols and the character after them.

We're using [placeholders](ES-Placeholders.md) to make certain things display.
You can use any placeholders here, just remember to use `%essence_player%` or nobody will know who's talking!

### allow-message-formatting
`allow-message-formatting` decides if players are allowed to use &amp; codes in chat. If this is set to true any `&x` sent will be converted into colours.

For example: `Hello &lEverybody!` will be converted into <code>Hello <strong>Everybody!</strong></code>

![ES-Chat message formatting.png](ES-Chat message formatting.png)

## Prefixes and Suffixes
To add prefixes and suffixes you must have a plugin that provides them which is compatible with Vault installed. We recommend using LuckPerms and Vault.

Team Prefixes (including the combined prefix placeholder) will work without Vault and LuckPerms.

In LuckPerms, create a group and add `prefix.100.MyPrefixName` which will give anyone in the group the prefix "MyPrefixName".
The number is the "weight" of the prefix, you might need to tweak this. We recommend reading LuckPerm's documentation for help here, Essence just displays what it tells us to!

## Broadcasts
Broadcasts send a message to the entire server. They're commonly known to be important messages from administrators.

To send a broadcast use the `/broadcast` command, for example: `/broadcast This is my broadcast message`.

You'll need the `essence.chat.broadcast` permission to use this command.

## Private Messages
Private Messages are secret conversations between you and someone else.

To send a private message use the `/msg` command, for example: `/msg LewIsLost Hey there!` will send 'Hey there!' to LewIsLost.

To reply to the last private message that you received, use the `/r` or `/reply` command. For example: `/r Hi, how're you?`

You'll need the `essence.chat.msg` and `essence.chat.reply` permission to use these commands.

## Nicknames
Players with the `essence.chat.nick.self` permission can change their in-chat name, also known as nickname or displayname.

Simply type `/nick &lt;name>`

Players with the `essence.chat.nick.self` and `essence.chat.nick.other` permission can change their in-chat name, and the in-chat name of other players!

To do that type `/nick &lt;username> &lt;nickname>`
