---
layout: post
title: How to Solve Papership Webdev Sync Failure
date: 2022-05-02 13:45:10
description:
tags: ['Papership', 'Webdev', 'Zotero']
categories: Guide
---

Currently, I am using Papership to read and make note on papers collected and managed by Zotero.
All paper files from Zotero are hosted by a Webdev service on a NAS back home.
But there's a sync failure regularly going on of my Papership app, while all Zotero across different devices syncs without any problem.
Only the edition made by Papership cannot sync with other devices. I have no idea why this issue happens all the time.

But there's one way to fix it:

Just create an empty text file called `lastsync.txt` inside the zotero root folder that is hosted by webdev service.

It will sync again on Papership.
