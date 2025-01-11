# Kryptonite Optimisation System

<warning>
    <b>This guide applies to Kryptonite 2.0.0 and above.</b> KOS received major changes and improvements in this version. We highly recommend updating.
</warning>

The Kryptonite Optimisation System (KOS) is the optimisation system that runs on Kryptonite.

It works by modifying configuration files to match values preconfigured in Kryptonite [profiles](KR-Profiles.md).
This is **not** a one-size fits all system, and you may wish to modify these values depending on your specific needs.
You can also modify individual values manually if you'd prefer.

Kryptonite does not optimise the server directly, it enables a number of configuration optimisations built-in to your server software.
Because of this you can uninstall the software after running the command, as Kryptonite does not need to be on the server once the process has been completed.
However, keeping Kryptonite on the server will give you update messages which may contain additional optimisations in the future.

## Using KOS
See [our how to use KOS guide](KR-KOS-Guide.md) for help on using KOS.

## Supported patches
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