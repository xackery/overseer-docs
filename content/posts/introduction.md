---
banner: "post/images/site.jpg"
categories:  ["site"]
date:  "2023-08-27T01:19:18-07:00"
description:  "Introduction"
images:  ["post/images/site.jpg"]
menuTitle: ""
tags:  ["tech"]
title:  "Introduction to Overseer"

---
Overseer is a suite of tools made to assist your eqemu experience
<!--more-->
- start: Recommended way to start the server, runs shared memory then overseer
- stop: A more aggressive way to stop overseer and all eqemu programs. In most cases, pressing CTRL+C or Q on the overseer console window is all you need to shut down your server. However, if you run overseer headless, or it crashed in some way and there's lingering processes, this will kill them all.
- overseer: Runs and manages zones, world, queryserv, ucs, and other programs. Provides a brief overview for at a glance health. If a zone is loop crashing, it does a gradual restart system, where first reboot will happen almost immediately, second one will wait 5 seconds, and adds 5 seconds each restart, until 30+ seconds between attempts. (Resets the +5 after 30 minutes of being up) This is to lessen the burden on the server restarting processes, as well as make it more obvious on overseer when something is wrong. If a zone is generated any errors in the last 30 minutes, it will be placed in the error category.
- verify: Verifies "online" related things such as if login server is exposed to WAN, if ports are forwarded properly, security concerns with ports that may not want to be forwarded, and also quick reporting tips for errors being reported on overseer
- diagnose: Verifies "offline" related things that verify does not entail, things like config file setup, files that may be improperly configured.
- analyze: Does a deep analysis of logs to give suggestions on root cause problems you may be facing. 
- install: This is for installing a brand new server from scratch. Goal: Never use admin, attempt to make all content within the same folder, so it is portable.
- update: Verifies everything in eqemu is up to date. During initial setup, if you opt for auto update, the "start" program will automatically do updates for you. This is for manual updates.