---
id: 543
title: 'Redstone: Power Sources'
date: 2014-07-31T18:09:28+00:00
author: Jerome Tiong
layout: post

permalink: /?p=543
categories:
  - Redstone Mania
---
<h1 style="color: #222222;">
  Redstone Power Sources
</h1>

<p style="color: #222222;">
  Below you will find all the blocks that are capable of producing a redstone signal.
</p>

<h2 id="basic-power-sources" style="color: #222222;">
  Basic Power Sources
</h2>

<p style="color: #222222;">
  These are the standard sources of power for redstone circuits.
</p>

<div class="tagged" style="color: #222222;">
  <h3 id="redstone-torch">
    Redstone Torch
  </h3>
</div>

<p style="color: #222222;">
  This is the most basic source of redstone power. A redstone torch powers the block that contains it, plus the block above it.
</p>

<p style="color: #222222;">
  A redstone torch also acts as a signal inverter, where if power is transmitted to the block that a redstone torch is attached to, the torch will be switched off.
</p>

<div class="tagged" style="color: #222222;">
  <h3 id="block-of-redstone-">
    Block of Redstone
  </h3>
</div>

<p style="color: #222222;">
  This is the other &#8220;always-on&#8221; power source. It differs from a redstone torch in two ways:
</p>

<ul style="color: #222222;">
  <li>
    it only powers its own block, not the block above it.
  </li>
  <li>
    it is a solid block, so it is not destroyed by water or if you push it with a piston
  </li>
  <li>
    it does not invert signals.
  </li>
</ul>

<p style="color: #222222;">
  <p style="color: #222222;">
    The next three items are the basic switches that can be operated by players.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="button">
      Button
    </h3>
  </div>
  
  <p style="color: #222222;">
    These can be crafted from either wood or stone. They are activated by a right click. Wooden buttons can also be activated by hitting them with an arrow, fired from a bow, a dispenser or by a skeleton.
  </p>
  
  <p style="color: #222222;">
    Buttons provide a pulse of power to their own block and the one they are attached to. Each pulse from a stone button lasts 1 second; the pulse from a wooden button lasts 1.5 seconds, unless it is activated by an arrow, in which case the signal lasts until the arrow disappears, which disappears after 1 minute.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="lever">
      Lever
    </h3>
  </div>
  
  <p style="color: #222222;">
    This is a simple lever to switch redstone power on and off. The lever powers its own block and the one it&#8217;s attached to. Levers are very cheap to make and are often the most convenient power source.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="pressure-plates">
      Pressure Plates
    </h3>
  </div>
  
  <p style="color: #222222;">
    These are swiched on by a player or mob standing on them. The wooden pressure plate can also be activated by dropped items or arrows. Pressure plates power their own blocks and the block underneath them.
  </p>
  
  <h2 style="color: #222222;">
  </h2>
  
  <h2 id="variable-power-sources" style="color: #222222;">
    Variable Power Sources
  </h2>
  
  <p style="color: #222222;">
    These power sources are all sensors that output redstone power at various strengths, from 1 to 15. 15 is the same level as provided by basic power sources such as redstone torches and lever. &#8220;Signal strength&#8221; is the number of blocks a signal can travel along a redstone wire.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="weighted-pressure-plates-">
      Weighted Pressure Plates
    </h3>
  </div>
  
  <p style="color: #222222;">
    These pressure plates provide a variable output depending how much stuff is on them. They are not activated by players or mobs, just by dropped items.
  </p>
  
  <p style="color: #222222;">
    The light version is made of gold and its output power increases by one for every 4 items on it, reaching max power at 57. The heavy version is made of iron and weighs in increments of 42 blocks, reaching a maximum at 598 items.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="daylight-sensor-">
      Daylight Sensor
    </h3>
  </div>
  
  <p style="color: #222222;">
    Daylight sensors outputs a signal that varies in strength depending how much sunlight they are getting. The signal is highest at noon, and less in the morning or evening. Daylight sensors are not affected by light from torches or lamps.
  </p>
  
  <div class="captioned" style="color: #222222;">
    <p>
      It easy to invert the signal from a daylight sensor so that it causes a light to be switched on at night.
    </p>
  </div>
  
  <p style="color: #222222;">
    You will need to enter the nether and collect some Quartz before you can make a Daylight Sensor. Daylight sensors power their own block, but not the one below it.
  </p>
  
  <div class="tagged" style="color: #222222;">
    <h3 id="comparator">
      Comparator
    </h3>
  </div>
  
  <p style="color: #222222;">
    One of the uses of a comparator is as a sensor for how full a container is. If a comparator is placed next to a container, pointing away from it, it will output a signal depending on how full the container is.
  </p>
  
  <h2 style="color: #222222;">
  </h2>
  
  <h2 id="traps" style="color: #222222;">
    Traps
  </h2>
  
  <h3 id="tripwire" style="color: #222222;">
    Tripwire
  </h3>
  
  <p style="color: #222222;">
    A tripwire is made by connecting two Tripwire Hooks with string. When a player, mob or item disturbs the string, the tripwire is activated, and both tripwire hooks and the blocks they are attached to are powered.
  </p>
  
  <p style="color: #222222;" align="center">
    <div class="tagged" style="color: #222222;">
      <h3 id="trapped-chest">
        Trapped Chest
      </h3>
    </div>
    
    <p style="color: #222222;">
      A Trapped Chest is made by combining a tripwire hook with a chest. When the chest is opened, both the chest and the block it is placed on will be powered. The signal is very weak in the single player game, but in multiplayer it increased by 1 for each person who is viewing the chest inventory at the same time.
    </p>
    
    <h2 style="color: #222222;">
    </h2>
    
    <h2 id="rails" style="color: #222222;">
      Rails
    </h2>
    
    <div class="tagged" style="color: #222222;">
      <h3 id="detector-rail">
        Detector Rail
      </h3>
    </div>
    
    <p style="color: #222222;">
      Detector rails are activated when a minecart is on it.
    </p>