---
layout: post
status: publish
published: true
title: Build 39 Changelog
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 66
wordpress_url: http://vbitz.com/?p=66
date: 2012-11-17 13:03:24.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link</strong>:<a title="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_39.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_39.zip"> http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_39.zip</a>

<strong>Changes</strong>
<ul>
	<li>Command now runs from playerapi on the player specified</li>
	<li>Added world().getBiome(vector3f pos) which returns the name of the biome in pos</li>
	<li>Added world().spawn(vector3f pos, string name) Spawns mob name at pos</li>
	<li>Added world().grow(vector3f pos) Uses bonemeal at pos</li>
	<li>Added difficulty(string level) which changes the current difficulty</li>
	<li>MinecraftScript now no longer requires the client though stick and scripted blocks will be disabled unless the clientside is enabled which can be done with a config option.</li>
</ul>
