---
date: 2019-11-20T20:01:17-05:00
title: Editorial: A Brief Essay on Lexical Ambiguity by G. Irwin
author: Gregg Irwin
category: opinion
tags:
  - lexicon
  - ambiguity
  - language
  - design
  - opinion
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---
<i>The original commentary was posted in Red's Gitter channel, <a href="https://gitter.im/red/red?at=5dc32b09ef84ab37860a9b11">here</a>, by Gregg Irwin, one of our core team members, in response to various requests for the ability to create new datatypes in Red.</i><br />
<i><br /></i>
<i>As a writer, Red has always appealed to me because of its flexibility; but, of course, "the <a href="https://youtu.be/08MqYvU-yuM">[lexicon] devil</a> is in the details," as the idiom goes (okay, I edited that idiom a little, but it was too cool a link to pass up). It means the more specific we try to be, the more challenges and limitations we encounter, and we can lose some of the amazing versatility of the language. On the other hand, precision and refinement--the "exact right word at the exact right time," can powerfully enhance a language's utility. The dynamic tension between what he calls "generality and specificity, human friendliness and artifice," in the text below, can be an energetic ebb and flow that serves to strengthen our language, to make it more robust.&nbsp;</i><br />
<i><br /></i>
<i>Two quotes from community members provide some context:</i><br />
<div style="text-align: center;">
<i>_____________________________</i></div>
<br />
<div style="text-align: center;">
&gt; The real problem is not number of datatypes, but the lexical syntax of the new ones. -@Oldes</div>
<div style="text-align: center;">
<br /></div>
<div style="text-align: center;">
&gt; ...However if something like<span style="font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;"> <span style="color: lime;">utype!</span></span> is added, nothing prevents you from (ab)using <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">system/lexer/pre-load</span> and reinventing whole syntax. -@Rebolek</div>
<br />
<br />
"I don't support abusing <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">system/lexer/pre-load</span>, and (in the long view) there will almost certainly be special cases where a new lexical form makes sense. We can't see the future, so we can't rule it out. But, and this is key, how much value does each new one add?<br />
<br />
I believe that each new lexical form adds less value, and there is a point of diminishing returns. This is not just a lexical problem for Red, but for humans. We have limited capacity to remember rules, and a constrained hierarchy helps enormously here. Think more like linguists, and less like programmers or mathematicians.<br />
<br />
In language we have words and numbers. Numbers can be represented as words, with their notation being a handy shortcut for use in the domain of mathematics. And while we classify nouns, verbs, and adjectives by their use, they are all words, and don't have syntax specific to their particular part of speech. That's important because a single word may be used in more than one context, for more than one purpose.<br />
<br />
This is interesting, as a tangent, because human language can be ambiguous, though some synthetic languages try to eliminate that (e.g. Lojban). The funny thing is that it's almost impossible to write poetry or tell jokes in Lojban. Nobodyº speaks Lojban. This ties to programming because, while we all know the strengths and value of strict typing, and even more extreme features and designs meant to promote correctness, dynamic languages are used more at higher levels<i> [such as poetry, songwriting and humor, where even the sounds used in one single word can be employed to evoke specific emotive responses in the listener--the effects of devices like assonance, consonance, and loose associations we make with even single letters, in the way a repeated letter R throughout a line of poetry or literature can subtly impart a sense of momentum and intensity to the text...possibly because it evokes a growl... -Ed.]</i>. Why is that? Humans.<br />
<br />
When Carl designed Rebol, it had a goal, and a place in time. He had to choose just how far to go. Even what to call things like <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">email!</span>, which are very specific to a particular type of technology. This is what gives Redbol langs so much of their power. They were designed as a data format, meant for exchanging information. That's the core. What are the "things" we need to exchange information about with other humans, not just other programmers?<br />
<br />
Do I want new types? I'm pushing for at least one:&nbsp;<span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">Ref!</span> with an <span style="color: red;">@some-name-here</span> syntax. It's not <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">username!</span> or <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">filename+line-number!</span>, or specific in any way. It's very general, as lexical types should be; their use and meaning being context-specific (the R in Redbol, which stands for "relative"). I also think<span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;"> ~ </span>could be a leading numeric sigil to denote approximation. It came mainly from wanting a syntax for floats, to make it clear that they are imprecise; but it's tricky, because it could also be much richer, and has to take variables into account. <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">~.1</span> is easy, but what about <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">x = ~n+/-5%</span>? Units are also high value, but they are just a combination of words and numbers. (Still maybe worth a lexical form.)<br />
<br />
When we look at what Red should support, and the best way to let users fulfill application and purpose-specific needs, we can learn from the past, and also see that there is no single right answer. Structs, Maps, Objects, data structures and functions versus OOP, strict vs dynamic.<br />
<br />
As Forth was all about "Build a vocabulary and write your program in that," think about what constitutes a vocabulary; a lexicon. It's a balance, in Red, between generality and specificity, human friendliness and artifice. So when we ask for things, myself and Nenad included, we should first try to answer our need with what is in Red today, and see where our proposed solution falls on the line of diminishing returns. To this end, we can and should abuse <span style="color: lime; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">system/lexer/pre-load</span> for experimentation."
