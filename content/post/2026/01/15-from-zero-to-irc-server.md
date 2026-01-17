---
layout: post
title: "From zero to IRC server in just a day"
date: 2026-01-15T06:48:31+0800
lastmod: 2026-01-16T20:27:01+0800
type: post
categories:
- "Posts"
- "Tech"
- "Indie Web"
thumbnail: https://s3.amazonaws.com/micro.blog/thumbnails/2026/01/16/blog.zerocchi.com/78d3f08ea4ca0ae1304c422ba7a3e4ef.png
opengraph:
  title: "Zerocchi Blog - From zero to IRC server in just a day"
  image: https://s3.amazonaws.com/micro.blog/opengraph/2026/01/14/5710088.png
images:
- https://cdn.uploads.micro.blog/285193/2026/6ce9024d41.png
photos:
photos_with_metadata:
url: "/2026/01/15/064831.html"
bluesky:
  id: "bafyreigbpigguj72s7bi4hslwj5ic3jy3423rdbwur5bhl3baevcv2uwca"
  url: "at://did:plc:wpdbknogd47ooysv6eau2yjt/app.bsky.feed.post/3mcg5onev7f2p"
  link: "https://bsky.app/profile/did:plc:wpdbknogd47ooysv6eau2yjt/post/3mcg5onev7f2p"
  handle: "zerocchi.com"
  hostname: "bsky.social"
  did: "did:plc:wpdbknogd47ooysv6eau2yjt"
---
Whoops I almost slipped to the realm of not writing. 

What can I say.. this past few days I was hyperfixating with IRC, and yesterday alone I spent the entire day setting up a small IRC server for my project circle just for the heck of it because I don't think any sane, normal person will use IRC in this day and age, especially when Discord exist. I'm here not to discuss the technical aspect of it, but my experiences setting up these little gremlins.

The first thing I need to do is to find an IRCd, or what people call IRC daemon. This thing is the one that responsible to implement IRC protocols so that people can talk over the internet. I was looking to install InspIRCd just because it look popular enough, but after a few while I decided against it and proceed to get [ngIRCd](https://github.com/ngircd/ngircd) instead. The reason being ngIRCd is pretty much a small and simple IRC daemon, unlike [InspiIRCd](https://www.inspircd.org/) and [UnrealIRCd](https://www.unrealircd.org/) which is quite complex under the hood and are tailored to big servers. But even ngIRCd is pretty tricky to set up the first time. Making it run with Systemd is just very annoying, and it failed to spawn so many times it got me frustrated. Eventually after a few hours I managed to get it to spin together with additional settings like user cloak to hide the IP address attached as hostname. But still, it's pretty lonely since the server is quite barebone. So I decided to install a collection of IRC services that provide you stuff like NickServ, ChanServ and all those server management stuff. 

There are two popular packages, Anope and Atheme. I decided to go with [Atheme](https://atheme.dev/) because it looks simple and modern enough, although not as popular as Anope. Atheme is even trickier not because it's difficult to set up, it's because I skipped reading docs and just DuckDuckGo-ing my way jumping across Github issues and forum posts to set the thing up. Had I sit down, sip some tea, and went through the docs properly, I'll be done in few minutes. With some luck and patience, the services got through and connected to my server. I just need to attach a few modules afterwards and I already have a collection of Servs at my disposal. 

At the end of the day, after wrestling with all the configurations and seemingly hundreds of errors, I finally managed to own a complete small IRC server with all the bells and whistles. I finished them up by getting an IRC bot because what's IRC without all those bots. After few searches I decided on using [Limnoria](https://limnoria.net/), a successor to Supybot. I also set up The Lounge web client so anyone (my friends) without desktop client can join the server easily. The whole process was quite frustrating and fun at the same time and I learnt a lot along the way. Still feel like wanting to try writing IRC bot from scratch so I would have extra goodies for my small server.

Where is the server, you ask? As this is for my own amusement, I will just keep it to myself and several friends for now. It's public and part of a project I was in, but one needs to know the address to enter and I don't think anyone else interested at this point of time. Maybe one day when the project become bigger, people will find out and join the server by themselves. That is if the server is still available at that point.

![The aforementioned IRC server](6ce9024d41.png)
