---
layout: post
status: publish
published: true
title: Build 43 Changelog
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 69
wordpress_url: http://vbitz.com/?p=69
date: 2012-11-21 17:04:50.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link: </strong><a title="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_43.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_43.zip">http://vbitz.com/minecraftscript/MinecraftScript_MC1.4.4_43.zip</a>

<strong>Changes:</strong>
<ul>
	<li>MinecraftScript can now be run without the client-side installed if the client has MinecraftForge installed.</li>
	<li>Added world().replaceCube() which is basically the same as setCube</li>
	<li>Added world().setBiome(int biome, vector3f location) you do need to close and reopen the world for this to take effect right now.</li>
	<li>Added addSmeltingRecipe(int inputId, int outputId, int exp) which registers a new smelting recipe</li>
	<li>Fixed bugs on a server</li>
	<li>world().killDrops now requires a center</li>
	<li>Updated test.js</li>
	<li>Added player.exp(int amo) which grants experience</li>
	<li>Added player.expLevel(int amo) which grants experience levels</li>
	<li>Added v(double x, double y, double z) as a shorthand for vector</li>
	<li>Added player.getName() which returns the name of the player</li>
	<li>Added give to ScriptedBlock which gives you or another player a count of the block</li>
	<li>Added ScriptedItem</li>
	<li>ScriptedItems can be thrown and on impact will run there right click function with a vector3f of the hit position</li>
	<li>Added world().activate(vector3f pos) which simulates a right click on a block. This means you can now activate redstone from javascript easily.</li>
	<li>Added Extension support. This is not really useful to most people right now.</li>
</ul>
