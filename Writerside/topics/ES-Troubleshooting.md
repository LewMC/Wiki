# Troubleshooting

## Invalid move player packet received
This error can sometime occur when a non-vanilla loaded world is set as the main-world if always-spawn is also enabled.
We recommend setting the main-world to a vanilla loaded world (the world set in server.properties) if you also use always-spawn.

If this is not causing the issue please [open an issue](https://github.com/lewmc/essence/issues).

## Unable to send message to player.

### 1.6.0 and above.
Please check your plugins/Essence/language folder. If it contains "![Old en-gb.yml](en-gb-old.yml.png)", please delete this file and restart your server.

The English language file should be "![en-gb.yml](en-gb.yml.png)", it appears that your server was unable to migrate the file to the new format correctly which may be causing your issue.

If this is not causing the issue please [open an issue](https://github.com/lewmc/essence/issues).

### Pre-1.6.0
Please delete your en-gb.yml file and restart your server.
Please note that earlier versions are no longer supported for bug-fixes, and we recommend updating Essence.

## Reloading Essence
Reloading your server using the /reload command, or reloading Essence using a plugin such as Plugman can cause a huge number of issues.

As such, we will not provide support for plugin reloaders.

Issues caused can range from permissions lookups failing, memory leaks, zip file exceptions, and more.

We **highly** recommend restarting your server instead of reloading it.