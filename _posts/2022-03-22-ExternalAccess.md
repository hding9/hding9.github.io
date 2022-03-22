---
layout: post
title: External Access Your NAS
date: 2022-03-21 01:01:15
description:
tags: ['NAS', 'DDNS', 'frp', 'openvpn']
categories: Tips
---

<!-- I heard "NAS" a long time ago, but I used to think it's just not something that I really need. 
I don't have too much data to store, and iCloud + Dropbox + Onedrive seems to meet my daily needs well enough. 
Apparently, the reason I write this post is because I have a NAS running 24/7, and I'm pretty happy to have it.


It's all started from a software called **Mendeley** -->


If you have a public IP (the router IP is the same with the IP you get online), no matter if it is static or not,
things will be easy. Just configure port forwarding on your router. Then for static IP, use your IP:port to access 
the NAS. For dynamic IP, configure DDNS (assigns dynamic IP to your domain), and use domain:port to access.


A more safer way is to configure a VPN tunnel between the NAS and devices outside NAS's local network. 
However, this only works if your ISP provides no NAT service or static NAT (meaning that you have a static IP).


If you don't have a public IP, then you will need reverse proxy to help you expose your local network behind a NAT 
to the internet. For that, a VPS with public IP and reverse proxy tool (NGINX, FRP) is required. 
Thus, the drawback is evident. The communication between your device and NAS highly depends on internet quality, 
and hardware performance of your VPS. 

Just save a spot for this topic right here. I will introduce methods above once I have time in the future.
