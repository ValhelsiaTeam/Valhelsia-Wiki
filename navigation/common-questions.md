---
description: Frequently asked questions for Valhelsia projects.
---

# Common Questions

If you can't find an answer to your question here, please also look at the [Knowledge Base](knowledgebase/). It covers many things in much more depth than here - there are articles on several commonly asked questions and subjects.

In addition, please check the pinned messages in the support channels on the Valhelsia [Discord server](https://valhelsia.net/discord) to see if your problem is mentioned there. We frequently cover temporary issues that apply only to specific versions of packs in the pinned messages there.

## <mark style="color:orange;">General FAQ</mark>

**Q: Which modpack should I play?**\
**A:** If you're unsure which Valhelsia pack to play, try [Valhelsia 3](https://www.curseforge.com/minecraft/modpacks/valhelsia-3) first. It has the broadest range of available mods and has long term support, even as newer packs are being developed. It also has decent performance on most computers (if following the tips from the [Performance Tweaks](knowledgebase/performance-tweaks.md) page).

Want to try something different? [Valhelsia: Enhanced Vanilla](https://www.curseforge.com/minecraft/modpacks/valhelsia-enhanced-vanilla) may be for you instead!\


**Q: I get a message about insufficient allocated RAM, or the game has performance issues, how do I fix this?**\
**A:** The most common reason for the pack taking a long time to load in or create a new world is that inadequate memory is allocated. You can see the minimum memory requirement on the CurseForge page for the pack you're using. See [Allocating Memory](knowledgebase/allocating-memory.md) for instructions on how to adjust the amount of memory allocated to Java.\


**Q: Open to LAN isn't working, how can I get it to work?**\
**A:** In general, open to LAN is not a well supported feature in modded minecraft. Most mod developers seemingly don't test it, and it is otherwise quite problematic. While it may work in some modpacks and at some times, it can break at any time with any mod change in any update. Therefore we're unable to support it as a multiplayer option. As an alternative, you can run a server locally (free), on a cloud/virtual server ([free option](https://blogs.oracle.com/developers/post/how-to-set-up-and-run-a-really-powerful-free-minecraft-server-in-the-cloud)), or via a paid hosting service. [BisectHosting](https://bisecthosting.com/Valhelsia) is Valhelsia's official hosting partner. Using the promo code "**Valhelsia**" to get **25%** off your first month as a new client for any of their gaming servers.\


**Q: I'm trying to run a server but it crashes immediately, how do I fix this?**\
**A:** One of the most common problems is using the wrong version of Java for the pack you're trying to run. All Valhelsia packs require 64-bit Java. Minecraft 1.16 and earlier (such as Valhelsia 3) requires Java 8, and Minecraft 1.17 and later (such as Valhelsia: Enhanced Vanilla) requires Java 17. You can [download it from here](https://adoptium.net/) - Temurin 8 is the same as Java 8, and Temurin 17 is the same as Java 17.\
\
Note that most modern Linux systems include OpenJDK by default but may not necessarily have the correct version. Type `java --version` in a Terminal to check.\
\
Please also see the [Server Setup](knowledgebase/server-setup.md) guide as it contains more information.\


**Q: How do I get my server listed in #servers forum on the** [**Valhelsia Discord**](https://valhelsia.net/discord) **server?**\
**A:** You can publish your advertise by yourself, you just have to select the tags and put some important information about your server.\
\
Many people also choose to advertise their Valhelsia servers on Reddit here: [https://www.reddit.com/r/feedthebeastservers/](https://www.reddit.com/r/feedthebeastservers/) (which, despite the name, isn't just for FTB servers), or on the [Valhelsia subreddit](https://www.reddit.com/r/Valhelsia/).

## <mark style="color:orange;">Advanced Users FAQ</mark>

Note: This FAQ is intended for advanced users only who already know their way around Minecraft mod packs and are familiar with adjusting launcher settings.

**Q: Are there any JVM flags that can help pack performance?**\
**A:** Please refer to [this excellent guide](https://aikar.co/mcflags.html) by Aikar, which includes highly optimised JVM parameters, and explains it far better than we could. These are designed with servers in mind, but should still work reasonably well for clients too.

## <mark style="color:orange;">Gameplay FAQ</mark>

### Valhelsia 5

**Q: Does Valhelsia 5 have Vein Miner or Ore Excavation?**\
**A:** No, but there are tools available with vein mining options, such as the Meka-Tool from Mekanism. For tree felling, there is the Terra Truncator from Botania and the Buzzsaw from Immersive Engineering.&#x20;

There are also many tools with AoE (area of effect) capabilities, such as the following:

* Terra Shatterer (Botania)
* Excavating Enchant (Ensorcellation - can be applied to any pickaxe)

This isn't an exhaustive list by any means - you'll often discover more useful tools while progressing through various mods.



**Q: Are there any Chunk Loaders in Valhelsia 5?**\
**A:** Yes, Valhelsia 5 includes the [Open Parties and Claims](https://www.curseforge.com/minecraft/mc-mods/open-parties-and-claims) mod, this one gives you the ability to claim and to forceload world chunks.

### Valhelsia 3

**Q: Does Valhelsia 3 have Vein Miner or Ore Excavation?**\
**A:** No, but there are tools available with vein mining options, such as the Meka-Tool from Mekanism. For tree felling, there is the Terra Truncator from Botania and the Buzzsaw from Immersive Engineering.&#x20;

There are also many tools with AoE (area of effect) capabilities, such as the following:

* Cthonic Extractor (Tetra)
* Terra Shatterer (Botania)
* Infinity Drill (Industrial Foregoing)
* Mining Drill (Immersive Engineering)
* Excavating Enchant (Ensorcellation - can be applied to any pickaxe)

This isn't an exhaustive list by any means - you'll often discover more useful tools while progressing through various mods.\


**Q: Are there any Builder's Wands in Valhelsia 3?**\
**A:** Yes. The Building Gadget (from the Building Gadgets mod) as well as the Formation Wand from Astral Sorcery.\


**Q: Are there any Chunk Loaders in Valhelsia 3?**\
**A:** Yes, Valhelsia 3 includes the [Chunk Loaders](https://www.curseforge.com/minecraft/mc-mods/chunk-loaders) mod.\


**Q: Can you move spawners in Valhelsia 3? And how?**\
**A:** There are several methods: (1) You can pick up a spawner with both of your hands empty by crouching and right-clicking, (2) by using a cardboard box from Mekanism (requires sawdust), or (3) by using a pickaxe enchanted with Silk Touch. There are other methods but these are the easiest.\


**Q: Can you store Experience (XP) in Valhelsia 3?**\
**A:** Yes.&#x20;

One method is via the Supplementaries mod - you can shift-right-click with a Glass Bottle on an Enchanting Table to convert some XP and Health into a Bottle o' Enchanting. You can use Bottles o' Enchanting on a Jar (also from the Supplementaries mod) to store it for later use, and can extract it via the Faucet or Glass Bottles.

Another method is via the Tome of Peritia from Blood Magic. Instructions for how to use it can be found in the Sanguine Scientiem (Blood Magic's Instruction Manual).

Industrial Foregoing also provides several machines that use Essence instead of XP to work with enchantments. See Industrial Foregoing's Manual (included in the starting Akashic Tome) for information on these machines.
