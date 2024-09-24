# Profiles

<warning>
<strong>Custom profiles MUST have all the options present in the provided profile to work correctly.</strong> There is currently no detection for missing values and leaving values blank <u>will break your server</u>.
</warning>

Profiles are collections of settings or configuration options that can be used as templates for KOS.

## Provided Profiles
There is currently 2 provided profiles.

| Profile        | Authors                                          | Description                                                                                                                                                                                                                                                                                                                                                               |
|----------------|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| YouHaveTrouble | YouHaveTrouble (Values), LewMC (Kryptonite Port) | The YouHaveTrouble profile is an aggressive optimisation profile used to apply the [YouHaveTrouble Optimisation Guide](https://github.com/YouHaveTrouble/minecraft-optimization) to your server. This profile breaks a number of vanilla gameplay mechanics including mob farms and mob spawning, but is the most aggressive against lag and will yield the best results. |
| FarmFriendly   | LewMC                                            | This profile applies patches that won't break mob farms, but may yield less positive results.                                                                                                                                                                                                                                                                             |

## Custom Profiles
You can create a custom profile by copying one of the provided profiles, renaming it, and modifying it's values.

If you're using KOS in-game, it should appear in the menu - if it does not, restart the server.

If you're using KOS from the console, you'll need to edit Kryptonite's [configuration](KR-Configuration.md) to run your custom profile.

### Sharing your Profile
If you'd like to share your profile with us to be added to KOS, we'd be happy to take it! You'll be given full credit via the in-game menu and profile list here, simply open an issue on [GitHub](https://github.com/lewmc/kryptonite) and send us the file.