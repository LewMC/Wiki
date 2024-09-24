# Guide

<warning>
    <strong>We highly recommend backing up your server before using KOS.</strong>
    See <a href="KR-Backup.md">our backup guidance page</a> for more information.
</warning>

## Main Menu
The main menu provides quick access to either Manual or Automatic mode.

Automatic mode will ask you a few questions, then configure the server accordingly. We recommend you start here, then use manual mode to change things slightly if you need to.

Manual mode allows you to fine-tune configuration options to your liking.

## Automatic

## Manual
### Changing Values
To change values, simply click on the value you'd like to change! Left clicking will decrease the value by 1, and right clicking will increase the value by 1.

You can hold the shift key whilst clicking to change the value by 10 either way (depending on which mouse key you click). For example Shift+Left click will decrease the value by 10.

### Block Colours
| Colour | Meaning                                                                                                                                                                                                                                                                                                                          |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Green  | This is an ideal value for this option. Please note that ideal values may be in a range, so you can sometimes go a few options either way.                                                                                                                                                                                       |
| Red    | This value will likely impact the performance of your server. Hovering over the block will tell you if it's too high or too low.                                                                                                                                                                                                 |
| Orange | This value will likely impact the experience your players have on your server, as it may differ too far from typical Minecraft behaviour. This may include some features not working as expected, or certain technical skills such as mob farms being broken. Hovering over the block will tell you if it's too high or too low. |

## When you're done
You must restart your server for values set in KOS to be applied.
This is because most configuration files are cached so that their values cannot change whilst the server is running.
This is done to ensure the server does not have any errors or break.

Optimisations applied in KOS will not take effect until the server has restarted.

**Do not use the /reload command or reloading plugins** - This is highly flawed and can cause more problems, especially with permissions and other plugins.

If you're happy with your optimisations you can uninstall Kryptonite.
It is not required to stay on the server, and all your optimisations will remain.

If you'd prefer, you can keep it. You'll be notified if we push any updates, and you'll be able to modify your configuration later as well should you require any changes.

We also have the [Exploit Database](KR-Exploit-Database.md) that is part of Kryptonite as well, you might like to try that next.

## "Your server does not support this"
If you see this in the menus, it is because your server does not have the required configuration files present to be able to manage them.

If automatic or manual mode is listed as unsupported it is because no configuration files could be found.

To resolve this, please try to restart your server. If this does not help, please check that configuration files are present. You'll need to be using Bukkit or a fork of it (for example: Spigot, Paper, Pufferfish, Purpur, etc.), if you're not you may run into some issues.