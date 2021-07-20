---
date: 2019-02-14T20:01:17-05:00
title: January 2019 Update
author: 9214 and Gregg Irwin
category: update
tags:
  - relocation
  - core team
  - GTK
  - View
  - GUI
  - Rebol
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---

{{< rawhtml >}}
<br />
<br />
<h2>
Stepping-up</h2>
<br />
2019 started with continued advances in the main development branch, implementation of features, and triage of pending tickets. For example, smart merging of a style's actors with the actors of a particular face instance was introduced in the&nbsp;<a href="https://www.red-lang.org/2016/03/060-red-gui-system.html">VID dialect</a>.&nbsp;Example:<br />
<br />
<pre><code>view [
    style my-button: base
        on-down [face/color: face/color / 2 do-actor face event 'click]
        on-up   [face/color: face/color * 2]

    my-button "Say hi!" red on-click [print "hi"]
]
</code></pre>
<br />
But this is just a tiny drop in the January ocean, and nothing special in the grand scheme of things. More than 50 commits to the mainline, lots of doc updates, and many improvements to the Red Wallet, which we'll talk about in another blog post. On the other hand, Red's progress is rarely trivial and silky smooth, and <a href="https://github.com/red/red/issues/3692#issuecomment-450722963">this write-up</a> gives a deeper insight into our daily routine. Well, what did you expect, Pumpkin Juice? ;-)<br />
<br />
Alas, as much as we love coding, organizational heavy-lifting needs to be done too — one of our short-term priorities this year is relocation of core team to Europe, and (ongoing) activity on this front took a lot of our time and resources in January. That is to say, after little overture, the core team's main activity shifted behind the scenes, giving the stage to our outstanding community's efforts. <sup><a href="https://www.red-lang.org/2019/02/january-2019-update.html#footnote-1">1</a></sup><br />
<br />
<h2>
</h2>
<h2>
</h2>
<h2>
Community highlights</h2>
<h2>
</h2>
<h3>
GTK backend</h3>
<br />
Red strives to be a truly cross-platform language, but the&nbsp;<a href="https://trello.com/b/FlQ6pzdB/red-tasks-overview">project's roadmap</a> always implies a certain order of priorities, where some milestones come later than others. One such missing cross-platform feature is the View engine's backend for Linux — its development requires dedicated resources, which the core team cannot fully afford, probably until near the 1.0 release.<br />
<br />
With that in mind, it is much to our delight that <a href="https://github.com/red/red/pull/3718">development of GTK backend</a> is being carried out as a dedicated community effort. We'd like to take an opportunity and thank all the people participating in it — their proactive contributions make Red a truly open-source project, and help us to advance it towards our collective vision. Big thanks to&nbsp;<a href="https://github.com/rcqls">@rcqls</a>&nbsp;for taking the lead on this.<br />
<br />
Last but not least, you can track development's progress in a recently created <a href="https://gitter.im/red/GTK">GTK room</a>. Don't forget to visit it and give our contributors all the praise they deserve! Or even better — become one of them and get a share of fame and glory! ;-)<br />
<br />
<br />
<h3>
</h3>
<h3>
</h3>
<h3>
View and Rich-text tweaking</h3>
<br />
Not only do missing parts of the View engine get developed, but existing ones receive thorough maintenance too. Features <i>and</i> fixes.<br />
<br />
Among fixes are&nbsp;<code>base</code> and <code>text</code> rendering, Red's codebase received a <a href="https://github.com/red/red/pull/3683">contribution</a> for testing of image-related features on Windows platforms, accompanied by more than 300 tests. Coupled with our <a href="https://github.com/red/red/tree/master/modules/view/backends/test">"null" testing backend</a> (covered in some detail in <a href="https://www.red-lang.org/2017/07/063-macos-gui-backend.html">here</a>) this casts a wide net for catching regressions in View.<br />
<br />
After the&nbsp;<a href="https://www.red-lang.org/2018/12/064-simple-gc-and-pure-red-gui-console.html">0.6.4 release announcement</a>, many users checked out rich-text support and gave Red's&nbsp;<a href="https://github.com/red/red/wiki/%5BDOC%5D-Rich-Text-support">Rich-text dialect</a> a proper spin, with numerous <a href="https://github.com/red/red/pull/3698">bug fixes and tweaks</a> being submitted in the process.<br />
<br />
<br />
<h3>
</h3>
<h3>
</h3>
<h3>
</h3>
<h3>
Editing, with a capital E</h3>
<br />
As you can see from the above, native GUI support is one of our strongest aspects, which piques the interest of many community members.<br />
<br />
Another special feature that catches everyone's fancy is Red's <a href="https://en.wikipedia.org/wiki/Homoiconicity">"code as data"</a> nature. But, while giving Red enormous expressive power (metaprogramming and the creation of domain-specific languages, DSLs for short), it makes some things trickier — with the boundary between code and data being blurred, and multiple dialects (our term for embedded DSLs) at one's disposal, it is extremely challenging to assign any particular meaning to a given piece of code (data!); both for humans (esp. newr Red programmers) and automatic tools, such as syntax highlighters, static code analyzers, debuggers and linters.<br />
<br />
Historically, this was the main argument when it came to Rebol's tooling. Sprinkling your code with <code>print</code> and <code>probe</code> is still the most common debugging method, and error reporting boils down to stack traces rather than source text info; text editing support can accommodate only cosmetic niceties like "keywords" highlighting and indentation, covering only general subset of the language.<br />
<br />
Being a direct descendant of Rebol, we carried over this bag of concerns, aiming to resolve them at some point in development. A quite natural answer to points raised would be an editor written in pure Red and its dialects, integrated in our self-contained toolchain.<br />
<br />
And while writing a basic version of such editor is <a href="https://www.red-lang.org/2016/07/eve-style-clock-demo-in-red-livecoded.html">rather trivial</a>, such a naive approach leaves much to be desired, and keeps questions about proper tooling surrounded with an air of uncertainty, begging for a detailed investigation. Thankfully, this is where community projects and experiments come to the rescue!<br />
<ul>
<li>
<strong><code><a href="https://github.com/rebolek">@rebolek</a></code></strong>'s <a href="https://gitlab.com/rebolek/values">Values</a>, announced at last year's <a href="https://www.red-lang.org/2018/11/redcon-1-and-ethereum-devcon-4-world.html">RedCon</a>, is a sophisticated <a href="https://en.wikipedia.org/wiki/Structure_editor">projectional editor</a> with Vim's flavor and an ingenious schtick — rather than working with textual form, it <code>load</code>s a program and directly manipulates its internal data structure (a <code>block!</code> of <em>values),</em> reflecting all changes back in the text area.<br /><br />Idiomatically written, and offering sheer power in a few keystrokes, it struck us in awe back at RedCon, and stimulated a lot of technical discussions. With our <a href="https://www.red-lang.org/2018/12/064-simple-gc-and-pure-red-gui-console.html">new GUI console</a>'s plug-in API on its way for 0.6.5 release, we are eager to see how it will get integrated in day-to-day user experience, and what fresh insights it can bring to all of us.<br />

</li>
<li><strong><code><a href="https://github.com/toomasv">@toomasv</a></code></strong> is well-known in our community as an avid Draw and View tinkerer, and his recent <a href="https://github.com/toomasv/syntax-highlighter">experiment</a> only firms this reputation.<br /><br />Datatype-aware syntax highlighting, contextual help, auto-completion, step-by-step evaluation and bunch of other niceties — all in ~1K lines of code! Magic, you say? No, Reducing at its finest. ;-)</li>
</ul>
<div class="separator" style="clear: both; text-align: center;">
<a href="http://vooglaid.ee/red/syntax4.gif" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" src="http://vooglaid.ee/red/syntax4.gif" data-original-height="497" data-original-width="704" height="449" width="640" /></a></div>
<br />
<br />
Projects like this (and all others that we didn't get a chance to mention) aren't just eye-candy for the public — they help us, core developers, to evaluate all options and to revisit old ideas in a new light. Besides, it's extremely rewarding to see Red (in its <em>alpha</em> stage) being put to real use.<br />
<br />
Once again, our cheers go to all the people who dedicate their time and efforts to support us. No matter how small your contribution, it makes Red stronger and readier for the prime-time: day by day, bit by bit.<br />
<br />
<h2>
</h2>
<h2>
</h2>
<h2>
C3 project</h2>
<br />
Since the core team relocation is our ongoing No.1 priority, development of the C3 project got sidetracked a bit. There are still a few final touches that need to be done (e.g. finishing AST parser, <code>hex!</code> and <code>bigint!</code> datatypes support) but, aside from that, the first alpha version of compiler is almost ready for a public release. The first 90% of a task takes 90% of the time, the last 10% takes the other 90%.<br />
<br />
In the meantime, we have one appetizer to serve: RedCon talk about C3! Due to technical issues and time constraints, it became available only recently, and was captured on a nearby web-camera. Because of that, video quality and recording angle are so-so, but the good news is that you can gain a deeper insight into the blockchain aspect of Red... and witness the talking belly. :-)<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<iframe allowfullscreen="" class="YOUTUBE-iframe-video" data-thumbnail-src="https://i.ytimg.com/vi/HwYkrHDe0M8/0.jpg" frameborder="0" height="266" src="https://www.youtube.com/embed/HwYkrHDe0M8?feature=player_embedded" width="320"></iframe></div>
<br />
<br />
As evident from the talk<a href="https://www.red-lang.org/2019/02/january-2019-update.html#footnote-2"><sup>2</sup></a>, C3's design proved to be much more challenging than we initially anticipated, muddled by pesky EVM (Ethereum Virtual Machine) constraints (like gas), lack of good reference documentation, complex tooling and blockchain hype haze.<br />
<br />
At this point, we're convinced that <em>at least two</em> layers are required for C3 to be a sound smart-contract development solution:<br />
<ol>
<li>The low-level one, named <em>C3/System</em>, is a language with simple semantics (close to Solidity, but without foot-shooting), serving as a base for building high-level dialects on top of it. We also want to implement a couple of experimental features, like off-chain Cron-like scheduler of Smart Contract execution and embedded FSM (finite-state machine) sub-dialect.</li>
<li>Possibly <em>multiple</em> high-level layers, each covering different blockchain aspect and tailored to specific solutions: creation of crypto tokens, gambling, in-game collectibles, legal contracts and business logic, bids and auctions, asset tracking... who-knows-what people may come up with.</li>
</ol>
Despite all the media craze surrounding blockchains, the technology itself is still in a nascent state, constantly searching for a real-world use-case. Because of that, navigating this new and constantly shifting space (not to mention building a development platform like C3) is like sailing in stormy weather.<br />
<br />
In light of the above, we owe much to<a href="https://github.com/9214"> <strong><code>@9214</code></strong></a> for his help with C3 preliminaries and conducting in-depth research on Smart Contract languages. His constant background presence affirmed many of our assumptions, and guided us past many reefs and pitfalls.<br />
<br />
Back in the day, our&nbsp;<a href="https://www.red-lang.org/2017/12/leaping-into-future-red-goes-blockchain.html">"Red goes blockchain"</a>&nbsp;announcement generated much controversy, and prompted many people (both community members and outsiders) to cast their doubts on this decision. Some go as far as to dismiss the Red project entirely, based on our new roadmap.<br />
<br />
Yet, very few realize that, in some sense, we're picking up the game that Rebol left — with Carl's conception of <a href="http://www.rebol.com/news/news3404.html">X-Internet</a><a href="https://www.red-lang.org/2019/02/january-2019-update.html#footnote-3"><sup>3</sup></a> replaced by decentralized consensus-driven P2P networks, and EVM instead of <a href="http://www.rebol.com/ios/ios-intro.html">IOS</a>. Indeed, Smart Contracts are just very limited...slow&nbsp;<a href="http://www.rebol.com/reblets.html">Reblets/services</a>&nbsp;in disguise ;-) And behind blockchain fatigue lies the brave new world, where Red can be the missing puzzle piece and stepping stone towards simple, human-friendly tooling.<br />
<br />
All in all, we hold to our beliefs, and going to play this card, aiming to hit the jackpot. But we're also not putting all our eggs in one basket. Bear with us as we tread forward, and stay tuned for future updates!<br />
<br />
<h2>
</h2>
<h2>
</h2>
<h2>
Wrapping-up</h2>
<br />
January, with its holidays and family reunions, is nothing but a calendar sheet. The work on Red never ceases, spans through weekends, occupies all time and space (both physical and mental) and now reaches across the globe. For some, it became the animating principle of their lives.<br />
<br />
With our hard work at stake, and with 1.0 release in near sight, encounters with the outside world get more frequent and progressively challenging — criticism and cross-checks with reality are important, but it's equally important to apply a fair yardstick, and judge the project on its own merits.<br />
<br />
That's why, when it comes to media coverage and public discussions, we expect outsiders to stay open-minded and not to cast aspersions lightly. We want Red to succeed, and welcome technical debate and comparisons with other projects (like, e.g., <a href="https://www.reddit.com/r/redlang/comments/aebxct/contrast_red_with_racket/edoerll/">Red vs. Racket</a>; again, kudos to <strong><code>@9214</code></strong> for writing such a well-articulated response). But, more often than not, discussion threads turn into exercises at damage control, with constructive points being hamstrung and torn to pieces in a cross-fire.<br />
<br />
Our mission to fight software complexity is challenging, and not for the faint-hearted. Remember — the best way to prove one's case is not in word, but in deed... and the strongest argument is a tech-savvy pull-request. ;-)<br />
<br />
Come to think of it, I can't help remembering Pierre Rabhi's tale:<br />
<blockquote class="tr_bq">
Once upon a time, the scorching fire swallowed the forest. All the animals, terrified and powerless, watched it destroying their homes from afar. Only little Hummingbird kept flying back and worth between the fire and nearby pond, carrying tiny drops of water in its beak and throwing them in the flames.&nbsp;&nbsp;</blockquote>
<blockquote class="tr_bq">
Irritated by bird's constant flickering, grouchy Armadillo yelled: "Hummingbird! Don't you see that your pathetic attempts won't save the forest?"</blockquote>
<blockquote class="tr_bq">
"I know.", answered Hummingbird, "but I'm doing my part."</blockquote>
<br />
Hectic 2018 barely passed by, but we're already steering wheels on our <a href="https://www.red-lang.org/2019/01/full-steam-ahead.html">new roadmap</a>. There is more news to announce, once the dust has settled. We'll be in touch. Until then, Happy Reducing!<br />
<br />
<em>-- Post by 9214, edits and amendments by Gregg</em><br />
<h2>
<em><br /></em></h2>
<h2>
<em>Footnotes</em></h2>
<ol>
<li><a href="https://www.blogger.com/null" name="footnote-1"></a> Remember that you can track progress of Red projects (both community-driven and official ones) at <a href="https://progress.red-lang.org/"></a><a href="https://progress.red-lang.org/">https://progress.red-lang.org/</a></li>
<li><a href="https://www.blogger.com/null" name="footnote-2"></a> Reminder: C3 presentation slides in PDF format are available <a href="https://static.red-lang.org/C3/Red-C3.pdf">here</a>.</li>
<li><a href="https://www.blogger.com/null" name="footnote-3"></a> "X" here stands for eXecutable and eXtendable.</li>
</ol>
<br />
{{< /rawhtml >}}