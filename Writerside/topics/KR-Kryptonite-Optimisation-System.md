# Kryptonite Optimisation System

<warning>
    <b>This guide applies to Kryptonite 1.4.0 and above.</b> KOS received major changes and improvements in this version. We highly recommend updating.
</warning>

The Kryptonite Optimisation System (KOS) is the optimisation system that runs on Kryptonite.

It works by modifying configuration files to match values preconfigured in Kryptonite [profiles](KR-Profiles.md). This is **not** a one-size fits all system, and you may wish to modify these values depending on your specific needs.

Kryptonite does not optimise the server directly, it enables a number of configuration optimisations built-in to your server software. Because of this you can uninstall the software after running the command, as Kryptonite does not need to be on the server once the process has been completed. However, keeping Kryptonite on the server will give you update messages which may contain additional optimisations in the future.

## Using KOS
### In-game
> This is the recommended way to use KOS.

Run /kos in-game (you must be an operator), select the profile you'd like to use, and then tell KOS if your world is pre-generated.

That's it! Once you're done, you can uninstall Kryptonite or keep it for update notifications.

### From the console
First, check the profile you want to use is selected (see [configuration](KR-Configuration.md)).

Run /kos, then follow the instructions.

That's it! Once you're done, you can uninstall Kryptonite or keep it for update notifications.

### Custom Profiles
If you don't like the profiles we've provided, you can make your own! See [profiles](KR-Profiles.md) for more information.

### After KOS has finished.
Once you get the message saying it's done, restart your server and you're done! You can uninstall Kryptonite if you'd like to, or try the [Exploit Database](KR-Exploit-Database.md) next.

We recommend leaving Kryptonite installed so you get notified of any updates that may add new patches to the system.

Please note that for Purpur does not receive Pufferfish patches, and Pufferfish does not receive Purpur patches. Both receive all other patches.

Patches applied to upstreams of forks are also applied to their forks (for example: Paper gets Paper, Spigot, CraftBukkit, and Vanilla patches).

| File                     | Patches | Supported server jars                                               |
|--------------------------|---------|---------------------------------------------------------------------|
| server.properties        | 4       | All                                                                 |
| bukkit.yml               | 2       | All                                                                 |
| spigot.yml               | 5       | Spigot, Paper, Purpur, Pufferfish, Folia, or forks of any of these. |
| paper-world-defaults.yml | 57      | Paper, Purpur, Pufferfish, Folia, or forks of any of these.         |
| paper-global.yml         | 0       | Paper, Purpur, Pufferfish, Folia, or forks of any of these.         |
| purpur.yml               | 8       | Purpur, or any forks of this.                                       |
| pufferfish.yml           | 8       | Purpur, or any forks of this.                                       |

## Treasure Maps
Kryptonite may change how Treasure Maps appear and generate in the world - see [Treasure Maps](KR-Treasure-Maps.md) for more information.