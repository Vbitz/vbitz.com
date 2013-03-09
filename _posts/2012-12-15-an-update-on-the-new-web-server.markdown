---
layout: post
status: publish
published: true
title: An Update on the new Web Server
author: Vbitz
author_login: Vbitz
author_email: jscarsbrook@gmail.com
wordpress_id: 82
wordpress_url: http://vbitz.com/?p=82
date: 2012-12-15 03:08:42.000000000 +13:00
categories:
- Uncategorized
tags: []
comments: []
---
Java has a really awesome built in web server that spins it's self off in a separate thread. That's what I'm going to be using for MinecraftScript now rather then my own one. The downside of separate threads is minecraft is nowhere near thread-safe. I will solve that issue by invoking web server events on the main thread at a fixed rate. Same way the old web server worked in that respect but now static files and such can be served without interrupting the main thread.
