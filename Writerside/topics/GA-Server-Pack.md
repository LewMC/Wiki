# Server Pack

<warning>
You will need to edit your port number in server.properties if your server does not use the default 25565.
</warning>

> To update your server pack, extract it first outside of the server's directory, delete your existing 'mods' folder, then just upload/copy across the 'mods' folder.

## Running on a server host
1. Upload and uncompress the .zip pack file,
2. In your hosting panel set the startup jar to `galactica-server.jar` for Galactica, or `galactica-je-server.jar` for Galactica: Jurassic Edition, your host should have instructions on how to do this.
3. Start the server, it should generate the required files but not start.
4. Open EULA.txt and accept it.
5. Restart the server, it should now start.

## Running Locally
<warning>
   <strong>Local servers are resource intensive, especially if you're playing the game on the same machine.</strong>
   If you're running a server locally, you'll need to ensure you have enough processing power on your computer to handle the game twice.
</warning>

If you'd like your friends to be able to connect, you'll need to port forward your internet. [More info (external link)](https://portforward.com)

First, unzip the server pack, then follow the instructions in the relevant section for you below.

### Windows
1. Create a new file titled 'start.bat'
2. In the file, enter this for Galactica:
    <code-block>
    @echo off
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-server.jar nogui
    pause
    </code-block>
    or this for Galactica: Jurassic Edition:
    <code-block>
    @echo off
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-je-server.jar nogui
    pause
    </code-block>
3. Replace the '#' with the amount of RAM you'd like to allocate to the server.
4. Run the file by double-clicking it, the server should generate the required files but not start.
5. Open EULA.txt and accept it.
6. Run the file again by double-clicking it, the server should now start.

### MacOS
> If it doesn't run, use `chmod a+x` in the terminal to give it more permissions.
1. Create a new file titled 'start.command'
2. In the file, enter this for Galactica:
    <code-block>
    #!/bin/sh
    cd "$( dirname "$0" )"
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-server.jar nogui
    </code-block>
    or this for Galactica: Jurassic Edition:
    <code-block>
    #!/bin/sh
    cd "$( dirname "$0" )"
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-je-server.jar nogui
    </code-block>
3. Replace the '#' with the amount of RAM you'd like to allocate to the server.
4. Run the file by double-clicking it, the server should generate the required files but not start.
5. Open EULA.txt and accept it.
6. Run the file again by double-clicking it, the server should now start.

### Linux
> If it doesn't run, use `chmod +x start.sh` in the terminal to give it more permissions.
1. Create a new file titled 'start.sh'
2. In the file, enter this for Galactica:
    <code-block>
    #!/bin/sh
    
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-server.jar nogui
    </code-block>
    or this for Galactica: Jurassic Edition:
    <code-block>
    #!/bin/sh
    
    java -Xms#G -Xmx#G -XX:+UseG1GC -jar galactica-je-server.jar nogui
    </code-block>
3. Replace the '#' with the amount of RAM you'd like to allocate to the server.
4. Run the file using `./start.sh`, the server should generate the required files but not start.
5. Open EULA.txt and accept it.
6. Run the file again using `./start.sh`, the server should now start.