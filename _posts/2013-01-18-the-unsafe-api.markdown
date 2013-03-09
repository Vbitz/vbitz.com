---
layout: post
status: publish
published: true
title: The Unsafe API
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 92
wordpress_url: http://vbitz.com/?p=92
date: 2013-01-18 00:52:03.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
This is one of the biggest addition's I've made to the mod in quite a while and like the /js command before it it changes the direction of the mod somewhat. In this case it splits off a more advanced API for experienced coders to invoke code without the sandbox imposed by MinecraftScript.

The Unsafe API is on the surface quite a simple system, I disable the class shutter (what stops you from running vanilla minecraft code) and give access to internal Minecraft objects (like the current world and the player). This is exposed with a new config setting that when enabled prints a warning on startup. Also it adds some helpers to make moving around the minecraft codebase easier, a listing of mods and the ability to fetch a mod's main class. A helper to access the TileEntity or class of a block and some methods that will allow you to call and modify any variable.

This is really useful while I'm developing in MCP and though it works wonders outside of it (most mods aren't obfuscated) it still needs real class mappings to be of any use.

I initially planed to do this by parsing the MCP configs if you have them on hand (I'm not going to distribute them on my own) but as they follow a different naming scheme for methods that won't work.

Another way of doing it will be to generate a class file that registers all the bindings, this will be generated in such a way as method names and class names will be there MCP equivalents. The only issue if I choose to go with this method is I don't feel comfortable coping such a large part of the work from MCP (It's not really allowed either).

If I get permission to do so then I will but until this I may just write a utility that generates it off a existing MCP install, this utility will be on the main repo but will not be supported or provided in the downloads.

<strong>On a really positive note </strong>I have tested MinecraftScript on a otherwise normal FTB Install (The Direwolf20 Pack, the Mindcrack pack would work fine) with a config disabling the client-side so I don't register any block ID's and unsafe mode enabled. Some of the things I was able to do were quite interesting...
<ul>
	<li>Change the amount of energy in a ThermalExpansion Redstone Energy Cell.</li>
	<li>Doing the same thing with a MFSU (and any energy storage block) from IC2.</li>
	<li>Reading and Writing from the memory of a RP2 Computer.</li>
	<li>Printing text to the display of a ComputerCraft and RP2 Screen.</li>
	<li>Changing CPU registers on a RP2 Computer.</li>
	<li>Causing a meltdown of a IC2 Reactor (much easier then I expected).</li>
	<li>Electrocuting myself with a unconnected tesla coil from IC2</li>
	<li><strong>Corrupting</strong> a world after messing with a Buildcraft Quarry</li>
</ul>
Injecting items into a BuildCraft pipe, this one requires a little more explanation, messing with machines is one thing but pipe networks are a lot more complex. Since BuildCraft is open-source I was able to trace it through the source-code and found out how after binding another vanilla function to the Unsafe API.

In all a very productive day.
