# Worlds

The worlds module can be used to create and manage worlds.

## Create a World
Command: `/world create <world name> <flags>`

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
