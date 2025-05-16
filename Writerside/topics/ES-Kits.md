# Kits

Kits are sets of items that can be given to players via commands. The command to access Kits is /kit.

## kits.yml
Kits are stored in the kits.yml file which can be found in Essence's data folder (/plugins/essence/data).

### Example
The default example kits are as follows:
```
kits:
  wooden-tools:
    items: ["WOODEN_AXE","WOODEN_PICKAXE","WOODEN_SHOVEL","WOODEN_SWORD"]
    maxclaims: 1
  god-tools:
    items: ["DIAMOND_AXE","DIAMOND_PICKAXE","DIAMOND_SHOVEL","DIAMOND_SWORD"]
    maxclaims: 1
    permission: "essence.kits.god"
```
These example kits come pre-installed with Essence. If you've accidentally deleted them and would like to get them back, you can delete the kits.yml file and restart your server. The file will be re-generated.

### Parameters
| Parameter             | Description                                                                                                                                                                                          | Required? | Example                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| Kit name (root-level) | The name of your Kit - can be any string                                                                                                                                                             | Yes       | wooden-tools                                                     |
| items                 | List of items you'd like the player to receive from this kit - must be a list of strings (Each string must be a valid [Material](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html)) | Yes       | `["WOODEN_AXE","WOODEN_PICKAXE","WOODEN_SHOVEL","WOODEN_SWORD"]` |
| maxclaims            | The maximum number of times the kit can be claimed. To disable set to -1. Can be bypassed with permissions, see below. Kit claims are always being counted even if this restriction is not present, if you'd like to restart all user's counters either rename the kit of remove the counter from their player data file.  | Yes        | 3                                                 |
| permission            | <strong>Optional</strong> - See the "Permissions" section below.                                                                                                                                     | No        | essence.kits.god                                                 |

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
