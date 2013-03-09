---
layout: post
status: publish
published: true
title: Well That's more like it
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 19
wordpress_url: http://vbitz.com/?p=19
date: 2012-10-22 21:09:09.000000000 +13:00
categories:
- Uncategorized
tags:
- MinecraftScript
comments: []
---
<pre>var blk = api.getScriptedBlock(1);
blk.setBlockBrightness(0.8);
blk.setBlockCreativeTab("blocks");
blk.setBlockTexture("tntTop");</pre>
I've been working on more scripting for MinecraftScript. This is a lot more concise and easier to understand then working straight with Minecraft's code.

One thing you might notice if your ever worked with Minecraft modding is when I set the texture of the block I use a string rather then a index. These correlate directly to terrain.png and are just stored inside of a HashMap. If you want to look at the whole file for some reason you can find it <a title="https://github.com/Vbitz/MinecraftScript/blob/master/src/common/com/vbitz/MinecraftScript/ScriptedBlock.java" href="https://github.com/Vbitz/MinecraftScript/blob/master/src/common/com/vbitz/MinecraftScript/ScriptedBlock.java" target="_blank">here</a>.<a href="http://vbitz.com/images/Snapshot%2022:10:2012%2021:04.png"><img class="alignnone" title="That wil make it all easier" src="http://vbitz.com/images/Snapshot%2022:10:2012%2021:04.png" alt="" width="955" height="57" /></a>

In some more news with the same project I've switched from Java's built in scripting suport to the engine it's based on <a title="https://developer.mozilla.org/en-US/docs/Rhino" href="https://developer.mozilla.org/en-US/docs/Rhino" target="_blank">Mozilla Rhino</a>. In the end this should be quite a bit faster then just using javax.script. It does add a little complexity to compiling the project but if you want to download it yourself then.
