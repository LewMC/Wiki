# Configuration

Kryptonite provides a basic configuration file that can manage certain functions of the plugin.

For most users, leaving this on the default values will be fine.

## config.yml
| Value                                       | Accepts    | Default | Description                                                                                                                                                                                                              |
|---------------------------------------------|------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| update-check                                | Boolean    | true    | Should Kryptonite check the LewMC server for updates? This does not transfer any data from your server.                                                                                                                  |
| chat-alerts                                 | Boolean    | true    | Should Kryptonite tell operators about any pending alerts when they join the server?                                                                                                                                     |
| kos.override-pregenerated-world-protections | Boolean    | false   | You can enable this setting to override KOS's pre-generated world protections, this allows you to access treasure maps and dolphin features without pre-generating your world. This may cause additional lag if enabled. |
| kos.using-tcpshield                         | Boolean    | false   | Enable this if you're using TCPShield, this option prevents Kryptonite from applying patches that may cause instability or incompatibilities. Only affects Purpur Servers.                                               | 
| kos.world-is-pregenerated                   | String/Int | 0       | 0 = Unset, 1 = No, 2 = Yes --- Used by Automatic KOS.                                                                                                                                                                    | 
| verbose                                     | Boolean    | false   | Outputs additional information to the console. This may absolutely flood your log files and make it difficult to find stuff. Only turn it on if you need it, otherwise use the kryptonite.log file.                      | 
| logfile                                     | Boolean    | true    | Logs actions taken on Kryptonite to the kryptonite.log file.                                                                                                                                                             | 