---
title: GPIO Port for Raspberry Pi
date: 2019-07-18T20:02:07.000Z
author: Nenad Rakocevic
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
category: update
tags:
  - Raspberry Pi
  - GPIO
  - port
  - board
  - hardware
  - hack
---

{{< rawhtml >}}
As part of the R&amp;D work on port! datatype in port-type branch, we have implemented a <a href="https://en.wikipedia.org/wiki/General-purpose_input/output" target="_blank">GPIO</a>&nbsp;driver for <a href="https://www.raspberrypi.org/" target="_blank">Raspberry Pi</a> boards, as a <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">gpio://</span> scheme (no third-party library needed). This work helped define the low-level API for ports written in purely Red/System or a mix of Red and Red/System.<br />
<br />
The Raspberry Pi is a very popular board with millions of units sold, so this is a market where Red could be potentially helpful to developers. We could run Red on such boards for years but did not have proper GPIO support, so this is now fixed!<br />
<br />
The current features supported by the GPIO port are:<br />
<ul>
<li>auto-detecting the Raspberry Pi board type</li>
<li>uses <span style="font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">/dev/mem</span> or<span style="font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">/dev/gpiomem</span> for direct and fast access.</li>
<li>reading a GPIO pin state.</li>
<li>writing to a GPIO pin state.</li>
<li>hardware PWM output support (on capable pins).</li>
<li>a simple DSL for sending commands.</li>
</ul>
<br />
Planned (but not scheduled) future features include:<br />
<ul>
<li>generating events when a pin state changes.</li>
<li>software PWM on all GPIO pins.</li>
<li>a higher-level reactive object layer for a API-less interface.</li>
<li>various drivers for common peripherals.</li>
</ul>
<br />
The source code for the&nbsp;<span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">gpio://</span>&nbsp;scheme can be found <a href="https://github.com/red/red/blob/master/environment/schemes/GPIO.red" target="_blank">there</a>.<br />
<br />
In the short video below, you can find a little pet project meant for testing some of the features. It implements a simple joypad with 4 directions support, a red LED indicating when the pad is active and a green one for notifying when a level is completed. The game is the <a href="https://github.com/hyzwhu/redbox" target="_blank">Red port</a> contributed by Huang Yongzhao of <a href="https://www.softinnov.org/rebol/rebox.shtml" target="_blank">Rebox!</a>, my old clone of BoxWorld written in Rebol. In the video below, it is running on a Raspberry Pi 3 using our work-in-progress <a href="https://github.com/red/red/tree/GTK" target="_blank">red/GTK</a> backend for Red (contributed by Rcqls), locally merged with the red/port-type development branch (EDIT: that branch has been merged into master now).<br />
<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<iframe allowfullscreen="" class="YOUTUBE-iframe-video" data-thumbnail-src="https://i.ytimg.com/vi/Gqc1nz61PtU/0.jpg" frameborder="0" height="266" src="https://www.youtube.com/embed/Gqc1nz61PtU?feature=player_embedded" width="320"></iframe></div>
<br />
<br />
You can find the breadboard layout below made using <a href="http://fritzing.org/" target="_blank">Fritzing</a>. Sorry for the messy wiring, it is my first try with such kind of tool. If you have the skills to improve it, here is the <a href="https://static.red-lang.org/sketches/RPi3-joypad.fzz" target="_blank">sketch file</a>. The buttons rely on the internal pull-down resistors. Note that in the video, the board is reversed.<br />
<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="/images/blog/RPi3-joypad_bb.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="1377" data-original-width="1080" height="400" src="/images/blog/RPi3-joypad_bb.png" width="311" /></a></div>
<br />
The source code of Redbox has been modified to add GPIO support, you can find the modified code <a href="https://gist.github.com/dockimbel/46b358bdda64f60c7f7aaa9e2bc32033" target="_blank">here</a>. The GPIO-related code is enclosed in a context:<br />
<br />
<pre class="code">    joypad: context [
        mapping: [
            16 down  20 up
            17 left  21 right
        ]

        row: [(id) state: #[false] direction: (direction)]
        table: collect [
            foreach [id direction] mapping [keep compose row]
        ]

        pins: extract table length? row
        port: none

        acquire: has [pin][
            port: open gpio://
            foreach pin pins [
                insert port [
                    set-mode  pin in
                    pull-down pin
                ]
            ]

            insert port [
                set-mode 18 out
                set-mode  4 out
                set 4 on
            ]
        ]

        pressed?: function [][
            foreach pin pins [
                entry: find table pin
                old: entry/state

                insert port [get pin]
                entry/state: make logic! port/data

                ;-- detect 0-to-1 transitions only, to avoid auto-firing
                if all [not old entry/state][return entry/direction]
            ]
            none
        ]

        show-win: does [insert port [set 18 on]]

        release: does [
            insert port [
                set  4 off
                set 18 off
            ]
            close port
        ]
    ]

</pre>
<br />
The GPIO port has a simple API:<br />
<br />
<ul>
<li>opening: <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">port: open gpio://</span></li>
<li>sending commands: <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">insert port [...commands...]</span></li>
<li>closing: <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">close port</span></li>
</ul>
<br />
The sent commands form a small DSL:<br />
<pre class="code">Set the working mode for a given pin:
 
    set-mode &lt;pin&gt; &lt;mode&gt;

    &lt;pin&gt; : pin number (integer!)
    &lt;mode&gt;: in, out, pwm

Write a value on a pin: 
 
    set &lt;pin&gt; &lt;value&gt;
  
    &lt;pin&gt;  : pin number (integer!)
    &lt;value&gt;: true, false, on, off, yes, no, 0, 1

Read a value from a pin (the returned value is in port/data):

    get &lt;pin&gt;

    &lt;pin&gt;: pin number (integer!)    

Manage pull-up/down resistors:

   pull-off &lt;pin&gt;    ;-- disable any pull previously set
   pull-down &lt;pin&gt;   ;-- activate pull-down on the given pin
   pull-up &lt;pin&gt;     ;-- activate pull-up on the given pin   

Write a PWM value on a pin:

   set-pwm &lt;pin&gt; &lt;value&gt;
 
   &lt;pin&gt;  : pin number (integer!)
   &lt;value&gt;: an integer between 0 and 1024, or a percentage for duty cycle.

Fade in/out values on a PWM pin:

   fade &lt;pin&gt; from &lt;start&gt; to &lt;end&gt; &lt;delay&gt;   

   &lt;pin&gt;  : pin number (integer!)
   &lt;start&gt;: starting value (0-1024)
   &lt;end&gt;  : ending value (0-1024)
   &lt;delay&gt;: duration of the whole fading (time!)

Wait for a given duration:

   pause &lt;delay&gt;

   &lt;delay&gt;: integer =&gt; pause in miliseconds, float =&gt; pause in seconds.
</pre>
<br />
<u>Important notes</u><br />
<ul>
<li>Only BCM numbering for GPIO pins is supported.</li>
<li>A word, or path or paren expression containing regular Red code can be used in place of any numeric value.</li>
<li>A single command block can contain an arbitrary number of commands.</li>
<li>The <span style="color: #6aa84f;"><span style="font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">get</span>&nbsp;</span>command can be used multiple times, a block of corresponding results will then be returned in <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">port/data</span>.</li>
<li>Use <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">sudo</span>&nbsp;when running your GPIO code if it involves PWM!</li>
<li>An example of using <span style="color: #6aa84f;"><span style="font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">fade</span>&nbsp;</span>and other commands is available&nbsp;<a href="https://github.com/red/red/blob/master/environment/schemes/GPIO.red#L511" target="_blank">here</a>.</li>
<li>The PWM range is currently preset to 1024, though, the DSL can be trivially extended to allow a user-provided range value.</li>
</ul>
<br />
Happy hardware hacking! ;-)<br />
<br />
{{< /rawhtml >}}