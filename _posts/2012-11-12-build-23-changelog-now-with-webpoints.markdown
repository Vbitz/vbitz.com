---
layout: post
status: publish
published: true
title: ! 'Build 23 Changelog : Now with Webpoints'
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 48
wordpress_url: http://vbitz.com/?p=48
date: 2012-11-12 21:02:31.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
<strong>Download Link:</strong> <a title="http://vbitz.com/minecraftscript/MinecraftScript_23.zip" href="http://vbitz.com/minecraftscript/MinecraftScript_23.zip" target="_blank">http://vbitz.com/minecraftscript/MinecraftScript_23.zip</a>

<strong>Webpoints</strong>

The Server will now listen on port 12524 for HTTP requests. These can be bound to a javascript function using api.addWebpoint. The return of the function or any errors encountered will be returned to the HTTP client. The Server will only accept connections from clients while game ticks are running (The game needs to be unpaused on singleplayer).

In the very near future the http request will support arguments which will be passed to the function.

<strong>Changes</strong>
<ul>
	<li>Added tidy JavaScript output. Undefined will no longer print anything</li>
	<li>Added isPreload which will be true if startup scripts are running</li>
	<li>Added api.addWebpoint(string name, Function funct)</li>
</ul>
