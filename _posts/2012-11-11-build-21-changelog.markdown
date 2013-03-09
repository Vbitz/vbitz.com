---
layout: post
status: publish
published: true
title: Build 21 Changelog
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 42
wordpress_url: http://vbitz.com/?p=42
date: 2012-11-11 15:37:25.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link: </strong><a title="http://vbitz.com/minecraftscript/MinecraftScript_21.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_21.zip" target="_blank">http://vbitz.com/minecraftscript/MinecraftScript_21.zip</a>

<strong>Changes</strong>:
<ul>
	<li>Added get and set Hunger commands as part of the Player API</li>
	<li>Added playerapi.getPlayerLook() which returns a vector containing the point the player is looking at, If that point is invalid (off the world) then it returns the player's current position.</li>
	<li>Added playerapi.tpv(Vector3f vec) which is a version of tp which takes a vector</li>
	<li>Added JS Stick. You can now run /jss js-string to put a stick in your inventory which runs js-string on right click. A good example of this is /jss me().tpv(me().getPlayerLook().add(0, 2, 0)) Which makes a blinking spell.</li>
</ul>
