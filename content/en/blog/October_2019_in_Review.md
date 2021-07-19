---
date: 2019-10-25T13:52:27-05:00
title: October 2019 In Review
author: Lucinda Knapp
category: update
tags:
  - update
  - lexer
  - contributors
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---

{{< rawhtml >}}
Over the last few weeks the Red Lang core team drilled down to make some truly great progress on Red's fast-lexer branch--while we also gained valuable support from the contributions of Red doers and makers as they consolidate a world of useful information and resources.<br />
<b><br /></b>
<br />
<h3>
<span style="font-weight: normal;">Fast-Lexer Benchmarks</span></h3>
<br />
In the  <a href="https://github.com/red/red/tree/fast-lexer">fast-lexer branch</a>   of Red, you can see lots of new work from Red creator  <a href="https://github.com/dockimbel">@dockimbel (Nenad Rakocevic</a>)&nbsp;and core teammate  <a href="https://github.com/qtxie">  @qxtie</a>.  Among other fixes and optimizations, they substituted a hashtable for what had previously been a large array in <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">context!</span><br />
<br />
The numbers so far: Loading 100'000 words (5 to 15 characters, 1MB file): 
Red (master): 19000ms.&nbsp; Red (fast-lexer): 150ms. Nenad's observations on further testing:<br />
<blockquote class="tr_bq">
<i>"FYI, we just [ran] some simple benchmarks on the new low-level lexer for Red using 1M 10-digit integers. The new lexer completes the loading about 100 times faster than the current high-level one. Loading 1M 10-digit integers in one block: Red: 175ms; R2: 136ms; R3: 113ms.&nbsp;</i></blockquote>
<blockquote class="tr_bq">
<i>"We use a faster method than Rebol, relying on several lookup tables and a big FSM with pre-calculated transition table (while Rebol relies on a lot of code for scanning, with many branches, so bad for modern CPU with branch predictions). With an optimizing backend, Red's LOAD should in theory run 2-3 times faster than Rebol's one. (Though, we still need to optimize the symbol table loading in order to reach peak performance).&nbsp; Given that Rebol relies on optimized C code while Red relies on sub-optimal code from R/S compiler, that speaks volume about the efficiency of our own approach. So, Red/Pro should give us a much faster LOAD.</i></blockquote>
<blockquote class="tr_bq">
<i>"The lexer is not finished yet, but the hard part is done. We still need to figure out an efficient way to load keywords, like escaped character names (`^(line), ^(page), ...) and month nouns in dates." </i></blockquote>
This is a huge accomplishment, and it's shaping up to make future goals even more impressive. The  <a href="https://github.com/red/red/tree/fast-lexer">  fast-lexer branch</a> is a work in progress, but stay tuned: Nenad has more to say about why it's been prioritized just now, which we will have in an upcoming post.<br />
<b><br /></b>
<br />
<h3>
<span style="font-weight: normal;">Red's MVPs Contribute New Resource Material &amp; Tools</span></h3>
<br />
If you're new to Red, sometimes the flexibility of the language can leave you uncertain about which aggregate structure to use. In <a href="https://github.com/red/red/wiki">red/red's wiki</a> on github, <a href="https://github.com/9214">@9214</a> contributes a useful <a href="https://github.com/red/red/wiki/%5BDOC%5D-Comparison-of-aggregate-values-(block!-object!-hash!-map!)">guide</a> for those seeking to tease apart the differences. For example, <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">map!</span> works better with data that can be atomized, or framed as a conventional associative array, while <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">hash!</span> lends itself to data that will be queried at a high volume and which will require fewer updates. Learn further linguistic nuances, including <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">object!</span> and <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">block!</span>, as well as a useful comparison table of their algorithmic complexity,  <a href="https://github.com/red/red/wiki/%5BDOC%5D-Comparison-of-aggregate-values-(block!-object!-hash!-map!)">here</a>.&nbsp;<a href="https://github.com/rebolek">@Rebolek</a>, meanwhile, has furnished us with loads of useful information, diving deeper into code statistics. His value datatype distribution, <a href="https://gitter.im/red/sandbox?at=5d94a2789d4cf17360577d04">here</a>, his unofficial Red build archive <a href="https://rebolek.com/builds/">here</a>, and his  <a href="https://github.com/rebolek/red-tools">rebolek/red-tools repo</a> containing various tools--line parsers, codecs, APIs and documentation among them--are greatly appreciated. The tools repo has a number of new features you can check out  <a href="https://gitter.im/red/red?at=5daa09d93e33a9652af1c123">here</a>.<br />
<br />
<br />
<h3>
<span style="font-weight: normal;">About Those Ports...</span></h3>
<br />
Wondering about <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">port!</span>?&nbsp;<a href="https://gitter.im/red/red?at=5d94c8289d4cf1736058b0a4">Here's the latest</a>. We've got <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">port!</span> in the master branch already, but low-level input/output networking abilities aren't complete yet, so we need to focus on this, and your feedback can always help. "We have a working async TCP and TLS ports implementation (both client and server-side)," explains Nenad, "but they still require more work to cover all the target platforms." <a href="https://gitter.im/red/red?at=5d94c8289d4cf1736058b0a4">Here</a>, he goes on to explain the prerequisites for our team to complete this process; your thoughts and code contributions are welcomed.<br />
<br />
<br />
<h3>
<span style="font-weight: normal;">Games and Experiments</span></h3>
<br />
It's <a href="https://gitter.im/red/red/gui-branch?at=5d91f526fcb47b627fefd967">a fun one</a> to end this update on: Red community member <a href="https://github.com/GalenIvanov">@GalenIvanov</a>'s "Island Alleys," a game of unspooling Hamiltonian paths! A path of this type only allows its line, which inscribes a closed loop, to cross through a vertex within a graph once, a process which can lend itself to neural network-related interpretations. And <a href="https://gitter.im/red/red/gui-branch?at=5d91f526fcb47b627fefd967">@planetsizedcpu</a> offers a wintry little spin on <a href="https://github.com/planetsizecpu/Cave-In">this repo</a>. Enjoy, and thanks to all!
{{< /rawhtml >}}