# Configuration

Kryptonite provides a basic configuration file that can manage certain functions of the plugin.

For most users, leaving this on the default values will be fine.

## config.yml
| Value                                       | Accepts | Default        | Description                                                                                                                                                                                                              |
|---------------------------------------------|---------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| update-check                                | Boolean | true           | Should Kryptonite check the LewMC server for updates? This does not transfer any data from your server.                                                                                                                  |
| kos.default-profile                         | String  | YouHaveTrouble | **If you're using KOS in-game, you can ignore this.** The name of the .kos file in the /profiles/ folder that Kryptonite will use when being run from the console.                                                       |
| kos.override-pregenerated-world-protections | Boolean | false          | You can enable this setting to override KOS's pre-generated world protections, this allows you to access treasure maps and dolphin features without pre-generating your world. This may cause additional lag if enabled. |
| kos.using-tcpshield                         | Boolean | false          | Enable this if you're using TCPShield, this option prevents Kryptonite from applying patches that may cause instability or incompatibilities. Only affects Purpur Servers.                                               | 