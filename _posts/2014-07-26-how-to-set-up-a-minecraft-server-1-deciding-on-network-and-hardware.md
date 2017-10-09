---
id: 12
title: 'Server Setup #1 (Deciding on Network and Hardware)'
date: 2014-07-26T11:31:46+00:00
author: Duncan Leo
layout: post

permalink: /?p=12
categories:
  - Server Setup
---
So, you&#8217;re thinking of setting up a Minecraft server. That&#8217;s fantastic! Here&#8217;s a comprehensive guide on how to do so!

&nbsp;

Firstly, consider the purpose of the server. This section will cover two of the most common scenarios.

**<span style="text-decoration: underline;">A small group of friends</span>**

<span style="text-decoration: underline;">Network</span>

VPN or Port-forwarding?
  
The first is simpler, requiring no software installation, while the second is more complicated but does not require any software at all. It really depends on whether your friends mind the hassle.<figure id="attachment_283" style="width: 134px" class="wp-caption alignleft">

[<img class=" wp-image-283" src="/wp-content/uploads/2014/07/LogMeIn-Hamachi.png" alt="LogMeIn Hamachi" width="134" height="207" />](/wp-content/uploads/2014/07/LogMeIn-Hamachi.png)<figcaption class="wp-caption-text">LogMeIn Hamachi</figcaption></figure> <figure id="attachment_282" style="width: 288px" class="wp-caption alignleft">[<img class="wp-image-282 size-full" src="/wp-content/uploads/2014/07/gaming-vpn.png" alt="Evolve Gaming VPN" width="288" height="204" />](/wp-content/uploads/2014/07/gaming-vpn.png)<figcaption class="wp-caption-text">Evolve Gaming VPN</figcaption></figure> 

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

&nbsp;

Another alternative would be using a server host or VPS, which should come with ports opened by default. The downside to this is the cost involved. It also requires the knowledge of how to transfer files and control the Minecraft console remotely.<figure id="attachment_98" style="width: 300px" class="wp-caption alignnone">

[<img class="wp-image-98 size-medium" src="/wp-content/uploads/2014/07/MCSS-300x231.png" alt="Screenshot" width="300" height="231" srcset="http://128.199.175.217/wp-content/uploads/2014/07/MCSS-300x231.png 300w, http://128.199.175.217/wp-content/uploads/2014/07/MCSS.png 585w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/2014/07/MCSS.png)<figcaption class="wp-caption-text">Sample Minecraft server console</figcaption></figure> 

&nbsp;

<span style="text-decoration: underline;">Hardware specifications</span>

As a server for your friends, you could definitely run it on your own computer! All you would need are sufficient hardware resources. I would recommend at least the following specifications:

  * **2GB** of memory
  * **1 GB** of disk space

Now that you&#8217;ve reached this point, skip the public server section and read the rest!

&nbsp;

**<span style="text-decoration: underline;">A server for the public</span>**

<span style="text-decoration: underline;">Network</span>

Unless you run a server at home, you will most likely be running the Minecraft server off a dedicated host or a VPS*. Both typically require knowledge of the **File Transfer Protocol (FTP). **<figure id="attachment_101" style="width: 300px" class="wp-caption alignnone">

[<img class="size-medium wp-image-101" src="/wp-content/uploads/2014/07/FTP-300x151.png" alt="FileZilla screenshot" width="300" height="151" srcset="http://128.199.175.217/wp-content/uploads/2014/07/FTP-300x151.png 300w, http://128.199.175.217/wp-content/uploads/2014/07/FTP-1024x518.png 1024w, http://128.199.175.217/wp-content/uploads/2014/07/FTP.png 1366w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/2014/07/FTP.png)<figcaption class="wp-caption-text">FileZilla, an FTP client</figcaption></figure> 

&nbsp;

If you are using a VPS, remotely connecting to it will differ for different operating systems. Windows would require RDP\*\* or VNC\*\*, while for Linux it would typically be SSH\***.

<span style="text-decoration: underline;">Hardware specifications</span>

There are several things to consider for the server on a VPS/host. Here are some basic specifications:

  * **2GB **of memory
  * **1TB** of network transfer (varies per provider)
  * **1 **processor core
  * **10GB** of disk space

These is a very basic list. If your server is going to serve more than 30 players, I recommend at least adding **one more processor core **and a **few more gigabytes** of memory.

&nbsp;

* **(VPS)** Virtual Private Server, basically a remote computer. Mostly used as servers.
  
** **(RDP/VNC)** Remote Desktop Protocol (RDP), Virtual Network Computing (VNC) are desktop-sharing mechanisms.
  
\*** **(SSH) **Secure Shell, secure network services between remotely-connected computers

&nbsp;

After settling on the server network and hardware, it&#8217;s now time to choose your server &#8216;flavour&#8217;.

_This tutorial will continue in Part #2._

&nbsp;

_References:_

_Screenshot of LogMeIn Hamachi:  <http://cdn.ilovefreesoftware.com/wp-content/uploads/2010/04/LogMeIn-Hamachi.png>
  
Screeshot of Evolve Gaming VPN: _<https://assets.evolvehq.com/img/ill/gaming-vpn.png>

_ _