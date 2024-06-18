# Teams
<warning>
Users will need to have the <a href="ES-Commands.md">correct permissions</a> to be able to access these features.
</warning>

## What is a team?
A team is a group of players that join together to share certain resources. Similarly to factions, teams allow for configurable rulesets and access levels depending on user preference.

### Should I enable teams on my server?
Why not! Even if you don't plan on having much team-based play or functionality, it's a useful and fun system for players to use. It allows players to share homes and avoid hurting each other, so it can be good when playing with friends.

## Team features
### Managing teams
Teams can be created by using the `/team create <name>` command.

You can disband (delete) by using the `/team disband` command.

You can hand the leadership over to another player by using `/team changeleader <name>`

If you want to remove someone from your team you can use `/team kick <name>`.

### Join requests
Joining teams is managed by a request system. To send a join request use the `/team join <name>` command. The team leader can then use `/team requests` to view incoming requests.

To accept pending requests use `/team accept <name>` or `/team decline <name>`.

If you want to remove someone from your team you can use `/team kick <name>`.

### Rules
Rules are a set of values that control gameplay features when players are in teams. You can set these by using `/team rule <rule> <value>` and see what they're currently set as by using `/team rule <rule>`

| Rule                  | Description                   | Accepted Values | Default |
|-----------------------|-------------------------------|-----------------|---------|
| `allow-friendly-fire` | Allows PvP between teammates. | true or false   | true    |

### Team Homes
Alongside having personal homes, teams can also have joint homes. These are set using the `/thome` commands.

You'll need to give players access to the home command wildcard or the thome command permissions. You can find out more on the [commands page](ES-Commands.md).

Team homes work exactly the same as normal homes, except they're shared amongst team members. Every team member can access every team home.