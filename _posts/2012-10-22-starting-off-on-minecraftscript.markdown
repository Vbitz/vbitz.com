---
layout: post
status: publish
published: true
title: Starting off on MinecraftScript
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 15
wordpress_url: http://vbitz.com/?p=15
date: 2012-10-22 16:05:51.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
Scripting is a wonderful thing and as I recently discovered it's really easy to add JavaScript based scripting to any java program using

<a title="http://docs.oracle.com/javase/6/docs/technotes/guides/scripting/programmer_guide/index.html" href="http://docs.oracle.com/javase/6/docs/technotes/guides/scripting/programmer_guide/index.html" target="_blank">http://docs.oracle.com/javase/6/docs/technotes/guides/scripting/programmer_guide/index.html</a>.

As a big Minecraft fan myself I wondered what can do with this in Minecraft, as it turns out a lot. In less then a hour of coding using <a title="http://www.minecraftforge.net/forum/" href="http://www.minecraftforge.net/forum/" target="_blank">Minecraft Forge</a> I was able write a basic script loader for minecraft and use very low level basic scripting to add a new block. With JavaScript it took about 8 lines to add a new block.

<pre>nmc = net.minecraft.src;
fmlCommon = Packages.cpw.mods.fml.common;
var i = new nmc.Block(3000, nmc.Material.grass);
i.setCreativeTab(nmc.CreativeTabs.tabBlock);
fmlCommon.registry.GameRegistry.registerBlock(i);
fmlCommon.registry.LanguageRegistry.addName(i, "Hello World");</pre>

That code is really messy. The Java scripting engine basically allows you to import Java classes into JavaScript and call them as if your using Java. When it comes to Minecraft and Minecraft Forge this has quite a few limitations.
<ul>
	<li>You need to load the blocks as Minecraft starts.</li>
	<li>You need a free block id.</li>
	<li>Since Java's scripting engine does not allow the creation of extended classes and only allows implementing interfaces you can't create a block more complex then a new kind of Glowstone or wool or Obsidian</li>
</ul>
This is where a API could come in. To fix the issue of loading blocks at startup you can register a block of template classes for javascript to fill in using a API. That also fixes the other 2 problems.

In the end all you really need to script Minecraft is a good quality API. I will hopefully make more posts in the future showing my progress on this project but for now there's already a Github repo <a title="https://github.com/Vbitz/MinecraftScript" href="https://github.com/Vbitz/MinecraftScript" target="_blank">Vbitz/MinecraftScript</a>
