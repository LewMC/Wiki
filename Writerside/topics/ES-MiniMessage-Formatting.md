# MiniMessage Formatting

<warning>
As of Essence 1.12.0, legacy (`§` and `&`) colour codes are no longer supported. Please migrate to MiniMessage Tags.
The language and configuration files will update automatically.
</warning>

Broadcasts, language file messages, and config-defined messages support MiniMessage formatting. Chat messages and
private messages support MiniMessage formatting when `allow-message-formatting` is set to `true` in the `chat`
[configuration](ES-Configuration.md) section.

All tags are placed inside `<tag>`. If you are changing an entire message, you don't need to close the tags.
You can close tags like this: `</tag>`, ending that tag section. For example,
`<red>Hello,<bold> world!</bold> how are you?` will make the whole sentence red, but only 'world!' will be bold.

## Colours

| Colour       | Tag                                                     | Legacy Code |
|--------------|---------------------------------------------------------|-------------|
| Black        | `<black>`                                               | §0          |
| Dark Blue    | `<dark_blue>`                                           | §1          |
| Dark Green   | `<dark_green>`                                          | §2          |
| Dark Aqua    | `<dark_aqua>`                                           | §3          |
| Dark Red     | `<dark_red>`                                            | §4          |
| Dark Purple  | `<dark_purple>`                                         | §5          |
| Gold         | `<gold>`                                                | §6          |
| Gray         | `<gray>`/`<grey>`                                       | §7          |
| Dark Gray    | `<dark_gray>`/`<dark_grey>`                             | §8          |
| Blue         | `<blue>`                                                | §9          |
| Green        | `<green>`                                               | §a          |
| Aqua         | `<aqua>`                                                | §b          |
| Red          | `<red>`                                                 | §c          |
| Light Purple | `<light_purple>`                                        | §d          |
| Yellow       | `<yellow>`                                              | §e          |
| White        | `<white>`                                               | §f          |
| Rainbow      | `<rainbow>`                                             |             |


### Using Hex
You can create custom colours using hex codes.

| Colour     | Tag                         | Legacy Code |
|------------|-----------------------------|-------------|
| Hex Colour | `<#00ff00>Example hex code` | _None_      |

### Gradients
You can create gradients using the `gradient` tag and two hex codes.

| Colour       | Tag                                                     | Legacy Code |
|--------------|---------------------------------------------------------|-------------|
| Gradient     | `<gradient:#0040FF:#00FBFF>Example Gradient</gradient>` | _None_      |

### Shadows

| Colour       | Tag                                       | Legacy Code |
|--------------|-------------------------------------------|-------------|
| Black        | `<shadow:black>`                          | _None_      |
| Dark Blue    | `<shadow:dark_blue>`                      | _None_      |
| Dark Green   | `<shadow:dark_green>`                     | _None_      |
| Dark Aqua    | `<shadow:dark_aqua>`                      | _None_      |
| Dark Red     | `<shadow:dark_red>`                       | _None_      |
| Dark Purple  | `<shadow:dark_purple>`                    | _None_      |
| Gold         | `<shadow:gold>`                           | _None_      |
| Gray         | `<shadow:gray>`/`<shadow:grey>`           | _None_      |
| Dark Gray    | `<shadow:dark_gray>`/`<shadow:dark_grey>` | _None_      |
| Blue         | `<shadow:blue>`                           | _None_      |
| Green        | `<shadow:green>`                          | _None_      |
| Aqua         | `<shadow:aqua>`                           | _None_      |
| Red          | `<shadow:red>`                            | _None_      |
| Light Purple | `<shadow:light_purple>`                   | _None_      |
| Yellow       | `<shadow:yellow>`                         | _None_      |
| White        | `<shadow:white>`                          | _None_      |
| Rainbow      | `<shadow:rainbow>`                        | _None_      |
| Hex Colour   | `<shadow:#00ff00>`                        | _None_      |

## Formatting
| Format        | Tag               | Legacy Code |
|---------------|-------------------|-------------|
| Bold          | `<bold>`          | §l          |
| Underline     | `<underline>`     | §n          |
| Italic        | `<italic>`        | §o          |
| Strikethrough | `<strikethrough>` | §m          |
| Magic         | `<magic>`         | §k          |
| Reset         | `<reset>`         | §r          |