---
date: 2017-05-01T20:01:17-05:00
title: Title goes here
author: Gregg Irwin
category: update
tags:
  - blockchain
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---

Hello to all the great makers, doers and creative people who are using Red, helping the Red Language grow and improve!

As always, there's a standing invitation for you to join us on <a href="https://gitter.im/red/help" target="_blank">Gitter</a>, <a href="https://t.me/redofficial" target="_blank">Telegram</a> or <a href="https://github.com/red" target="_blank">Github</a> (if you haven't already) to ask questions and tell us about your Red-powered projects.<br />
<br />
Here are some recent highlights we’d like to share with you:<br />
<br />
<h4>
1. Tickets Get Priority</h4>
In the last month, our core team has closed a large number of tickets.We’d like to thank community members <a href="https://github.com/red/red/issues/4006" target="_blank">rgchris</a>, <a href="https://github.com/red/red/issues/3950" target="_blank">giesse</a>, and <a href="https://github.com/red/red/issues/3915" target="_blank">dumblob</a> who are just a few of the passionate contributors putting Red through its paces and providing feedback as fixes and changes occur. @WArP ran the numbers for us, showing a cyclical growth pattern linking bursts of closed issues and some serious Red progress, and September’s not even done yet!...:<br />
<img height="246" src="https://lh4.googleusercontent.com/YDTKrNALQF7Q_z27RQE1Z9CYPT4rihiZaRcoFG55Jw4MlOVps7NlIH14sVHbns5Qhrq_Khx1UyJq7NshSk9-sZYods6RgfVWUZAEacC7b1oSYU6lqnAz9wFDO-SjDXfU1XECdl4T" style="background-color: white; color: #222222; font-family: arial; font-size: 11pt; margin-left: 0px; margin-top: 0px; white-space: pre-wrap;" title="Chart" width="398" /><br />
<br />
<h4>
2. CSV Codec Available</h4>
Our newly updated&nbsp;<a href="https://github.com/red/red/wiki/CSV-codec" target="_blank">CSV codec</a>&nbsp;has been merged in the master branch and is now a part of the nightly (or automatic) build&nbsp;<a href="https://www.red-lang.org/p/download.html" target="_blank">here</a>. It is in an experimental phase, and we want your&nbsp;<a href="https://gitter.im/red/red" target="_blank">feedback</a>.<br />
<br />
Should the standard codec only support block results, so it’s as simple as possible? Or do people want and need record and column formats as well (using the <span style="color: #38761d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">load-csv/to-csv</span>&nbsp;helper funcs, rather than <span style="color: #38761d; font-family: &quot;courier new&quot; , &quot;courier&quot; , monospace;">load/as</span>)? Including those features as standard means they’re always available, rather than moving them to an extended CSV module; but the downside is added size to the base Red binary.<br />
<br />
Applause goes to @rebolek’s excellent organization and his <a href="https://github.com/red/red/wiki/CSV-codec" target="_blank">wiki</a> on the codec, which explains the various ways in which Red can represent data matrices. He writes, “Choosing the right format depends on a lot of circumstances, for example, memory usage - column store is more efficient if you have more rows than columns. The bigger the difference, the more efficient.”<br />
<br />
You can judge their efficiency <a href="https://gist.github.com/rebolek/e9c718175a0c60c1ec1a6e1a97d8cd2c" target="_blank">here</a>, where @rebolek has laid out the compile time, size and speed of each version, including encapping and lite. Be sure to get the <a href="https://www.red-lang.org/p/download.html" target="_blank">latest build</a>, and chat with everyone on <a href="https://gitter.im/red/red" target="_blank">Gitter</a> to tell us what you think.
<br />
<br />
<h4>
3. Red has reached <a href="https://github.com/red/red/stargazers" target="_blank">4K stars</a> on GitHub!</h4>
We’re truly grateful for all the interest and support, and we are proud of the way our growth has been powered by this community.<br />
<br />
<h4>
4. AI + Red Lang Stack: Precision Tuning With Local OR Web-Based Datasets</h4>
In conversation with @ameridroid:<br />
“Presently, it seems like most AI systems available today either allow building an AI from scratch using low level code (difficult and time-consuming), *OR* using a pre-built AI system that doesn't allow any fine-tuning or low-level programming...with the advent of NPUs (Neural Processing Units) akin to CPUs and GPUs, an AI toolkit would allow specifying what type of AI we want to perform (facial, image or speech recognition, generic neural net for specialized AI functions, etc.), the training data (images, audio, etc.) and then allow us to send it the input data stream and receive an output data stream…[using Red] would also allow us to integrate with the AI system at a low level if we have specific needs not addressed by the higher-level funcs. Red dialects would be a good way to define the AI functionality that's desired (a lot like VID does for graphics), but also allow the AI components, like the learning dataset or output data stream sanitization routines, to be fine-tuned via functions. Red can already work on web-based data using 'read or 'load, or work on local data in the same way; the learning data for a particular AI task could be located on the web or on the local machine. That's not easily possible with a lot of the AI solutions available today.”<br />
<br />
Check back in the next few days for an update from @dockimbel!<br />
<br />
Ideas, contributions, feedback? Leave a comment here, or c’mon over and join our conversation on&nbsp;<a href="https://t.me/redofficial" target="_blank">Telegram</a>,&nbsp;<a href="https://gitter.im/red/help" target="_blank">Gitter</a>,&nbsp;or&nbsp;<a href="https://github.com/red" target="_blank">Github</a>.
