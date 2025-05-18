# Permissions

<warning>
Using plugin reloaders can cause permissions lookups to fail. <a href="ES-Troubleshooting.md">Learn more</a>
</warning>

You need to give your players permission to access certain commands. By default, all Essence commands are restricted to players with permissions. You can use a permission system such as LuckPerms (highly recommended) to give players these permissions. Server operators ("ops") can access every Essence command without requiring permissions.

Permissions are listed in the tables on the [commands page](ES-Commands.md).

## Wildcards vs Granular
Essence uses Wildcard permissions for some commands. The wildcard permission can be used if you'd like to give users access to all commands in that section, it makes writing permissions a whole lot faster! Wildcard permissions are shows at the top of each section. They look like this:
`essence.gamemode.*`
If you use wildcard permissions, you don't need to give players other permissions from that section. For example if you use essence.gamemode.* you don't need to also use essence.gamemode.survival as that permission is included in the wildcard.

Alternatively, you can use granular permissions if there are only certain commands in a section you'd like players to be able to use. They look like this:
`essence.gamemode.survival`

### Administrator Wildcard

`essence.*` provides access to all standard Essence commands, this is useful for administrators.

`essence.admin.*` provides access to all Essence administrator commands, this is useful for administrators. Also allows for bypassing of various restrictions.

Administrators who require access to _everything_ should be given both these permissions.

#### Bypassing Restrictions
`essence.bypass.*` allows bypassing of all restrictions listed below.

Please note you should not give all players these permissions, instead disable the functionality in the configuration if desired.

| Restriction                                                              | Bypass Permission                       | Scope                      |
|--------------------------------------------------------------------------|-----------------------------------------|----------------------------|
| Teleport cooldown times (please wait X seconds before teleporting again) | `essence.bypass.teleportcooldown`       | All teleportation commands |
| Teleport delay times (teleporting in X seconds)                          | `essence.bypass.teleportdelay`          | All teleportation commands |
| Bypass extended teleport toggles.                                        | `essence.bypass.extendedteleporttoggle` | All teleportation commands |
| Maximum kit claims                                                       | `essence.bypass.maxkitclaims`           | All kit commands           |

## Update Alerts
`essence.admin.updates` shows update alerts in the chat when first joining.

## Warp and Home Creation Limits
By default, users can create as many warps and homes as they'd like. You can limit this by using permissions.

<warning>
If a user already has more homes than the limit before you apply it, this won't delete existing homes, it will just prevent the user from creating more.
</warning>


Using this feature, you can define the number of homes a user can create by using a permissions plugin. This allows different ranks to have a different number of homes.

### Warps
By giving a user the permission `essence.warp.limit.1`, it will limit the user to creating only 1 warp. You can change the number to what you'd like to set the limit to.

### Homes
By giving a user the permission `essence.home.limit.1`, it will limit the user to creating only 1 home. You can change the number to what you'd like to set the limit to.

### Team Homes
By giving a user the permission `essence.home.team.limit.1`, it will limit the user to creating only 1 team home. You can change the number to what you'd like to set the limit to.

A user must already be a member of a team to create team homes, and team homes must be enabled in the team's rules. [Learn more](ES-Teams.md).

<seealso>
    <category ref="es-commands">
        <a href="ES-Commands.md">Commands</a>
        <a href="ES-Disabling-Commands.md">Disabling Commands</a>
    </category>
</seealso>
