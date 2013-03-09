---
layout: post
status: publish
published: true
title: Build 26 Changelog
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 51
wordpress_url: http://vbitz.com/?p=51
date: 2012-11-14 10:52:33.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link</strong>: <a title="http://vbitz.com/minecraftscript/MinecraftScript_26.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_26.zip" target="_blank">http://vbitz.com/minecraftscript/MinecraftScript_26.zip</a>

<strong>Changes</strong>
<ul>
	<li>Added world() which returns the current world</li>
	<li>Added vector(double x, double y, double z) which returns a new vector</li>
	<li>Refactored functions so all now take a vector rather then a x, y, z</li>
	<li>Added world().downfall(bool rain, int time) which turns on and off the rain</li>
	<li>Changed player.getLoc() to player.pos()</li>
	<li>Fixed world().explode(int size, vector point)</li>
	<li>Added world().killDrops() which removes all item drops in a 100 block radius of the player</li>
</ul>
