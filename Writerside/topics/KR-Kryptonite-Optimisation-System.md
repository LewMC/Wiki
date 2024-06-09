# Kryptonite Optimisation System

The Kryptonite Optimisation System (KOS) is the optimisation system that runs on Kryptonite.

It works by modifying configuration files to match values preconfigured in Kryptonite [profiles](KR-Profiles.md). This is **not** a one-size fits all system, and you may wish to modify these values depending on your specific needs.

Kryptonite does not optimise the server directly, it enables a number of configuration optimisations built-in to your server software. Because of this you can uninstall the software after running the command, as Kryptonite does not need to be on the server once the process has been completed. However, keeping Kryptonite on the server will give you update messages which may contain additional optimisations in the future.

## Using KOS
There's two ways to use KOS - you can either run our recommended patches, or change them. Whilst the underlying system is the same Advanced Mode has more customisation, but also takes a lot more time to configure. Both ways provide incredible optimisation and lag reduction benefits to your server. We recommend using the recommended patches first, and then customise them as you see fit if you'd like to.

### Running the Recommended Patches
It's super simple to use KOS with the recommended patches - just type /kos into your server's console or chat menu (you need to be operator if you're doing it in chat as a player), and follow the instructions. KOS will then automatically apply the best patches taken from the guide linked at the top of this page.

### Customising KOS
Customising KOS brings a whole new layer of optimisation to KOS - and by that we mean you can optimise everything down to the very detail. KOS stores its patches in the 'profiles' folder that is created within the KOS folder. In there you'll find every value that is entered into your server's configuration files.

Some of these values affect gameplay mechanics, or may need to be restricted/loosened as time goes on. Whilst this may seem like it adds an additional step to the process, having all of your configuration files in one place can help you to understand how they interact with each other. There's more information on what each of these values do over at the [Configuration page](KR-Configuration.md).

Once you've edited these files, run /kos as you normally would.

### After KOS has finished.
Once you get the message saying it's done, restart your server and you're done! You can uninstall Kryptonite if you'd like to, or try the [Exploit Database](KR-Exploit-Database.md) next.

We recommend leaving Kryptonite installed so you get notified of any updates that may add new patches to the system.

Please note that for Purpur does not receive Pufferfish patches, and Pufferfish does not receive Purpur patches. Both receive all other patches.

Patches applied to upstreams of forks are also applied to their forks (for example: Paper gets Paper, Spigot, CraftBukkit, and Vanilla patches).

| File                     | Patches | Supported server jars                                               |
|--------------------------|---------|---------------------------------------------------------------------|
| server.properties        | 4       | All                                                                 |
| bukkit.yml               | 2       | All                                                                 |
| spigot.yml               | 5       | Spigot, Paper, Purpur, Pufferfish, Folia, or forks of any of these. |
| paper-world-defaults.yml | 57      | Paper, Purpur, Pufferfish, Folia, or forks of any of these.         |
| paper-global.yml         | 0       | Paper, Purpur, Pufferfish, Folia, or forks of any of these.         |
| purpur.yml               | 8       | Purpur, or any forks of this.                                       |
| pufferfish.yml           | 8       | Purpur, or any forks of this.                                       |