---
title: "PCSX2 : A PS2 Emulator"
date: 2022-04-08
tags: ["retro-gaming","tutorial"]
weight: 3
---

<div align="center">
	<img src="/images/PS2Tutorial/logo.PNG" width="50%">
</div>

##### Table of contents
- [Introduction](#introduction)
- [Minimum requirements](#mr)
- [Prerequisites](#pr)
	- [Dumping your BIOS](#bios)
	- [Download your BUIS](#bios2)
	- [PS2 ROM](#ROM)
- [Installing PCSX2](#ipcsx)
- [Configuration](#conf)
	- [Controller](#cont)
	- [Emulation settings](#emu)
	- [Graphics settings](#gset)
- [Loading your game](#game)
- [Conclusion](#concl)
- [Sources](#src)


##### Introduction <a name="introduction"></a>

Have you ever wanted to play some sweet classics such as "Jak X : Combat Racing" or "Ratchet and Clank" 
but find yourself stuck because it's a Playstation 2 exclusive title and you don't have the hardware or 
think that the PS2 in itself is not convenient? Well, there's a way !

Here we'll discuss about [PCSX2](https://pcsx2.net/), an open-source software that let you play PS2 games
 on your computer. Before installing, let's talk about the prerequisites.

##### Minimum requirements <a name="mr"></a>

**Operating system** : Windows 8.1 or highter / Ubuntu 18.04 or higher 

**CPU** : SSE4.1 support -> anything above the Silvermont micro-architecture for
 Intel and K10-based micro-architecture for AMD

**Memory** : 4 GB RAM

**Graphics hardware** : Anything DX10 or OpenGL 3.x capable with at least 2GB VRAM



##### Prerequisites <a name="pr"></a>

You'll will need two things before installing the emulator. 

- BIOS file
- PS2 ROM

The BIOS is required to start the emulator and to play games.The BIOS version need to match the game version
 due to <a href="https://en.wikipedia.org/wiki/Regional_lockout" target="_blank">regional lockout</a>, for
example you will need a PAL BIOS for European copies and NTSC BIOS for American copies.
There are two ways of obtaining a BIOS:
- Dumping your BIOS - 😇
- Downloading it - 😈

###### Dumping your BIOS <a name="bios"></a>

Dumping your PS2 bios seems like a tedious process reserved for tech savvy people but it's really not. There
 are many ways to achieve it : 
- Using a FMCB Memory card (purchasable 
<a href="https://www.amazon.com/RGEEK-FreeMcBoot-1-953-Memory-Playstation/dp/B07PB2DYTT" target="_blank">here</a>)
- Using Swap Magic disks (the method I personally used, disk purchasable 
<a href="https://www.amazon.com/Swap-Magic-CODER-Keys-swapmagic-es/dp/B01J4KDK0S/ref=sr_1_2?keywords=Ps2+Swap+Magic&qid=1649207125&s=videogames&sr=1-2" target="_blank">here</a>)
- FreeDVDBoot
- Mod-chipping (I don't have any experience in soldering)

Here's a great video explaining the process of dumping your BIOS using Swap Magic by FrozenFoxy :

<iframe align="center" width="100%" height="320" src="https://www.youtube.com/embed/QM6nT6zoOEw" title="YouTube video player" 
frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

###### Downloading your BIOS <a name="bios2"></a>

When it comes to downloading BIOS from the Internet, it is illegal since the BIOS is an intellectual property that belongs to Sony. Realistically, you can easily find  all the PS2 BIOS on the internet distributed by websites or cloud platforms. Act at your own risk.

###### PS2 ROM <a name="ROM"></a>

Obviously, you'll also need games to play. Depending on your country legislation, you can or cannot make a copy of
your PS2 game if it is for personal use. If you don't want to deal with the hassle of copying your game , there's a way to play PS2 CD's directly from your computer disk reader.

Assuming that you want to make a copy of your game so you don't have to constantly put your game on the disk reader, you have to use a disk burner software such as <a href="https://ninite.com/imgburn/" target="_blank">ImgBurn</a>.

I'd like to add that while PCSX2 support 98 % of the PS2 library, there are some unlucky foes that won't be playable. To check
the games that are not playable, click <a href="https://pcsx2.net/compat/" target="_blank">here</a>.

##### Installing PCSX2 <a name="ipcsx"></a>

The first step is to download PCSX2 <a href="https://pcsx2.net/downloads/" target="_blank">here</a>. I advise you to download the latest stable release which is, to this day, the 1.6.0 version. 

If you are on Windows, you would download the PCSX2 setup executable. Once it's launched follow these steps.

- Select the Normal Installation

<div align="center">
	<img src="/images/PS2Tutorial/1.PNG" width="50%">
</div>

- Select your language

<div align="center">
	<img src="/images/PS2Tutorial/2.PNG" width="50%">
</div>
	
- Let all the defaults plugins

<div align="center">
	<img src="/images/PS2Tutorial/3.PNG" width="50%">
</div>

- Select your PS2 BIOS

<div align="center">
	<img src="/images/PS2Tutorial/4.PNG" width="50%">
</div>



After all these steps, you'll have a working PS2 with no controls nor game. To check if the PS2 BIOS is good, boot
the PS2 by first pressing on CDVD > No disc then click on System > Boot BIOS

<div align="center">
	<img src="/images/PS2Tutorial/5.PNG" width="50%">
</div>



If the emulators boots up, hurray ! All is working as intended.

<div align="center">
	<img src="/images/PS2Tutorial/6.PNG" width="50%">
</div>

##### Configuration <a name="conf"></a>

###### Controller <a name="cont"></a>

Now that the emulator is working, you need to map your controller (or keyboard) by using the LilyPad plugin.
To access the settings of the plugin, you have to go to Config > Controllers > Plugin Settings.

Once the LilyPad settings open, click on "Pad 1A" beside the general tab and map your controller. You
can use the quick setup method to quickly configure your controller. Once it's done, apply the settings.

<div align="center">
	<img src="/images/PS2Tutorial/7.PNG" width="50%">
</div>

###### Emulation settings <a name="emu"></a>

Now we'll go over the emulation settings, you'll need to change couples of things in order to make the gaming experience as smooth 
as possible. To achieve that, you'll need 
to go over Config > Emulations Settings > Speedhacks

<div align="center">
	<img src="/images/PS2Tutorial/8.PNG" width="50%">
</div>

When you're here, activate MTVU (if your CPU has more than 3 cores). There's a little slider on the bottom, set it to balanced and apply
 the settings. You might want to set the slider to agressive mode if your CPU is underperforming.

<div align="center">
	<img src="/images/PS2Tutorial/9.PNG" width="50%">
</div>

If you face any instability when playing a certain game (frame drop, weird textures), I advise you to do these two things in this order.
 First, modify the preset level to a less agressive level. If it's not helping, then disable MTVU as last resort.

###### Graphics settings <a name="gset"></a>

Now, we want to tweak the graphics settings. Everyone doesn't have the same PC componants so it is really important to adapt your 
settings depending of your PC capacitiy. 

Here's a list of configurations for all types of computers : 

- You have a low end pc, I suggest you to watch <a href="https://youtu.be/NR-zydADlKM" target="_blank">this video </a>
- You have an average pc, check <a href="https://www.youtube.com/watch?v=SLTK_5A5o6c" target="_blank">this video</a>  out
- You have a high endpc, have a look at <a href="https://youtu.be/3rSiK2aO_5k?t=418" target="_blank">this video </a>

###### Loading your game <a name="game"></a>

Loading your game is easy as ABC, open PCSX2 and click on CDVD. Now choose the source of your ISO (HDD, diskreader) and it's done ! 
You're playing PS2 game on your computer, brilliant isn't it?

<div align="center">
	<img src="/images/PS2Tutorial/10.PNG" width="50%">
</div>

###### Conclusion <a name="concl"></a>

There's nothing that replaces the authentic feeling of turning on a real Playstation 2, but the comfort of being able to play 
on your setup is always appreciated. I hope this article has guided you through the installation of the emulator.

###### Sources <a name="src"></a>

PCSX2 Wikipedia page on <a href="https://en.wikipedia.org/wiki/PCSX2#Hardware_requirements" target="_blank">hardware requirements</a>, consulted the 8th Arpil 2022

