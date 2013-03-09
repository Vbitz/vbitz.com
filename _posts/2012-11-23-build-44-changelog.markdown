---
layout: post
status: publish
published: true
title: Build 44 Changelog
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 73
wordpress_url: http://vbitz.com/?p=73
date: 2012-11-23 10:33:32.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link</strong>: <a title="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_44.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_44.zip" target="_blank">http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_44.zip</a>

<strong>RegisterTick</strong>

I've been working over the issue of giving people access to ticks for a long time now and I finally have a way of doing it that will produce less lag then just hooking javascript functions right on tick. The downside is not all functions will run each frame although there is a (right now) hardcoded value that will allow server owners to run more functions each frame.

<strong>Changes</strong>
<ul>
	<li>JavaScript can now run code during ticks using registerTick(string id, Function func)</li>
</ul>
