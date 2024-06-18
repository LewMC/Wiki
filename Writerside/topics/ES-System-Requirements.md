# System Requirements

<warning>
Some commands do not work on Folia-based servers, please see the section at the bottom of this page for more information.
</warning>

| Essence Version | Minecraft Versions | Supported Software                                            | Java Version | Active Support |
|-----------------|--------------------|---------------------------------------------------------------|--------------|----------------|
| 1.4.0+          | > 1.20.4           | CraftBukkit, Spigot, Paper, Folia, or a fork of these         | 17           | Yes            |
| 1.0.0 - 1.3.2   | > 1.19.0           | CraftBukkit, Spigot, Paper, or a fork of these (except Folia) | 17           | No             |

## Minecraft Version Support
We aim to support as many Minecraft versions as possible, however this may not always be possible.

We generally do not provide bug fixes for older versions of Minecraft if newer versions of Essence no longer support it.
If you're unusure if we'll fix something, ask! [Open an issue on our GitHub](https://github.com/lewmc/essence/issues) and we'll advise there.
If you're running a version of Essence that is still actively supported, we'll fix any and all bugs and issues.

We may drop support for certain Minecraft versions due to technical limitations, vulnerabilities, or other reasons.

## Folia Support
Essence supports Folia-based Minecraft Server Software in versions 1.4.0 and greater.

Unfortunately, due to how the Folia software works, some commands are currently disabled as we're not able to add support for them at this time due to technical reasons.
If you'd like to help us add support for these commands on Folia-based servers, please [open a pull request on our GitHub](https://github.com/lewmc/essence).

| Disabled Command | Since | Reason                                                                                       |
|------------------|-------|----------------------------------------------------------------------------------------------|
| /tprandom        | 1.4.0 | Folia generates an exception when running this command due to the way RegionSchedulers work. |