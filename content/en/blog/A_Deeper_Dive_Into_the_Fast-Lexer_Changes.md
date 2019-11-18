---
date: 2019-10-30T20:01:17-05:00
title: A Deeper Dive Into the Fast-Lexer Changes
author: Lucinda Knapp
category: update
tags:
  - lexer
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---
<h3 style="text-align: left;">
What made the fast-lexer branch a priority?</h3>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
Several things. It started when <a href="https://github.com/dockimbel">@dockimbel</a> looked into ticket <a href="https://github.com/red/red/issues/3606">#3606</a>, which was impossible to fix currently, and we didn't want to give up on the auto-syncing between <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">/text</span>&nbsp;and <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">/data</span>&nbsp;facets. So he had to consider bigger options, including how to make the lexer instrumentable. It was not easy, because the current lexer is not re-entrant, so having the lexer emit events to a callback function could have caused serious problems.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
Digging through all Red's repos showed that the current lexer code was duplicated twice, beyond the basic lexing needed by <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">load</span>: once in the console code, once in the VSCode plugin, each time for syntax coloring purposes, and each one lagging behind the original implementation. Not good.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
<a href="https://github.com/dockimbel">@Dockimbel</a> then considered changing the current lexer to make it instrumentable, but the changes were significant and would have made the parse rules much more complex. At the same time, <a href="https://github.com/qtxie">@qtxie</a> did some benchmarking, and the result showed Red's lexer was ~240 times slower than Rebol's. This is not due to <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">parse</span>, but&nbsp; rather because the high-level rules were optimized for readability, not performance.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
The lexer also caused delays in the VSCode plugin, because of its (lack of) performance. The high level code has served Red well, and was a showcase for <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">parse</span>, but <span style="color: #93c47d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">load</span>ing larger data is also being used by community members, and data sizes will just keep growing. With some projects we have on the horizon, the lexer's performance became a higher priority.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
As planned since the beginning (the lexer used to be R/S-only during the pre-Unicode era), <a href="https://github.com/dockimbel">@dockimbel</a> decided the best option was to not postpone the conversion of the lexer to pure R/S code any longer, by porting R3's C-based lexer to R/S. After studying Rebol's lexer in detail, he realized that the code was quite complex in some places (mostly the prescanner), and would lead to less than optimal R/S code that would be hard to maintain.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
Evaluating the state of the art in fast parsers for programming languages, he found inspiration in some unpublished papers. He then started prototyping the next lexer in R/S, and realized that it could be several times faster than Rebol's, with the additional benefit of much smaller and simpler code. Then he embarked on the full implementation. Knowing he and&nbsp;<a href="https://github.com/qtxie">@qtxie</a>&nbsp;would not have the opportunity to work on that for probably a year with all the big tasks ahead on the roadmap, he committed to it full time.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
Red's new R/S lexer is half the size of Rebol's, far simpler, with more maintainable code, and it performs at similar speeds (sometimes a bit faster, sometimes a bit slower). That is a fantastic result, because it means that with an optimizing backend (Red/Pro), our lexer will be 4-8 times faster than R3's. It should then be possible to load gigabytes of Red data in memory in just a few</div>
<div style="text-align: left;">
seconds (using the future 64-bit version). 😉</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
An additional benefit was brought by&nbsp;<a href="https://github.com/qtxie">@qtxie</a>, who added a hashtable for symbol lookup in Red contexts. That sped up word loading tremendously, and should have a measurable improvement on Red's start up time; especially on slow platforms like Raspberry Pi.</div>
<div style="text-align: left;">
<br /></div>
<div style="text-align: left;">
<a href="https://github.com/dockimbel">@Dockimbel</a>&nbsp;is almost done with the lexer itself, just <span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">date! </span><span style="font-family: inherit;">and</span><span style="color: #6aa84f; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;"> time!</span> to add, and it should be possible to replace the old one with the new one after thorough testing and debugging. Then, we'll add the hooks for a user-provided callback, allowing us to instrument the lexer in ways Redbolers could only dream about until now. One application of that will be the ability to implement "predictive loading," which will tell you the type and size of a Red value in a string, without loading it, and at extremely high speed (~370MB/s currently, 1-2GB/s with /Pro). Such a feature will allow us to finally address the <a href="https://github.com/red/red/issues/3606">#3606 issue</a>&nbsp;with a very clean and efficient solution, while keeping the facet's auto-syncing feature.</div>
<div style="text-align: left;">
<br /></div>
