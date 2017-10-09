---
id: 352
title: 'Server Setup #3 (Configuration)'
date: 2014-08-04T08:36:55+00:00
author: Duncan Leo
layout: post

permalink: /?p=352
categories:
  - Server Setup
---
<span style="text-decoration: underline;"><strong>server.properties</strong> explained</span><figure id="attachment_362" style="width: 342px" class="wp-caption alignleft">

<img class="wp-image-362" src="/wp-content/uploads/2014/07/ServerPropsSublime-620x348.png" alt="Default generated server.properties file" width="342" height="192" srcset="http://128.199.175.217/wp-content/uploads/2014/07/ServerPropsSublime-620x348.png 620w, http://128.199.175.217/wp-content/uploads/2014/07/ServerPropsSublime-940x528.png 940w, http://128.199.175.217/wp-content/uploads/2014/07/ServerPropsSublime.png 1366w" sizes="(max-width: 342px) 100vw, 342px" /><figcaption class="wp-caption-text">Default generated server.properties file</figcaption></figure> 

Here is an explanation of each line created in a default server.properties run under a **Bukkit server.**
  
 `#Minecraft server properties<br />
#Tue Jul 29 15:54:09 SGT 2014`

Customising SuperFlat world generation. This code is **not usually used**:
  
`generator-settings=`

Permission level for OPs:
  
`op-permission-level=4`

&nbsp;

_true_ to **enable nether**, _false_ for otherwise
  
`allow-nether=true` 

Default &#8216;Overworld&#8217; name:
  
`level-name=world`

Query remote console access. Typically not used*:
  
`enable-query=false`

_true_ to allow players to fly **in Survival mode**, _false_ for otherwise:
  
`allow-flight=false`

Whether to **announce player achievements**:
  
`announce-player-achievements=true`

Default server port. Usually **25565**:
  
`server-port=25565`

Type of world to generate. Accepts **DEFAULT, FLAT, LARGEBIOMES, AMPLIFIED, CUSTOMIZED:**
  
`level-type=DEFAULT`

Whether to enable **remote query:**
  
`enable-rcon=false`

Seed for world generation:
  
`level-seed=`

_true_ to force players to join in default gamemode, _false_ to let them join in the gamemode they left in previously:
  
`force-gamemode=false`

**Server IP.** Usually **left untouched**, even on private servers run locally:
  
`server-ip=`

Maximum build height. Usually more than enough. In older versions, it was 128:
  
`max-build-height=256`

Whether to **spawn villagers:**
  
`spawn-npcs=true`

Whether to turn on the **white-list:**
  
`white-list=false`

Whether to **spawn mobs**:
  
`spawn-animals=true`

If this is set to true, players are **banned when they die:**
  
`hardcore=false`

Whether the server sends **snoop data** to Mojang:
  
`snooper-enabled=true`

This is the setting that differentiates between a **premium** **server** and one that is **cracked:**
  
`online-mode=true`

Resource pack URL (direct). It must not contain in-between agents such as **adf.ly.** If set to true, players will get a dialog on join:
  
`resource-pack=`

Enable/Disable **PvP**:
  
`pvp=true`

Changes the magnitude of damage dealt to players (from things like hunger, etc):
  
`difficulty=1`

Enable/Disable **command blocks:**
  
`enable-command-block=false`

Game mode. 0 &#8211; Survival, 1 &#8211; Creative, 2 &#8211; Adventure, 3 &#8211; Spectator:
  
`gamemode=0`

How long a player can idle before being kicked:
  
`player-idle-timeout=0`

Maximum number of players:
  
`max-players=20`

Whether to spawn hostile mobs:
  
`spawn-monsters=true`

Enable/Disable structure generation in new chunks. **Usually not touched**:
  
`generate-structures=true`

How much world data the server sends to the client:
  
`view-distance=10`

Message of the day. Seen if the server is on a client&#8217;s **Server List:**
  
`motd=A Minecraft Server`

<span style="text-decoration: underline;">Notice for Spigot</span>

Spigot&#8217;s additional settings come in the form of **spigot.yml**, which has its own settings such as anti-xray.

&nbsp;

These settings are the main functionality of the Bukkit/Spigot server. Additional functionality will come in plugins that you can install into the **/plugins** folder.

&nbsp;

_References:_

Minecraft WIKI: http://minecraft.gamepedia.com/Server.properties#Server.properties