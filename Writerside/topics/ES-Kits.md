# Kits

> **The kit file changed in Essence 1.12.0**
> Your kits will be automatically migrated to the new format when you first run the new update.

Kits are sets of items that can be given to players via commands. The command to access Kits is /kit. To give players
access to all kits commands give them the `essence.kits.*` command.

## kits.yml
Kits are stored in the kits.yml file which can be found in Essence's data folder (/plugins/essence/data).

### Example
The below example is the defualt kits.yml file:
```
kits:
  wooden-tools:
    name: Wooden Tools
    description: Some basic wooden tools.
    items:
      WOODEN_AXE:
        amount: 1
      WOODEN_PICKAXE:
        amount: 1
      WOODEN_SHOVEL:
        amount: 1
      WOODEN_SWORD:
        amount: 1
  god-tools:
    name: God Tools
    description: Some amazing tools! Can only claim once!
    permission: "essence.kits.god"
    maxclaims: 1
    items:
      DIAMOND_AXE:
        amount: 1
      DIAMOND_PICKAXE:
        amount: 1
        enchantments:
          - EFFICIENCY:2
          - UNBREAKING:2
      DIAMOND_SHOVEL:
        amount: 1
      DIAMOND_SWORD:
        amount: 1
```

### Parameters
Please see above for an example of these parameters in use.

| Parameter                 | Description                                                                                                                                                                                                                                                                                                               | Required? | Example                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------|
| Kit ID (root-level_       | The ID of your Kit - can be any string, this is what players use in the command (e.g. /kit kit-id)                                                                                                                                                                                                                        | Yes       | wooden-tools                       |
| name                      | The name of your kit, typically just a nicer looking version of the ID                                                                                                                                                                                                                                                    | Yes       | Wooden Tools                       |
| description               | The kit's description.                                                                                                                                                                                                                                                                                                    | Yes       | A cool kit with some wooden tools. |
| items.[ITEM]              | List of items you'd like the player to receive from this kit - each key is the item name (Each key must be a valid [Material](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html))                                                                                                                         | Yes       | `WOODEN_AXE`                       |
| items.[ITEM].amount       | The amount of the item you'd like to give the player (required)                                                                                                                                                                                                                                                           | Yes       | `1`                                |
| items.[ITEM].enchantments | Any enchantments you'd like the items to have (optional) (see DIAMOND_PICKAXE example above)                                                                                                                                                                                                                              | Yes       | `UNBREAKING:2`                     |
| maxclaims                 | The maximum number of times the kit can be claimed. To disable set to -1. Can be bypassed with permissions, see below. Kit claims are always being counted even if this restriction is not present, if you'd like to restart all user's counters either rename the kit of remove the counter from their player data file. | Yes       | 3                                  |
| permission                | <strong>Optional</strong> - See the "Permissions" section below.                                                                                                                                                                                                                                                          | No        | essence.kits.god                   |

## Permissions
Kits require users to have a set of permissions to access them.

You can set the permission to whatever you want, or remove it if you'd like any players to be able to get the kit.

Players with the `essence.kits.all` permission can access all kits regardless of this value.

Players with `essence.bypass.maxkitclaims`, including `essence.bypass.*` can redeem kits an infinite number of times.

## Spawn Kits
You can set it so that players are given kits when they first join the server. Please note that this is based on if they have joined the server in the past, not if they have received the kit or not.

Players must have the required permissions to access the kit.

Claiming the spawn kit counts towards the player's maximum kit claims.

You can change this value in the [Configuration](ES-Configuration.md).
