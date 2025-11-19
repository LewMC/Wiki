# Stats
<warning>
    <strong>Commands in this module can give players unfair advantages.</strong>
    If you're playing survival, be cautious giving these permissions to players.
</warning>

The stats module allows you to modify player statistics. To give players access to all stats commands you can give them
the `essence.stats.*` permission.

## Feed

`/feed` will refill your hunger bar, `/feed <player>` will refill another player's

To feed yourself you'll need the `essence.stats.feed` permission, and to feed someone else you'll need that plus
`essence.stats.feed.other`

## Fly
Set if you can fly in survival using `/fly`. The command toggles it on and off.

| Format        | Function                     | Permission                                        |
|---------------|------------------------------|---------------------------------------------------|
| /fly          | Allows you to fly.           | `essence.stats.fly`                               |
| /fly <player> | Allows another player to fly | `essence.stats.fly` and `essence.stats.fly.other` |

## Heal

`/heal` will refill your health bar, `/heal <player>` will refill another player's

To heal yourself you'll need the `essence.stats.heal` permission, and to heal someone else you'll need that plus
`essence.stats.heal.other`

## Repair

`/repair` will remove all damage from the tool in your hand. You'll need the `essence.stats.repair` permission to do this.
This command can not be run from the console.

## Speed
Set your walking and flying speed using `/speed`. The speed value must be between -10 and 10. The default value is 2.

| Format                  | Function                          | Permission                                            |
|-------------------------|-----------------------------------|-------------------------------------------------------|
| /speed <value>          | Sets your speed                   | `essence.stats.speed`                                 |
| /speed reset            | Resets your speed to the default. | `essence.stats.speed`                                 |
| /speed <value> <player> | Sets another player's speed       | `essence.stats.speed` and `essence.stats.speed.other` |
| /speed reset <player>   | Resets another player's speed     | `essence.stats.speed` and `essence.stats.speed.other` |

## Burn & Extinguish
You can burn yourself or another player using `/burn`, and extinguish (stop burning them) using `/extinguish`. You'll
need the `essence.stats.burn` and `essence.stats.extinguish` permissions respectively.

## God
God mode can be enabled with `/god`, or for someone else using `/god <player>`.

## Enchant
You can enchant an item using `/enchant <enchantment> <level>`.

To god yourself you'll need the `essence.stats.god` permission, and to god someone else you'll need that plus
`essence.stats.god.other`
