---
title: "Netty from Scratch - Introduction"
layout: single
header:
  image: /assets/images/netty_banner.jpg
categories:
  - netty-from-scratch
series: "Netty from Scratch"
tags:
  - java
  - networking
  - jvm
  - netty
  - vertx
---

I would imagine most everyone who writes JVM based web services has either used or heard of Netty, even if only from stack traces or dependency conflicts.

For me, it was usually lurking a layer or two below the libraries and frameworks that I was using - such as VertX. I was aware of Netty, and what it's purpose was, but I wasn't sure *exactly* how it worked beneath the covers. Sure, I'd read about the Netty Event Loop, and I knew at a high level about it's different implementations (NIO, Epoll etc), but the precise details of its inner workings weren't completely clear to me.

As someone who has been working on large scale distributed systems for a number of years now, I thought it was time that I learnt more about the networking stacks that formed the core of these systems, without blindly relying on the (albeit very very good) abstractions that have been built in the open-source ecosystem. To that end, it seemed like the best way to learn what these libraries were doing for me, was to try and implement something similar myself (of course with far less features and optimizations that the real thing).

Due to the sheer breadth of topics that are associated with libraries such as Netty, I expect this to be a fairly long collection of posts, with the series going off on many tangents along the way. I'm not sure exactly where this series will end and what the resulting project will look like, but I hope that I can provide some insights into how we send and receive requests over the network, while focusing on the kinds of optmizations and trade-offs that exist deep below the high level api that we're used to.
