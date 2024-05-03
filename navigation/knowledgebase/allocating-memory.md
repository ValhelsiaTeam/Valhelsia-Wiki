---
description: How to allocate memory in Valhelsia modpacks.
---

# Allocating Memory

When running Valhelsia packs, you will need to set the amount of allocated memory (RAM) for Java to use.

The method to adjust allocated memory varies depending on the program that you are using to run the pack. Instructions for the most popular programs can be found below.

The amount of memory that should be allocated for Valhelsia packs is shown in the table below, but optimal amounts may vary depending on the total memory that is installed in your system, and you may find that setting the memory higher or lower works better for you.

<table><thead><tr><th width="194.83433552514745">Pack</th><th width="160.68456375838926">Minimum</th><th width="153.92951823166118">Recommended</th><th>Recommended (HD*)</th></tr></thead><tbody><tr><td>Valhelsia 6 (1.20)</td><td>4 GB (4096 MB)</td><td>5 GB (5120 MB)</td><td>5 GB (5120 MB)</td></tr><tr><td>Valhelsia 5 (1.19)</td><td>4 GB (4096 MB)</td><td>5 GB (5120 MB)</td><td>6 GB (6144 MB)</td></tr><tr><td>Valhelsia: Volatile</td><td>4 GB (4096 MB)</td><td>5 GB (5120 MB)</td><td>5 GB (5120 MB)</td></tr><tr><td>Valhelsia: Enhanced Vanilla</td><td>4 GB (4096 MB)</td><td>5 GB (5120 MB)</td><td>5 GB (5120 MB)</td></tr><tr><td>Valhelsia 3 (1.16)</td><td>4 GB (4096 MB)</td><td>6 GB (6144 MB)</td><td>8 GB (8192 MB)</td></tr><tr><td>Valhelsia: Origins (1.15)</td><td>4 GB (4096 MB)</td><td>5 GB (5120 MB)</td><td>8 GB (8192 MB)</td></tr><tr><td>Valhelsia 2 (1.15)</td><td>5 GB (5120 MB)</td><td>6 GB (6144 MB)</td><td>8 GB (8192 MB)</td></tr><tr><td>Valhelsia 1 (1.14)</td><td>5 GB (5120 MB)</td><td>6 GB (6144 MB)</td><td>8 GB (8192 MB)</td></tr></tbody></table>

\* Recommended for use with HD Resource Packs or Shader Packs.

## <mark style="color:orange;">CurseForge Client</mark>

:inbox\_tray: [CurseForge Download](https://curseforge.overwolf.com/)

**Method 1: Changing the default Allocated Memory for Minecraft mod packs.**

This method will change the default allocated memory for all packs that you install, excluding ones that altered the allocated memory using Method 2, below.

1. Click the settings icon in the lower-left corner of the CurseForge window.
2. Select Minecraft under the Game-Specific section.
3. Scroll down to Java Settings.
4. Adjust the slider under Allocated Memory to suit.

**Method 2: Changing the Allocated Memory for one specific pack.**

1. Make sure you are on the My Modpacks section of the CurseForge client.
2. Select the pack you wish to edit.
3. In the upper-right of the window, select the Menu icon (three stacked dots) next to the Play button.
4. Select Profile Options.
5. Uncheck Use System Memory Settings then adjust the slider to suit.
6. Click Done in the lower-right corner.

## <mark style="color:orange;">GDLauncher</mark>

:inbox\_tray: [GDLauncher Download](https://gdevs.io/#downloadContainer)

**Changing the Allocated Memory for one specific pack.**

1. Right-click on the pack, then select Manage.
2. Select Override Java Memory.
3. Adjust the slider to suit.
4. Click the cross in the upper-right corner. Settings will be automatically saved.

## <mark style="color:orange;">MultiMC</mark>

:inbox\_tray: [MultiMC Download](https://multimc.org/#Download)

**Changing the Allocated Memory for one specific pack.**

1. Right-click on the pack, then select Edit Instance.
2. Select the Settings tab on the left.
3. Tick the Memory checkbox.
4. Enter the amount of memory to allocate in the Minimum memory allocation and Maximum memory allocation boxes, in megabytes (MB).
   * Note: Minecraft generally functions best when the minimum and maximum memory are set to the same value.
5. Click Close in the lower-right.

## <mark style="color:orange;">Twitch Client</mark>

{% hint style="danger" %}
The Twitch client **no longer supports Minecraft mods** as of December 2020. It has been officially replaced with the Overwolf CurseForge client, which is currently in beta. Please switch to one of the above launchers instead.
{% endhint %}

## <mark style="color:orange;">Servers</mark>

If you are using a Valhelsia Server Pack, you can edit either ServerStart.bat (Windows) or ServerStart.sh (Linux or Mac) to adjust the amount of RAM dedicated to a server. Near the top of the file is a line including the text `ALLOCATED_RAM`- change the value here to the amount you wish to allocate.

If you are using a hosting provider instead of the Server Pack download, the method will vary depending on which hosting provider you use, and you may need to contact them to change it.
