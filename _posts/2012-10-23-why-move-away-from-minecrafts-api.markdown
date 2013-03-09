---
layout: post
status: publish
published: true
title: Why move away from Minecraft's API
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 23
wordpress_url: http://vbitz.com/?p=23
date: 2012-10-23 02:28:16.000000000 +13:00
categories:
- Uncategorized
tags:
- MinecraftScript
comments: []
---
In the end a lot of people see Minecraft's API as a messy thing to work with. That's why layers like Forge and Bukkit exist. There both lay a cloth over Minecraft's messy code and simply expose the best parts with well designed alternatives in between.

In the end that's why I'm making MinecraftScript. Mojang for a long time has been working on a API for Minecraft and right now it's going to look a lot like the Bukkit we know today. That's not a bad thing but still it exposes the issue. Your going to have to link to a API at some point  Your going to need to setup a build environment at some point.

That's the reason behind why I'm making MinecraftScript (I keep thinking more and more this will only be a code name). The idea is when you install it by dropping the jar into a folder it will create some basic directory structure that will teach you where to put code you want Minecraft to run.

Now that was a little off topic, just a tangent that I went off on that I needed to go towards to make the rest of this post work.

In the end Forge covers a lot of the Minecraft API with pretty code. It does little towards a basic building block of Minecraft's codebase. IDs, a lot of things in minecraft are registered using IDs in a array somewhere else in the code. These are messy to work with and end up with a lot of mods fighting with each other for a very limited resource.

How does MinecraftScript fix this problem. Well for registering it's own blocks it get's a 256 wide block of ID's at the start, this allows the programming to be a little more dynamic as I'm able to "create" new blocks while a world is currently loaded. When it comes to working with ID's that are already used I refer to them with human readable strings. For example instead of using the block ID of stone (which is 1) you can just use "stone". This is going to make code a little more busy in some places though will help with documenting the code.
