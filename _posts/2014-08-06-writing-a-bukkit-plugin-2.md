---
id: 484
title: 'Writing a Bukkit plugin #2'
date: 2014-08-06T23:03:36+00:00
author: Duncan Leo
layout: post
guid: http://thinkingminecraft.tk/?p=484
permalink: /?p=484
categories:
  - Bukkit Plugins
---
This tutorial carries on from [Part #1.](http://thinkingminecraft.tk/?p=420 "Writing a Bukkit plugin #1 (Initial Set-Up)")

In Part #1, we had Eclipse set up and a project created, waiting for us to code!

But first, we need to understand how Bukkit works with plugins.

<span style="text-decoration: underline;"><strong>Events</strong></span>

In Bukkit, plugins work based on an events system. Many actions in Minecraft itself are linked to events. An example is `PlayerJoinEvent`, which is an event called _every time a player joins._

In addition to these events, a plugin can also hook onto command events (which are called every time **any** command is run) and save data to the server directories.

The complete list of events can be seen at the Bukkit [Javadoc location](http://jd.bukkit.org/dev/apidocs "Bukkit Javadocs").<figure id="attachment_488" style="width: 196px" class="wp-caption alignleft">

[<img class="wp-image-488" src="http://thinkingminecraft.tk/wp-content/uploads/2014/08/bukkit_javadoc_events-620x272.png" alt="A section of Bukkit's Javadocs" width="196" height="86" srcset="http://128.199.175.217/wp-content/uploads/2014/08/bukkit_javadoc_events-620x272.png 620w, http://128.199.175.217/wp-content/uploads/2014/08/bukkit_javadoc_events-940x412.png 940w, http://128.199.175.217/wp-content/uploads/2014/08/bukkit_javadoc_events.png 1363w" sizes="(max-width: 196px) 100vw, 196px" />](http://thinkingminecraft.tk/wp-content/uploads/2014/08/bukkit_javadoc_events.png)<figcaption class="wp-caption-text">A section of Bukkit&#8217;s Javadocs</figcaption></figure> 

There are two important methods that **any plugin should have.** These are the `onEnable` and `onDisable` methods. They are called whenever the plugin is enabled and disabled, respectively.

Code that your plugin runs when an event is called are called **event handlers.** Your plugin has to register its event handlers&#8217; existence with Bukkit. This is done through this line of code:

&nbsp;

<pre class="prettyprint"><code>Bukkit.getServer().getPluginManager().registerEvents(this, this);</code></pre>

The handlers are typically registered at the `onEnable` method. Write in your `onEnable` method, and add in the line above:<figure id="attachment_492" style="width: 198px" class="wp-caption alignnone">

<img class=" wp-image-492" src="http://thinkingminecraft.tk/wp-content/uploads/2014/08/eclipse_code1-620x348.png" alt="The method in Eclipse" width="198" height="111" srcset="http://128.199.175.217/wp-content/uploads/2014/08/eclipse_code1-620x348.png 620w, http://128.199.175.217/wp-content/uploads/2014/08/eclipse_code1-940x528.png 940w, http://128.199.175.217/wp-content/uploads/2014/08/eclipse_code1.png 1227w" sizes="(max-width: 198px) 100vw, 198px" /><figcaption class="wp-caption-text">The method in Eclipse</figcaption></figure> 

Bukkit will now call your event handlers when the events are called!

&nbsp;

<span style="text-decoration: underline;"><strong>Main Variables/Classes</strong></span>

In Java, there are things like variables and classes. Bukkit has classes specific to Minecraft. Here, we will go through some of the more common classes.

This is the **Bukkit** class. This handles some of the more background parts of the server. Common uses of this class include:
  
``

<pre class="prettyprint"><code>Bukkit.broadcastMessage("hi"); //Broadcasts a message to all players
Bukkit.getPlayer(UUID); //Get a Player object from his UUID.
Bukkit.getScheduler() //This returns a BukkitScheduler object which can be used to schedule tasks using Bukkit's internal ticks system.</code></pre>

More often than not, you will be using the **Player** class. This pertains to certain parts of a player:

<pre class="prettyprint"><code>Player.getName(); //Returns a player's name
Player.getHealth(); //Returns a player's health as a double
Player.sendMessage("hi dude"); //Broadcasts a message to this player only (instead of everyone)
Player.kickPlayer("Go away man"); //Kicks a player
Player.setDisplayName("Cowboy"); //Sets a player's friendly name (not login name)
Player.updateInventory(); //Used when you need to update a player's inventory
Player.getLocation(); //Returns a Location object containing data about a player's location
</code></pre>

Further on here is the **Entity** class, which refers to any single entity. This may be a passive mob, a hostile mob or even an experience orb:

<pre class="prettyprint"><code>Entity.remove(); //Flags entity for removal
Entity.getType(); //Returns an EntityType object containing data about the entity's type</code></pre>

&nbsp;

<span style="text-decoration: underline;"><strong>Event Handlers</strong></span>

Here is an example of an event handler which greets a player with a &#8216;Hello&#8217; message when they join the server:

<pre class="prettyprint"><code>@EventHandler
public void HelloMessage (PlayerJoinEvent e) {
	Bukkit.broadcastMessage("Hello" + e.getPlayer().getName());
}</code></pre>

Take note of the `@EventHandler`, which marks the method as an event handler.

In this example, we wrote an Event Handler for the `PlayerJoinEvent` event, which is called when a player joins. The method is called `HelloMessage`.

With this, you can basically do anything based on the events made available by Bukkit!

&nbsp;

<span style="text-decoration: underline;"><strong>Command Handlers</strong></span>

While there is a PlayerCommandPreprocessEvent, it is generally used to intercept commands, which could be employed by command loggers and the like.

Commands use the onCommand method that returns a boolean. When the method returns false, Bukkit will automatically send the command sender the command&#8217;s usage. _Take note &#8211; the command sender could come from the Console, and isn&#8217;t always players._

Here&#8217;s an example:

<pre class="prettyprint"><code>@Override
public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
	if (cmd.getName().equalsIgnoreCase("sayhi")) {
		sender.sendMessage("Hi " + sender.getName());
		return true;
	}
	return false; 
}</code></pre>

Usually false is returned if the player seems to have misused the command arguments, etc.

&nbsp;

<span style="text-decoration: underline;"><strong>Other variables/classes</strong></span>

Bukkit has Java classes of almost anything that can be represented in-game. This can be a sign post, a chest, an item frame, or even a chicken egg. Each of these classes have their own methods and extend some of the &#8216;common&#8217; classes between them.

For example, there is the `Chicken` class, and the `Cow` class. Both represent the passive mobs in-game. They both have various methods like getHealth() and they both **extend certain classes &#8211; **`Entity` and `LivingEntity`.

If you ever had to test a general class for a more specific one, such as testing if an `Entity` was a `Chicken`, you could do this:

<pre class="prettyprint"><code>//Assuming you have an entity object called 'animal'
if (animal instanceof Chicken) {
	Bukkit.broadcastMessage("This is a chicken!");
}</code></pre>

&nbsp;

<span style="text-decoration: underline;"><strong>plugin.yml</strong></span>

This is an extremely important file. Plugins **cannot function** **without it.** This file is a plugin descriptor for Bukkit. It tells Bukkit what the main starting class is, the name of the plugin, the version and the commands registered with onCommand(). Here is a sample, using the plugin from our Eclipse sample:

<pre class="prettyprint lang-yaml"><code>name: Example
main: com.someones.example.Main
version: 1.0
commands:
	sayhi:
		description: Says hi to you
		usage: /sayhi
		permissions: example.hi
		permissions-message: No perms dude!</code></pre>

With this, you should be able to create many plugins. If you enjoyed the tutorial, please leave some comments below! Thank you 🙂