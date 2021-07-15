---
date: 2019-06-30T20:01:17-05:00
title: June 2019 Update
author: Nenad Rakocevic
category: update
tags:
  - development
  - RED Wallet
  - bitcoin
  - SegWit
  - Android
  - ETH
  - GTK
  - Trezor
  - Red/C3
  - Red/System
  - Raspberry Pi
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---

If you are an active member of the Red community, you will have likely been keeping track of Red's progress through our Gitter rooms and Github repositories, but we wanted to officially bring everyone up to speed with a shiny new blog post. The team has been busy since January on many fronts, multiplexing its efforts on many different branches of development. Here is an overview of what we have been cooking and what is coming.<br />
<br />
<span style="font-size: large;">RED Wallet</span><br />
<br />
We are preparing to release v0.4.0 of the <a href="https://www.red-lang.org/2018/06/red-wallet-tiny-simple-fast-and-secure.html" target="_blank">RED Wallet</a>&nbsp;which will feature:<br />
<ul>
<li>Bitcoin support with both Legacy and SegWit addresses!</li>
<li>Updated support for ERC-20 tokens for Ledger Nano keys (after Ledger externalized such token management to the wallet software earlier this year).</li>
<li>Support for the latest firmware of the Trezor key.</li>
<li>Some bug fixes.</li>
</ul>
The new wallet is currently under heavy testing, we plan to release it publicly in about a week.<br />
<br />
<span style="font-size: large;">C3</span><br />
<br />
The first public alpha of the C3/System compiler is coming this summer. It is still under heavy development though. C3/High has made little progress as it needs real-world use-cases from the smart contract ecosystem for modelling the DSL(s). That ecosystem has not spread around much, probably due to the so-called "crypto-winter". As new big players are now entering the space, we are looking forward to the possibilities for providing new backends for the C3/System, like for the <a href="https://libra.org/en-US/open-source-developers/" target="_blank">Libra</a> network.<br />
<br />
We will be soon releasing our ETH connector for Red. The final part missing is the integration of hardware and software key support for signing transactions on real online networks (we use private networks during development). The code for hardware key support is already there in our wallet, so we just need to integrate it inside the connector. For software keys, we have developed specific&nbsp;<a href="https://github.com/bitbegin/eth-wallet" target="_blank">support</a>&nbsp;for them, but it relies on third-party libraries, which are currently not a good match for our single binary distribution model.<br />
<br />
<span style="font-size: large;">GTK support</span><br />
<br />
Red should offer soon a pretty good GUI backend for Linux, thanks to the community effort led by <a href="https://github.com/rcqls" target="_blank">R cqls</a>. The <a href="https://github.com/red/red/pull/3928" target="_blank">last PR</a> for red/GTK branch weighs in at about 400 commits and covers most of View features.<br />
<br />
The main remaining features to cover are:<br />
<ul>
<li>Camera widget support (already available in an experimental branch)</li>
<li>Rich-text and Draw improvements</li>
<li>Shape dialect support</li>
<li>Some stability fixes</li>
</ul>
<div>
<br />
Here are some examples of scripts and apps using the GTK backend:</div>
<div>
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://files.gitter.im/red/GTK/TGpt/Capture-d_ecran-2019-04-28-a-22.18.03.png" imageanchor="1" style="clear: right; float: right; margin-bottom: 1em; margin-left: 1em;"><img data-original-height="772" data-original-width="800" height="192" src="https://files.gitter.im/red/GTK/TGpt/Capture-d_ecran-2019-04-28-a-22.18.03.png" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="200" /></a><a href="https://files.gitter.im/red/GTK/E9v6/Capture-d_ecran-2019-03-31-a-19.44.04.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img data-original-height="800" data-original-width="537" height="200" src="https://files.gitter.im/red/GTK/E9v6/Capture-d_ecran-2019-03-31-a-19.44.04.png" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="133" /></a><a href="https://files.gitter.im/red/GTK/QbWn/Capture-d_ecran-2019-04-20-a-17.23.42.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img data-original-height="800" data-original-width="666" height="200" src="https://files.gitter.im/red/GTK/QbWn/Capture-d_ecran-2019-04-20-a-17.23.42.png" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="166" /></a></div>
<div class="separator" style="clear: both; text-align: center;">
<br /></div>
<div class="separator" style="clear: both; text-align: left;">
GTK theming is also supported:</div>
<div class="separator" style="clear: both; text-align: left;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://files.gitter.im/red/GTK/n7t0/Capture-d_ecran-2019-04-25-a-13.43.27.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img data-original-height="572" data-original-width="800" height="227" src="https://files.gitter.im/red/GTK/n7t0/Capture-d_ecran-2019-04-25-a-13.43.27.png" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="320" /></a></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://files.gitter.im/red/GTK/vUQT/Capture-d_ecran-2019-04-25-a-13.38.50.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img data-original-height="572" data-original-width="800" height="227" src="https://files.gitter.im/red/GTK/vUQT/Capture-d_ecran-2019-04-25-a-13.38.50.png" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="320" /></a></div>
<div>
<br /></div>
<span style="font-size: large;">Red/System</span><br />
<span style="font-size: medium;"><br /></span>
The ARM backend got many improvements:<br />
<ul>
<li>Largely improved ARMhf (hard-float) support.</li>
<li>Fixes on regressions for ARMsf (soft-float).</li>
<li>Various libraries loading fixes, now all unit tests are passing again.</li>
<li>New ARMhf target added to our <a href="https://travis-ci.org/red/red" target="_blank">Travis CI</a> backend.</li>
</ul>
<br />
A few low-level features were <a href="https://static.red-lang.org/red-system-specs-light.html#section-20" target="_blank">added</a>, that would make it easier to write device drivers or operating systems directly in Red/System:<br />
<br />
<ul>
<li>Ability to save/reload all CPU registers on stack using intrinsics.</li>
<li>Ability to read/write CPU I/O ports using new intrinsics.</li>
<li>Ability to inline machine-code pretty much anywhere in R/S source code.</li>
<li>Replacing hard native support for modulo operation on floats by the soft <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">fmod()</span> import.</li>
</ul>
<div>
<br /></div>
<div>
<span style="font-size: large;">VSCode plugin</span></div>
<div>
<br /></div>
<div>
The <a href="https://marketplace.visualstudio.com/items?itemName=red-auto.red" target="_blank">Red plugin</a> for VSCode got a major refresh with a full <a href="https://github.com/red/VScode-extension" target="_blank">reimplementation</a> using <a href="https://langserver.org/" target="_blank">LSP model</a>&nbsp;improving the efficiency of existing features and adding some new ones:</div>
<div>
<ul>
<li>Smarter code completion</li>
<li>Realtime syntax checking</li>
<li>Goto definition support</li>
</ul>
<div>
<br /></div>
</div>
<div class="separator" style="clear: both; text-align: center;">
<a href="https://raw.githubusercontent.com/red/VScode-extension/master/images/goto-definition.gif" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="677" data-original-width="800" height="168" src="https://raw.githubusercontent.com/red/VScode-extension/master/images/goto-definition.gif" width="200" /></a><a href="https://raw.githubusercontent.com/red/VScode-extension/master/images/completion.gif" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="677" data-original-width="800" height="168" src="https://raw.githubusercontent.com/red/VScode-extension/master/images/completion.gif" width="200" /></a></div>
<div>
<br /></div>
<br />
<span style="font-size: large;">Other WIP features</span><br />
<span style="font-size: large;"><br /></span>
<b>JSON support</b><br />
<br />
JSON format is now <a href="https://github.com/red/red/blob/master/environment/codecs/json.red" target="_blank">supported</a> by Red's codec system. So it can be used in <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">load/as</span> and <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">save/as</span> to convert JSON data back and forth to Red values. More info about its usage in the Red 0.6.5 release notes.<br />
<br />
<b>Shadows in Draw</b><br />
<br />
Some simple shadow effects in Draw have been <a href="https://github.com/bitbegin/red/commits/blur-demo" target="_blank">implemented</a>. They have the capabilities of the <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow" target="_blank">box-shadow</a> model of CSS.<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="https://1.bp.blogspot.com/-GokDUymEu2Y/XRkfsMeZJ3I/AAAAAAAAAdY/aAQ4ZUGNzwYLPTa5o_9srijVRiekscMowCLcBGAs/s1600/photo_2019-06-30_22-46-26.jpg" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img data-original-height="593" data-original-width="1062" height="222" src="https://1.bp.blogspot.com/-GokDUymEu2Y/XRkfsMeZJ3I/AAAAAAAAAdY/aAQ4ZUGNzwYLPTa5o_9srijVRiekscMowCLcBGAs/s400/photo_2019-06-30_22-46-26.jpg" style="-moz-box-shadow: none; -webkit-box-shadow: none; background: none; border: 0; box-shadow: none; padding: 0;" width="400" /></a></div>
<br />
<br />
<b>GPIO library for Raspberry Pi</b><br />
<br />
Red has supported Raspberry Pi as a compilation target for many years, but we were still lacking a proper GPIO library, which is now under development. It will be implemented as a <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">gpio://</span> port for now in the <span style="colour: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">port-type</span> branch. A dedicated library or dialect should be added also as a higher abstraction layer in order to simplify GPIO programming even further. Hobbyists and seasoned programmers will be able soon to build IoT projects on RPi easily using Red with GTK for the GUI support.<br />
<br />
<br />
<span style="font-size: large;">Next Red releases</span><br />
<br />
<b>0.6.5: Splitting the console and compiler</b><br />
<br />
This is an important change that will be the new way to use Red and, hopefully, provide an even better experience, especially for newcomers. Not much coding is involved but we still need a prototype before giving the final go-ahead then proceeding with the code and infrastructure changes. We plan to finish those tasks during this summer (no precise ETA for now).<br />
<br />
<b>0.7.0: Full async I/O</b><br />
<br />
Work started on this release many months ago but with a low-priority, as we have many other features to release first. The current state on the main features is:<br />
<ul>
<li>port! type is almost completed and already usable (e.g. the eth:// port)&nbsp;</li>
<li>the native ports TCP, UDP, DNS should be implemented this summer.</li>
<li>the async API still needs design work before being implemented.</li>
</ul>
<div>
<br /></div>
<div>
<span style="font-size: large;">Tokens retro-distribution</span></div>
<div>
<br /></div>
<div>
We are setting up the last steps for the RED tokens retro-distribution (past contributions) and the first monthly distribution for new contributors. We will publish the first article in July that will provide all the rules that we have established for that process. Then shortly after, we will publish the list of the contributors who were selected according to those rules, with the reward amounts and proceed with the distribution (using the batch transactions feature of the RED Wallet).</div>
<br />
For example, as part of our tokens rewarding program for contributors, R cqls should receive a good amount of them in the next distribution,<br />
<br />
<br />
<span style="font-size: large;">The road ahead...</span><br />
<br />
The most notable next planned milestones are:<br />
<ul>
<li>RED Wallet 0.4.0 in July.</li>
<li>C3/System alpha release in August!</li>
<li>Red/Android beta release in September!</li>
<li>Red/Pro for New year!</li>
<li>Red 64-bit will be split into two phases:</li>
<ul>
<li>cross-compiled from 32-bit platform: end of the year</li>
<li>toolchain ported to 64-bit: 2020</li>
</ul>
</ul>
<br />
We plan to give more information about each of those big new additions to the Red family this summer.<br />
<br />
As several development tracks are coming to fruition in the next couple of months, new articles should come up more frequently.<br />
<br />
Go Red Go!
