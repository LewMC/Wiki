# Troubleshooting

<warning>
    <strong>Legacy versions of Kryptonite are no longer supported.</strong>
    If you haven't already, we highly recommend updating to Kryptonite 2.0.0 or newer.
</warning>

## Reloading Kryptonite
Reloading your server using the /reload command, or reloading Kryptonite using a plugin such as Plugman can cause a huge number of issues.

As such, we will not provide support for plugin reloaders.

Issues caused can range from permissions lookups failing, memory leaks, zip file exceptions, and more.

We **highly** recommend restarting your server instead of reloading it.

## Kryptonite broke my server, help!
We're sorry to hear our software caused you issues.

If you took a backup of your server before using Kryponite, you could roll back your changes.

If you didn't take a backup have a look at your server logs, they should say which configuration file is causing issues.
Once you've identified the file, delete it and restart your server.
Your server will automatically re-generate the default version of the file.

If you can't figure out which file went wrong, you can delete all your configuration files, or contact us and we'll
help you find the issue.

The configuration files we handle [can be found on the KOS page](KR-Kryptonite-Optimisation-System.md) under "Supported patches﻿".

Please send us a copy of your logs and config files via [GitHub](https://github.com/lewmc/kryptonite) or
[Discord](https://lewmc.net/discord) and we'll look into what caused the issue.
