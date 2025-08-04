# Admin

The admin module helps you to manage your server more efficiently. To give a player access to all admin module features
you can give them the `essence.admin.*` wildcard permission.

## Player Information
The player information command `/info` allows you to view information about players on your server. To access this
command you must either be an operator, or have the `essence.admin.info` permission.

You can see:
- The player's UUID/Unique ID
- The player's last known name
- The player's nickname
- When the player was last seen online
- The player's IP address (only if enabled in config & has `essence.admin.info.viewip` permission)
- The player's [team](ES-Teams.md)
- If the player has flying enabled
- The player's speed

## Invisibility
The /invisible command allows you to become invisible, hiding you from other players. To use this command you'll need
the `essence.admin.invisible` permission.

## Last-seen
The `/seen` command tells you when a player was last seen, it requires the `essence.admin.seen` permission.

To find a user, type `/seen [username]`.

For example: `/seen LewIsLost` will show when LewIsLost was last online.

If they have never joined it will say the player could not be found, and if they haven't joined since Essence began
recording this data it'll say they were never seen.