# Inventory

## /give command
The /give command overwrites the vanilla version. Essence's command allows you to give items to yourself and others.

### Giving items to yourself
This requires the `essence.inventory.give` permission

`/give &lt;item>` or `/give &lt;item> &lt;amount>`

### Giving items to another
This command can be run by the console.

This requires both the `essence.inventory.give` permission and the `essence.inventory.give.other` permission.

`/give &lt;player> &lt;item>` or `/give &lt;player> &lt;item> &lt;amount>`

## /invsee command
The /invsee command allows you to view another player's inventory. Due to the invasive nature of this command it is not
included in the wildcard.

### Blacklisting Items
The configuration file allows you to list items that should not be allowed to be given. The list is not case-sensitive,
but you should check that the names of items are correct. For example `WOODEN_SWORD` is valid but `WOOD_SWORD` is not.