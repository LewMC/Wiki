# Time and Weather

## Commands
Time and Weather commands consist of /time, /weather, /ptime, and /pweather.
They all work in the same way - send it without arguments to check, with to set.

For example: `/time` will check the time, and `/time day` or `/time 1000` will set the time.

## Time Values

> To reset the player time back to the server time, use `/ptime reset`

Time in Minecraft works on numerical values, typically 0-24000 in a single day.

However, it's much easier to use preset times - and we have loads! You can either use the numbers, or the alias instead - they'll both work!

| Alias    | Minecraft Equivalent | Usage Example  |
|----------|----------------------|----------------|
| day      | 1000                 | /time day      |
| morning  | 1000                 | /time morning  |
| noon     | 6000                 | /time noon     |
| midday   | 6000                 | /time midday   |
| evening  | 10000                | /time evening  |
| sunset   | 12000                | /time sunset   |
| night    | 13000                | /time night    |
| midnight | 18000                | /time midnight |
| sunrise  | 23000                | /time sunrise  |

## Weather Values

> To reset the player weather back to the server weather, use `/pweather reset`

Same as with time, we've also added some aliases to weather - you can use whichever you'd like!

| Alias     | Minecraft Equivalent | Usage Example      |
|-----------|----------------------|--------------------|
| clear     | clear                | /weather clear     |
| sun       | clear                | /weather sun       |
| sunny     | clear                | /weather sunny     |
| rain      | storm                | /weather rain      |
| raining   | storm                | /weather raining   |
| downpour  | storm                | /weather downpour  |
| storm     | thunder              | /weather storm     |
| thunder   | thunder              | /weather thunder   |
| lightning | thunder              | /weather lightning |

## Console Usage
Console usage is slightly different - since the console "user" is not in a world, they need to specify which one they're talking about.

For example when checking the weather a player would use `/weather`, but the console must use `/weather world`, replacing `world` with the world name.

Likewise when setting the weather a player would use `/weather clear`, but the console must use `/weather world clear`, replacing `world` with the world name.

The usage is the same for time.

Consoles cannot use /ptime or /pweather.