---
description: >-
  Information regarding OptiFine (and equivalent) & Shader Pack installation for
  Valhelsia packs.
---

# OptiFine

OptiFine is a mod for Minecraft clients intended to add a number of new graphics options to the game as well as add support for shader packs. In some cases it can also increase performance considerably, although this will vary depending on your hardware. We generally find that adding OptiFine results in higher memory usage but lower CPU and GPU usage.

Other equivalent mods to OptiFine are now available as for example [Iris Shaders](https://www.curseforge.com/minecraft/mc-mods/irisshaders/files) available only on Fabric. But there is now a fork of Iris Shaders which is called [Oculus](https://www.curseforge.com/minecraft/mc-mods/oculus) and available on Forge (require [Rubidium](https://www.curseforge.com/minecraft/mc-mods/rubidium)).

The version of OptiFine or Oculus supported for the latest version of the pack is listed in the table below. If you are instead using an older version of one of our packs, you can find the compatible version listed in the #changelog channel of our [Discord server](https://valhelsia.net/discord).

{% hint style="info" %}
&#x20;[Valhelsia: Enhanced Vanilla](../../modpacks/valhelsia-enhanced-vanilla/), [Valhelsia 5](../../modpacks/valhelsia-5/) and [Valhelsia 6](../../modpacks/valhelsia-6/) is provided with shaders, performance mods, and resource packs. OptiFine is not compatible with these mods, so can't be included in the pack (and serves no purpose due to the replacement mods).
{% endhint %}

<table><thead><tr><th width="193">Pack</th><th width="133">Pack Version</th><th width="222">OptiFine</th><th>Oculus</th></tr></thead><tbody><tr><td>Valhelsia: Volatile (1.19)</td><td>2.0.3</td><td>Not compatible.</td><td>Unknown.</td></tr><tr><td>Valhelsia 3 (1.16)</td><td>3.5.1</td><td><a href="https://optifine.net/downloads">OptiFine 1.16.5 HD U G8</a>¹</td><td>Unknown.</td></tr><tr><td>Valhelsia: Origins (1.15)</td><td>1.1.5</td><td><a href="https://optifine.net/downloads">OptiFine 1.15.2 HD U G6</a></td><td>Unknown.</td></tr><tr><td>Valhelsia 2 (1.15)</td><td>2.3.4</td><td><a href="https://optifine.net/downloads">OptiFine 1.15.2 HD U G6</a></td><td>Unknown.</td></tr><tr><td>Valhelsia 1 (1.14)</td><td>1.2.2</td><td><a href="https://optifine.net/downloads">OptiFine 1.14.4 HD U G5</a></td><td>Unknown.</td></tr></tbody></table>

¹ Note that some people have had more success with OptiFine 1.16.5 HD U G7 instead of G8. Please try downgrading to G7 if you experience any issues.

## <mark style="color:orange;">Installing OptiFine</mark>

You can add it to the pack by downloading the correct version of OptiFine and placing the .jar file in the mods folder alongside other mods. OptiForge is installed using the same method.

{% hint style="info" %}
OptiFine should never be added to a server (and will indeed crash the server). It is a client-side mod only.
{% endhint %}

Depending on the launcher you are using, there will be a different method to find the mods folder.

### CurseForge Client & GDLauncher

1. Right-click on the pack instance, then select Open Folder.
2. Double-click on the _mods_ folder, and drop in the downloaded OptiFine  .jar. You do not need run it - it functions as a mod.

## <mark style="color:orange;">OptiForge</mark>

[OptiForge](https://www.curseforge.com/minecraft/mc-mods/optiforge) is a mod that aims to fix some incompatibilities between OptiFine and Minecraft Forge in Minecraft 1.17 and earlier. It is generally not required in the most recent versions of our packs, but may be required for some older versions (or may resolve certain glitches or crashes).&#x20;

If you're encountering issues with OptiFine, consider adding the [OptiForge ](https://www.curseforge.com/minecraft/mc-mods/optiforge)mod (in the same way as described [above](optifine.md#installing-optifine)). Please see the OptiForge changelog to ensure you have the correct version for the OptiFine and Forge versions of the pack.

## <mark style="color:orange;">Installing Oculus</mark>

You can add it to the pack by downloading the correct version of Oculus and placing the .jar file in the mods folder alongside other mods. Oculus needs the Rubidium mod to work, installed using the same method.

{% hint style="info" %}
Oculus should never be added to a server (and will indeed crash the server). It is a client-side mod only.
{% endhint %}

Depending on the launcher you are using, there will be a different method to find the mods folder.

### CurseForge Client & GDLauncher

1. Right-click on the pack instance, then select Open Folder.
2. Double-click on the _mods_ folder, and drop in the downloaded Oculus  .jar. You do not need run it - it functions as a mod.

## <mark style="color:orange;">Installing Shader Packs</mark>

Note: Shader packs should be switched before loading a Minecraft world or connecting to a multiplayer server, from the title screen.

1. From the Valhelsia Title Screen, click on _Options_, then _Video Settings_, then _Shaders_, then click the _Shaders Folder_ button at the bottom.
2. Download the shader pack you wish to use. We have included links to several shader packs below, but this is by no means an exhaustive list.
3. Place the downloaded shader pack in the newly opened window showing the _shaderpacks_ folder.
4. Select the shader pack from the list in the in-game menu.

{% hint style="warning" %}
Enabling a shader pack in Valhelsia 3 may crash the game due to an incompatibility between OptiFine and Immersive Engineering. This will typically only happen once, and reloading the game should load the shader normally. This is a bug in OptiFine that we are unable to fix.
{% endhint %}

### Sildur's Shaders

Sildur's shaders come in a variety of levels - Lite, Medium, High, High w/ Motion Blur, Extreme, and Extreme w/ Volumetric Lighting. The range of packs available ensure that there's something for everybody. We use the Extreme w/ Volumetric Lighting pack to create the screenshots that you see on the Valhelsia 3 CurseForge page, as these shaders are particularly suited for breathtaking screenshots of your creations.

{% hint style="info" %}
To remove the horizontal line in the skybox you have to disable Astral Sorcery's custom skybox, by removing "minecraft:overworld" from skyRenderingEnabled at astralsorcery-client.toml in the config directory. There is more information about this pinned in the #support channel of our Discord server.
{% endhint %}

{% embed url="https://sildurs-shaders.github.io/" %}
Link to their website.
{% endembed %}

### BSL Shaders

BSL Shaders are great for survival Minecraft, with a focus on optimisation and customisation. They achieve a balance between looking good, performing well, and having subtle effects that don't detract from playing the game.

{% embed url="https://bitslablab.com/bslshaders/" %}
Link to their website.
{% endembed %}

### Complementary Shaders

Complementary Shaders were originally based on BSL Shaders, but the developer has shifted focus towards compatibility with as many different hardware and mod configurations as possible, and has deviated considerably from the starting point of BSL shaders, resulting in quite a different end result.

{% embed url="https://www.complementary.dev/" %}
Link to their website.
{% endembed %}

## <mark style="color:orange;">Warnings / Disclaimer</mark>

Most mod developers will not guarantee OptiFine or Oculus support since OptiFine changes a lot of expected Minecraft functionality and is additionally not an open source mod, causing it to be more difficult to achieve compatibility with. Many developers will avoid fixing problems that only occur with OptiFine installed and will close issue reports that include OptiFine. Because of this, you may experience missing textures or models, crashes, visual glitches, or negative performance while using OptiFine. While we have included the installation steps here and we will attempt to help you, we promise no support beyond this wiki page because of this. If you are seeking support on our [Discord server](https://valhelsia.net/discord) for help with a crash or bug, please remove OptiFine (and OptiForge, if added) before asking for help and submitting a crash report.
