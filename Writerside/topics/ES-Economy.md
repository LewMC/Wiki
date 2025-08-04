# Economy

The economy module helps you to manage your server more efficiently. To give a player access to all economy module
features you can give them the `essence.economy.*` wildcard permission.

You can change the money symbol ($/etc) and starting money in the configuration file.

## Checking your balance
Use `/bal` to check your balance. It requires the `essence.economy.balance` permission.

## Paying another player
Use `/pay <player>` to pay another player. It requires the `essence.economy.pay` permission.

## Other Plugins
Provided the configuration (see below) is set to VAULT, other plugins can also interact with your Essence balance. This
includes any plugins that have Vault support. For example you can use your Essence balance to buy items in shops, and
receive money from sales this way too.

## Configuration
The economy may work slightly differently depending on how you configure it. If Vault is installed Essence will act as
the economy provider for other plugins on your server, and Essence's balance and pay commands will be the main ones.

To change this, set economy.mode to the following:

| economy.mode value | What it does                                                                                                                                                                 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VAULT              | **Default, Recommended** Allows Essence to give other plugins access to it's economy via the Vault plugin. If Vault isn't installed this mode will behave like ESSENCE mode. |
| ESSENCE            | Essence keeps it's economy to itself - our economy commands will still work but other plugin's access to Essence's economy is prohibited.                                    |
| OFF                | Disables economy features entirely.                                                                                                                                          |
