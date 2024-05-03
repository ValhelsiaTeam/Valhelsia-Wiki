---
description: >-
  A guide to setting up a self-hosted Valhelsia server on Windows, Mac, or
  Linux.
---

# Server Setup

For easy reliable server setup and hosting, we recommend using [BisectHosting](https://bisecthosting.com/Valhelsia) to run Valhelsia servers. Use the code "**Valhelsia**" to get **25%** off your first month as a new client for any of their gaming servers. We recommend that you use **at least 4GB** to run the pack smoothly with 5-7 players.

{% embed url="https://www.bisecthosting.com/Valhelsia" %}
Link to their website.
{% endembed %}

The guide below is for self-hosting a server. You will need to be familiar with how to setup a vanilla Minecraft server before following this guide. If you are using another hosting provider, please see their documentation too, and contact their support first if you have any issues.

## <mark style="color:orange;">Before Beginning</mark>

You should ensure that you are familiar with how to setup a regular (vanilla) Minecraft server. [This article](https://minecraft.gamepedia.com/Tutorials/Setting\_up\_a\_server) on the Minecraft Wiki is a good way to learn the basics of setting up a Minecraft server. There are also many guides available on YouTube.

A key difference between vanilla Minecraft and modded Minecraft is that you will need far more memory to host a server with Valhelsia than you normally do with a vanilla server. Please make sure your server has ample specs before continuing (usually 4-8GB), and please do not try to host a Valhelsia server on the same system that you intend to play the pack on.

## <mark style="color:orange;">Installing Java</mark>

Before you start, you will need to make sure you have the correct version of Java installed. One of the most common problems that people encounter when running a server is having 32-bit Java or having the incorrect version of Java for the given Minecraft version. All Valhelsia packs require 64-bit Java, and the specific version required is listed below.

### Windows

* Go to [Adoptium.net](https://adoptium.net).
* For **Minecraft 1.16** or earlier: Select **Temurin 8** (LTS) as the version.
* For **Minecraft 1.17** or later: Select **Temurin 17** (LTS) as the version.
* Select Latest release if you are downloading it from a 64-bit Windows computer.
* Otherwise, select Other platforms and change Operating System to Windows and Architecture to x64.

### Ubuntu or Debian Linux

* For **Minecraft 1.16** or earlier: Run this command from the command line: `sudo apt-get install openjdk-8-jre`.
* For **Minecraft 1.17** or later: Run this command from the command line: `sudo apt-get install openjdk-17-jre`.

Note that the package might have a different name depending on the version of the distribution you are running, so you should get familiar with the _apt_ command and how to manage packages on your system.

### Fedora, RHEL, or CentOS Linux

* For **Minecraft 1.16** or earlier: Run this command from the command line: `su -c "yum install java-1.8.0-openjdk"`
* For **Minecraft 1.17** or later: Run this command from the command line:&#x20;
  * `su -c "yum install java-1.17.0-openjdk"`

Note that the package might have a different name depending on the version of the distribution you are running, so you should get familiar with the _yum_ command and how to manage packages on your system.

### Mac

* Go to [Adoptium.net](https://adoptium.net).
* For **Minecraft 1.16** or earlier: Select **Temurin 8** (LTS) as the version.
* For **Minecraft 1.17** or later: Select **Temurin 17** (LTS) as the version.
* Select Latest release if you are downloading it from a 64-bit macOS computer.
* Otherwise, select Other platforms and change Operating System to macOS and Architecture to x64.

## <mark style="color:orange;">Downloading the Server Pack</mark>

Each of our packs has a Server Pack available on [CurseForge](https://www.curseforge.com/members/valhelsiateam/projects).

* From the [Valhelsia CurseForge page](https://www.curseforge.com/members/valhelsiateam/projects), select the modpack of choice.
* Select the Files tab near the top of the page.
* Scroll down to Additional Files and select the Download button next to the Server Pack to download the latest Server Pack.
* If you instead wish to use a different version, scroll down to Recent Files and select the version of choice, then follow the above step for that version.

## <mark style="color:orange;">First Time Setup</mark>

* Edit the amount of memory allocated to the server (see [Allocating Memory](allocating-memory.md#servers)). By default our scripts allocate the minimum amount required to run, but you should normally increase this if at all possible.
* Launch the server via ServerStart.bat (Windows) or ServerStart.sh (Linux / Mac OS X).
* After launching the server for the first time, it will close automatically and have created the file eula.txt.
* Open eula.txt, read and accept the [Minecraft EULA](https://account.mojang.com/documents/minecraft\_eula), then change `eula=false` to `eula=true` to accept the EULA.
* Launch the server once more. This will now create a number of files and folders, including _server.properties_ (note: some of our packs include a default _server.properties_ file, so you may already have it included in the server pack).
* Edit the _server.properties_ file to your liking.
  * In Valhelsia 2 and 3 you can change `level-type=default` to `level-type=biomesoplenty` to use [Biomes O' Plenty](https://www.curseforge.com/minecraft/mc-mods/biomes-o-plenty) world generation. Valhelsia 1 automatically uses Biomes O' Plenty world generation.
  * In Valhelsia 2 you can change `level-type=default` to `level-type=terraforged` to use [TerraForged](https://www.curseforge.com/minecraft/mc-mods/terraforged) world generation.
  * In Valhelsia 3 you can change `level-type=default` to `level-type=realistic` to use [Quark](https://www.curseforge.com/minecraft/mc-mods/quark)'s Realistic World Type. Note that this world type does not contain Biomes O' Plenty biomes by default, and requires some customisation to allow them to work that is beyond the scope of this page.
  * At the time of writing, Valhelsia: Enhanced Vanilla, Valhelsia Fabric and Valhelsia 4 only include the default vanilla Minecraft level types, so you can leave the level type as default or optionally set it to any vanilla level type if you wish.
  * You should always set `allow-flight=false` to `allow-flight=true` on modded Minecraft servers to prevent issues with some mods.
  * You can get an overview of the remaining server properties at the [Server.properties](https://minecraft.gamepedia.com/Server.properties) page of the Minecraft Wiki.
* After editing _server.properties_, you should delete the world folder to allow settings to take effect.
* Launch the server one last time.
* If you enabled the whitelist while editing _server.properties_, you should whitelist yourself via `/whitelist add YourPlayerName`.
* You may also wish to set yourself as a server operator via `/op YourPlayerName`.

## <mark style="color:orange;">Port Forwarding</mark>

If you want to allow access to the server from the Internet, you will need to enable port forwarding to the server from your router. [This article](https://minecraft.gamepedia.com/Tutorials/Setting\_up\_a\_server#Port\_forwarding) on the Minecraft Wiki is a good start for how to do so, but the exact method will vary depending on your router.

## <mark style="color:orange;">Pre-generating Chunks</mark>

It is a good idea to pre-generate chunks on any Minecraft server, but it is even more important in a big mod pack as a way to eliminate the lag caused by world generation by doing it in advance.

Forge includes built-in commands to handle this. The examples provided below generate 100,000 chunks in the overworld and 50,000 chunks each in The Nether and The End, in a spiral pattern around the coordinates \[0,0]. For reference, an area of 100k chunks is roughly a diameter of 360 chunks, or 5760 blocks. You may want to increase the numbers further depending on the area your players are likely to explore. You should wait until the first command completes entirely before running the next command in the sequence.

`/forge generate 0 0 0 100000 minecraft:overworld`

`/forge generate 0 0 0 50000 minecraft:the_nether`

`/forge generate 0 0 0 50000 minecraft:the_end`

Many of our modpacks also include custom dimensions, and you can change the dimension listed in the commands above to generate chunks in those dimensions as well.\
\
For [Valhelsia: Enhanced Vanilla](../../modpacks/valhelsia-enhanced-vanilla/) and [Valhelsia 5](../../modpacks/valhelsia-5/) you can use [Chunky Pregenerator](https://www.curseforge.com/minecraft/mc-mods/chunky-pregenerator), included in the modpack and server pack by default. For example, to generate 1000 blocks around the coordinates \[0,0] you need to run the following commands:\
\
`/chunky radius 1000`

`/chunky start`

## <mark style="color:orange;">Updating to a New Release</mark>

To update a server to a new release of Valhelsia, follow the following steps:

* Read the changelog for the new release. Some of them have extra steps or warnings that are typically important to be aware of.
* Download the new server pack.
* Stop the server (normally using `/stop` from the console).
* Make a backup of everything.
* Delete these folders (if they exist) from the old server: config, defaultconfigs, libraries, openloader, mods, kubejs, and scripts. Each Valhelsia pack contains slightly different folder configurations, so don't be alarmed if they don't exist for you.
* Delete the existing Forge jar file. The name of this file will vary depending on the release (and also varies for some hosting providers).
* Copy the contents of the new server pack over the existing folder.
* If you changed any of the configs, data packs, or scripts from the deleted folders, you should restore whatever files you modified.
* Launch the server again using the same method described in [First Time Setup](server-setup.md#first-time-setup).

## <mark style="color:orange;">Troubleshooting Lag</mark>

Firstly, please ensure that you are running the latest version of the pack before continuing. We regularly include new fixes to reported performance issues and often simply updating will be enough to help resolve lag. Next you should ensure that your server has enough memory allocated. Keep in mind that servers usually have far more chunks loaded than in single-player and so require more memory to run. This will increase further if you have a high number of players or have chunk-loaders.

Consider adding the [Dynamic View](https://www.curseforge.com/minecraft/mc-mods/dynamic-view) mod to servers (included by default in [Valhelsia 5](../../modpacks/valhelsia-5/)). It causes a lagging server to load fewer chunks around each player, and a server running well to load more chunks. This will naturally vary over time to try to achieve adequate performance.

If you still have lag after trying the above, you can track the cause of lag on a server by using one of the following tools:

* Minecraft's built-in debug profiler, detailed [on the Minecraft Wiki](https://minecraft.gamepedia.com/Commands/debug). It will generate a report that shows the percentage of tick time that each entity and block entity takes up.
* The [Spark mod](https://www.curseforge.com/minecraft/mc-mods/spark). Information about how to use it is available on their wiki, such as [this guide on finding the cause of lag spikes](https://github.com/lucko/spark/wiki/Finding-the-cause-of-lag-spikes). Spark is able to show information about CPU, memory, and disk usage on a server.

You will have to take different action depending on the source of the lag. Sometimes it will be immediately obvious, such as if a specific block or entity type takes up a significant portion of the tick time. If you don't know where on your server the relevant blocks / entities are, there is a useful mod called [TellMe](https://www.curseforge.com/minecraft/mc-mods/tellme) that can help. Please read through the mod description for how to use it. Of note is the `/tellme locate` command, which can search for things in any loaded chunks.

If you are unsure how to proceed, you are welcome to contact us at our [Discord server](https://valhelsia.net/discord). We will likely need to see the results of your troubleshooting, above, so please ensure that you have completed that step before asking.
