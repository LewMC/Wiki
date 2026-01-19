# Kits

> **The kit file changed in Essence 1.12.0**
> Your kits will be automatically migrated to the new format when you first run the new update.

Kits are sets of items that can be given to players via commands. The command to access Kits is /kit. To give players
access to all kits commands, give them the `essence.kits.*` command.

## kits.yml
Kits are stored in the kits.yml file, which can be found in Essence's data folder (/plugins/essence/data).

### Example
The below example is the default kits.yml file:
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
| items.[ITEM].enchantments | <strong>Optional</strong> - See the "Enchantments" section below.                                                                                                                                                                                                                                                         | Yes       | `UNBREAKING:2`                     |
| maxclaims                 | The maximum number of times the kit can be claimed. To disable set to -1. Can be bypassed with permissions, see below. Kit claims are always being counted even if this restriction is not present, if you'd like to restart all user's counters either rename the kit of remove the counter from their player data file. | Yes       | 3                                  |
| permission                | <strong>Optional</strong> - See the "Permissions" section below.                                                                                                                                                                                                                                                          | No        | essence.kits.god                   |

## Permissions
Kits require users to have a set of permissions to access them.

You can set the permission to whatever you want or remove it if you'd like any players to be able to get the kit.

Players with the `essence.kits.all` permission can access all kits regardless of this value.

Players with `essence.bypass.maxkitclaims`, including `essence.bypass.*` can redeem kits an infinite number of times.

## Spawn Kits
You can set it so that players are given kits when they first join the server. Please note that this is based on whether
they have joined the server in the past, not if they have received the kit or not.

Players must have the required permissions to access the kit.

Claiming the spawn kit counts towards the player's maximum kit claims.

You can change this value in the [](ES-Configuration.md).

## Enchantments
As of Essence 1.12.0, Kits now support enchantments. You can use any valid Minecraft enchantment and level in the format
ENCHANTMENT:LEVEL.

Enchantments should be added to each item as a list, even if there is only one. For example:
```yaml
items:
  # No enchantments
  DIAMOND_SWORD:
    amount: 1
  # A single enchantment
  DIAMOND_AXE:
    amount: 1
    enchantments:
      - UNBREAKING:2
  # Multiple enchantments
  DIAMOND_PICKAXE:
    amount: 1
    enchantments:
      - EFFICIENCY:2
      - UNBREAKING:2
```

Please see the below tables for a list of valid enchantments.

> You can bypass the enchantment maximum level in the [](ES-Configuration.md) by setting `allow-unsafe-enchantments` to 
> `true`.

### All-Purpose

<table>
    <tr><th>Enchantment</th><th>Max Level</th><th>Description</th></tr>
    <tr><td>MENDING</td><td>1</td><td>Repairs the item when gaining XP orbs.</td></tr>
    <tr><td>UNBREAKING</td><td>3</td><td>Increases item durability.</td></tr>
    <tr><td>CURSE_OF_VANISHING</td><td>1</td><td>Item destroyed upon death.</td></tr>
</table>

### Armour

<table>
    <tr><th>Enchantment</th><th>Max Level</th><th>Description</th></tr>
    <tr><td>AQUA_AFFINITY</td><td>1</td><td>Increase the rate of underwater mining speed.</td></tr>
    <tr><td>BLAST_PROTECTION</td><td>4</td><td>Reduces explosion damage and knockback. </td></tr>
    <tr><td>CURSE_OF_BINDING</td><td>4</td><td>Items cannot be removed from armour slots unless the cause is death or breaking.</td></tr>
    <tr><td>DEPTH_STRIDER</td><td>3</td><td>Increases underwater movement speed.</td></tr>
    <tr><td>FEATHER_FALLING</td><td>4</td><td>Reduces fall damage.</td></tr>
    <tr><td>FIRE_PROTECTION</td><td>4</td><td>Reduces fire damage and burn time.</td></tr>
    <tr><td>FROST_WALKER</td><td>2</td><td>Changes the water source blocks beneath the player into frosted ice and prevents the damage the player would take from standing on magma blocks.</td></tr>
    <tr><td>PROJECTILE_PROTECTION</td><td>4</td><td>Reduces projectile damage.</td></tr>
    <tr><td>PROTECTION</td><td>4</td><td>Reduces most types of damage by 4% for each level.</td></tr>
    <tr><td>RESPIRATION</td><td>3</td><td>Extends underwater breathing time.</td></tr>
    <tr><td>SOUL_SPEED</td><td>3</td><td>Increases walking speed on soul sand and soul soil.</td></tr>
    <tr><td>THORNS</td><td>3</td><td>Reflects some of the damage taken when hit, at the cost of reducing durability.</td></tr>
    <tr><td>SWIFT_SNEAK</td><td>3</td><td>Increased player speed when crouching.</td></tr>
</table>

### Melee Weapons

<table>
    <tr><th>Enchantment</th><th>Max Level</th><th>Description</th></tr>
    <tr><td>BANE_OF_ARTHROPODS</td><td>5</td><td>Increases damage and applies Slowness IV to arthropod mobs (spiders, cave spiders, silverfish, endermites and bees).</td></tr>
    <tr><td>BREACH</td><td>4</td><td>Negate the effectiveness of enemy armour by 15% per level.</td></tr>
    <tr><td>DENSITY</td><td>5</td><td>Boosts the rate at which mace multiplies damage while falling.</td></tr>
    <tr><td>EFFICIENCY</td><td>5</td><td>When applied to an axe, it increases the chance that the axe may stun a shield, with the base chance being 25% and a 5% increase for each level of efficiency.</td></tr>
    <tr><td>FIRE_ASPECT</td><td>2</td><td>Sets target on fire.</td></tr>
    <tr><td>LOOTING</td><td>3</td><td>Increases the amount of loot earned from mobs.</td></tr>
    <tr><td>LUNGE</td><td>3</td><td>Spear jabs get a burst of speed. Consumes saturation and hunger.</td></tr>
    <tr><td>IMPALING</td><td>5</td><td>Trident deals additional damage to mobs that spawn naturally in the ocean.</td></tr>
    <tr><td>KNOCKBACK</td><td>2</td><td>Knocks back mobs away from you when hit.</td></tr>
    <tr><td>SHARPNESS</td><td>5</td><td>Increases weapon damage.</td></tr>
    <tr><td>SMITE</td><td>5</td><td>Increases damage to undead mobs.</td></tr>
    <tr><td>SWEEPING_EDGE</td><td>3</td><td>Increases sweeping attack damage.*</td></tr>
    <tr><td>WIND_BURST</td><td>3</td><td>Allows the player to bounce up into the air following a successful hit; the height of this bounce increases with higher enchantment levels.</td></tr>
</table>

<sub>* Minecraft Java Edition only – will not work for Bedrock players on Geyser servers.</sub>

### Ranged Weapons

<table>
    <tr><th>Enchantment</th><th>Max Level</th><th>Description</th></tr>
    <tr><td>CHANNELING</td><td>1</td><td>Trident channels a bolt of lightning toward a hit entity. Functions only during thunderstorms and if the target is unobstructed by opaque blocks.</td></tr>
    <tr><td>FLAME</td><td>1</td><td>Arrows set targets on fire.</td></tr>
    <tr><td>IMPALING</td><td>5</td><td>Trident deals additional damage to mobs that spawn naturally in the ocean.</td></tr>
    <tr><td>INFINITY</td><td>1</td><td>Shooting with projectiles does not consume arrows.</td></tr>
    <tr><td>LOYALTY</td><td>3</td><td>Trident returns after being thrown. Higher levels reduce the return time.</td></tr>
    <tr><td>RIPTIDE</td><td>3</td><td>Trident launches the player with itself when thrown. Functions only in water or rain.</td></tr>
    <tr><td>MULTISHOT</td><td>1</td><td>Shoot three arrows at the cost of one; only one arrow can be recovered.</td></tr>
    <tr><td>PIERCING</td><td>4</td><td>Arrows pass through multiple entities.</td></tr>
    <tr><td>POWER</td><td>5</td><td>Increases arrow damage.</td></tr>
    <tr><td>PUNCH</td><td>2</td><td>Increases arrow knockback.</td></tr>
    <tr><td>QUICK_CHARGE</td><td>3</td><td>Decreases crossbow charging time.</td></tr>
</table>

### Tools

<table>
    <tr><th>Enchantment</th><th>Max Level</th><th>Description</th></tr>
    <tr><td>EFFICIENCY</td><td>5</td><td>Increases mining speed.</td></tr>
    <tr><td>FORTUNE</td><td>3</td><td>Increases certain item drop chances from blocks.</td></tr>
    <tr><td>LUCK_OF_THE_SEA</td><td>3</td><td>Increases rate of fishing rare loot (enchanting books, etc.)</td></tr>
    <tr><td>LURE</td><td>3</td><td>Decreases wait time until fish/junk/loot "bites"</td></tr>
    <tr><td>SILK_TOUCH</td><td>1</td><td>Mined blocks will drop as blocks instead of breaking into other items/blocks.</td></tr>
</table>