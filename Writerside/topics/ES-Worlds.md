# Worlds

The worlds module can be used to create and manage worlds.

## Teleport to a World
Command: `/world tp <world name>` or `/spawn <world name>`

Using `/spawn` on it's own will teleport you to the spawn of the world you're currently in, unless a lobby world is set.

### Global Spawn / Lobby World and Forced Spawns
See [Teleportation](ES-Teleportation.md#spawns).

## Load or Unload a World
Command: `/world load <world name>` or `/world unload <world name>`

Worlds must be loaded before players can access them. Worlds created by Essence (and your world set in server.properties)
are automatically loaded upon startup by default. Worlds created outside of Essence or created with the `-a` flag set to
false must be loaded manually.

Worlds must be unloaded before deleting them.

To see which worlds are loaded use `/world list`.

## Delete a World
Command: `/world delete <world name>`

Worlds must be unloaded before they can be deleted. Deletion is permanent and cannot be undone, and there is no
confirmation step in this command.

## Create a World
Command: `/world create <world name> <flags...>`

Creating a world will also load it into memory. Unless set otherwise using one of the flags below, Essence will always
load the world on startup by default.

### Flags
The command accepts a number of flags to configure the world. Flags are optional, and any left out will use their
default values.

For example, `/world create new_end -e END -s TRUE`

**To use a flag's default value, leave it out of the command.**

| Flag  | About                                                                                                                   | Allowed values                                            | Default value     |
|-------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|-------------------|
| `-b`  | **Biome Provider** - Sets the world's biome provider. (Advanced)                                                        | Any valid biome provider                                  | Minecraft default |
| `-e`  | **Environment** - Sets the world's environment. This changes how the world looks and works as a "dimension" to players. | `NORMAL`,<br/>`NETHER`,<br/>`END`, or <br/>`CUSTOM`       | `NORMAL`          |
| `-g`  | **Generator**  - The world's generator. (Advanced)                                                                      | Any valid generator                                       | Minecraft default |
| `-gs` | **Generator Settings**  - The world's generator settings. (Advanced)                                                    | Any valid generator settings                              | Minecraft default |
| `-h`  | **Hardcore** - Sets if the world is in hardcore mode or not.                                                            | `TRUE` or `FALSE`                                         | `FALSE`           |
| `-n`  | **Generate Structures** - If the world should generate structures.                                                      | `TRUE` or `FALSE`                                         | `TRUE`            |
| `-s`  | **Seed** - The world's seed.                                                                                            | Any number                                                | Random            |
| `-t`  | **World Type** - The Minecraft world type.                                                                              | `NORMAL`,<br/>`FLAT`,<br/>`AMPLIFIED`,<br/>`LARGE_BIOMES` | `NORMAL`          |
| `-a`  | **Autoload** - Should the world be loaded on server startup?                                                            | `TRUE` or `FALSE`                                         | `TRUE`            |

## Troubleshooting
Please see [the troubleshooting page](ES-Troubleshooting.md#world-management).
