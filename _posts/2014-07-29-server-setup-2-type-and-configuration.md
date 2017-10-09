---
id: 27
title: 'Server Setup #2 (Server Types and Initial Run)'
date: 2014-07-29T17:44:09+00:00
author: Duncan Leo
layout: post


categories:
  - Server Setup
---
There are various types of Minecraft servers:

<span style="text-decoration: underline;"><strong>Vanilla</strong></span>

_The first one to be updated, the one that most people don&#8217;t use._<figure id="attachment_107" style="width: 205px" class="wp-caption alignleft">

[<img class="wp-image-107" src="/wp-content/uploads/2014/07/mcs-console2-620x363.png" alt="http://jafdip.com/wp-content/uploads/2011/09/mcs-console2.png" width="205" height="120" srcset="/wp-content/uploads/2014/07/mcs-console2-620x363.png 620w, /wp-content/uploads/2014/07/mcs-console2.png 857w" sizes="(max-width: 205px) 100vw, 205px" />](/wp-content/uploads/2014/07/mcs-console2.png)<figcaption class="wp-caption-text">Vanilla GUI</figcaption></figure> 

&#8216;Vanilla&#8217; is the name given to the Minecraft Server that can be downloaded from Minecraft.net. It cannot run any plugins (as of 1.7.10) and cannot defend itself against hackers. Functionality can only be added through command blocks in the game. The server also comes with a graphical interface.

**Not recommended for use &#8211; extremely limited functionality.**

<span style="text-decoration: underline;"><strong>Bukkit</strong></span>

_The one most widely used and supported. _<figure id="attachment_98" style="width: 181px" class="wp-caption alignright">

[<img class="wp-image-98" src="/wp-content/uploads/2014/07/MCSS-300x231.png" alt="Bukkit console" width="181" height="139" srcset="/wp-content/uploads/2014/07/MCSS-300x231.png 300w, /wp-content/uploads/2014/07/MCSS.png 585w" sizes="(max-width: 181px) 100vw, 181px" />](/wp-content/uploads/2014/07/MCSS.png)<figcaption class="wp-caption-text">Bukkit console</figcaption></figure> 

The successor to hMod is today one of the most widely used variants of the Minecraft server. It is also widely supported by plugin developers who add functionality to the game. It is also updated frequently as well.

**Highly recommended.**

&nbsp;

**<span style="text-decoration: underline;">Spigot</span>**

_The &#8216;high-performance&#8217; version of Bukkit._

Spigot touts itself as a high-performance version of Bukkit. It is able to use most Bukkit plugins and also has some built-in functionality such as Anti-Xray. It is also updated frequently.

**Highly recommended if your server is resource-tight or serves many players at once.**

&nbsp;

_The other variants listed below usually add functionality or are a different game mode built atop Bukkit/Spigot. They typically require a modified client as well. As such, they usually do require players to do some work on the client. Only some of the more well-known variants are listed._

&nbsp;

<span style="text-decoration: underline;"><strong>Spout</strong></span><figure style="width: 174px" class="wp-caption alignleft">

<img src="http://i49.tinypic.com/121ee04.jpg" alt="http://i49.tinypic.com/121ee04.jpg" width="174" height="135" /><figcaption class="wp-caption-text">Sample custom GUI, made possible by SpoutCraft</figcaption></figure> 

On the server side, this is just a plugin running on Bukkit/Spigot. Functionality is added through a client mod known as &#8216;SpoutCraft&#8217;. Mainly to add functionality that can&#8217;t be done with plugins and the unmodified client, such as custom items or music streaming.

**Recommended only if you have a pressing need for such functionality. Otherwise, this is an unnecessary trouble for your players.**

&nbsp;

**<span style="text-decoration: underline;">MC Port Central</span>**

This is a combination of Bukkit and Forge, carefully integrated to work together. Used mainly for mods. This variant is not updated as frequently as the others as it takes a lot of work integrating the two.

**Recommended if your players are into mods and do not mind playing an old version of Minecraft.**

&nbsp;

&nbsp;

This post will only cover the two main mods, **Bukkit** and **Spigot**. The server.properties file common to them will also apply to the **vanilla** server.

<span style="text-decoration: underline;"><strong>PREPARING THE SERVER</strong></span>

<span style="text-decoration: underline;"><strong>Software requirements</strong></span><figure style="width: 184px" class="wp-caption alignleft">

<img src="http://mtacertification.com/images/core-java.jpg" alt="http://mtacertification.com/images/core-java.jpg" width="184" height="130" /><figcaption class="wp-caption-text">Oracle Java</figcaption></figure> 

All of these mods require Java. Many Bukkit plugins require at least **version 7**.

Windows and Mac OS X users should install it from the Oracle site (following the OS architecture, i.e. 32/64 bit).

Linux users can follow this guide <a title="WebUPD8" href="http://www.webupd8.org/2012/01/install-oracle-java-jdk-7-in-ubuntu-via.html" target="_blank">here</a>

&nbsp;

<span style="text-decoration: underline;"><strong>Starting from</strong><strong> scratch</strong></span>**
  
** If you are using a dedicated host, **ignore the shell-script creation.** Your host will probably provide a point-and-click interface. **Skip to Configuration.**

Place your downloaded .jar file into a directory of your choice. _This directory will contain ALL the files for your server._

Create a shell script, and place this in it: (A server with **1024MB** of memory, change accordingly)

`java -jar <filename>.jar -Xms1024m -Xmx1024m`

If you are a VPS user, use this instead. It allows resuming of the Minecraft console:

`screen -s minecraft java -jar <filename>.jar -Xms1024m -Xmx1024m`

Save it using a plain text editor.

<span style="text-decoration: underline;"><strong>First run</strong></span>

Run the shell script once. It will create default files, including the worlds.

Here is a video showing the initial run:



**<span style="text-decoration: underline;">Text editor</span>**

At this point of time, it would be advisable to use a text editor other than Notepad or TextEdit. Use a text editor that can recognise syntaxes, with the most important being **YAML.**

<span style="text-decoration: underline;"><strong>server.properties</strong></span>

This file is present in all three variants (Vanilla, Bukkit, Spigot)

The syntax of this file is what is commonly known as a **Java Properties** file. _(key=value)_

The most notable entries include:
  
`online-mode=true` ( `true` for premium servers, `false` for cracked ones)
  
`server-port=25565` (This should be left as it is. Some dedicated hosts ignore this option)
  
`server-ip` (This should be left untouched so Minecraft is accessible from all the IPs pointing to the machine it is running on)
  
`max-players=20` (Change as you please)
  
`enable-command-block=false` (If your server won&#8217;t touch these blocks at all, ignore this option)<figure id="attachment_123" style="width: 151px" class="wp-caption alignnone">

[<img class=" wp-image-123" src="/wp-content/uploads/2014/07/MCServerProps.png" alt="server.properties" width="151" height="227" />](/wp-content/uploads/2014/07/MCServerProps.png)<figcaption class="wp-caption-text">Sample section of a server.properties file</figcaption></figure> 

If you intend to have a server resource pack, then the `resource-pack` option will be useful for you. It accepts a direct URL to a resource pack .zip file (Advertising services like bit.ly will not work with this)

<span style="text-decoration: underline;"><strong>.json files</strong></span>

These files are not meant to be edited using a text editor, but rather by in-game commands.

<span style="text-decoration: underline;"><strong>permissions.yml</strong></span>

This file is used by the primitive built-in permissions system in Bukkit. It is generally recommended not to use this but  rather permissions plugins such as PermissionsEX.

<span style="text-decoration: underline;"><strong>spigot.yml</strong></span>

This is a Spigot-specific file and contains settings that only affect Spigot.

&nbsp;

_This tutorial will be continued in Part #3._

&nbsp;

References:
  
Vanilla GUI: [http://jafdip.com/wp-content/uploads/2011/09/mcs-console2.png
  
](http://jafdip.com/wp-content/uploads/2011/09/mcs-console2.png) SpoutCraft: [http://i49.tinypic.com/121ee04.jpg
  
](http://i49.tinypic.com/121ee04.jpg) Java logo: <http://mtacertification.com/images/core-java.jpg>