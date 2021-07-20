---
date: 2019-07-19T20:01:17-05:00
title: RED Wallet 0.4.0
author: Nenad Rakocevic
category: update
tags:
  - blockchain
  - RED Wallet
  - bitcoin
  - token
  - wallet
  - release
hero_type: image
hero_src: https://images.pexels.com/photos/993019/pexels-photo-993019.jpeg?auto=compress&cs=tinysrgb&h=650&w=940
---

{{< rawhtml >}}

We are releasing today the version 0.4.0 of the RED Wallet with several major new features. As a reminder, the RED Wallet aims to be a simple and very secure wallet for the major cryptocurrencies (BTC, ETH, and ERC-20 tokens). Safety is enforced through the mandatory use of a hardware key (Ledger or Trezor keys), which protects against any failure of the wallet app (being it a bug or an attacker). The RED Wallet code is fully written in Red (using the <a href="https://static.red-lang.org/red-system-specs-light.html" target="_blank">Red/System DSL</a> for USB drivers implementation) and <a href="https://github.com/red/wallet" target="_blank">open source</a>.<br />
<br />
<span style="font-size: large;">BTC support</span><br />
<br />
The RED Wallet now supports the bitcoin network. The main features are:<br />
<ul>
<li>retrieval of address balances.</li>
<li>sending transactions (with follow-up on an online block explorer).</li>
<li>support both SegWit and Legacy addresses.</li>
<li>support both mainnet and testnet.</li>
</ul>
<div>
<br /></div>
<div class="separator" style="clear: both; text-align: center;">
<a href="/images/blog/wallet040.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="400" data-original-width="908" height="175" src="/images/blog/wallet040.png" width="400" /></a></div>
<br />
<div class="separator" style="clear: both; text-align: center;">
</div>
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="/images/blog/wallet040-4.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="752" data-original-width="946" height="317" src="/images/blog/wallet040-4.png" width="400" /></a></div>
<br />
The balance retrieval can be quite slow on the bitcoin network, so be patient.<br />
<br />
<br />
<span style="font-size: large;">ERC-20 tokens support</span><br />
<span style="font-size: large;"><br /></span>
ERC-20 tokens are supported since version 0.3.0. Though, Ledger removed the ERC-20 tokens list from the embedded Ethereum app since version 1.2.6, leaving it to the wallet app to manage the tokens list. This release now incorporates that list in the RED Wallet binary directly, resulting in a significantly bigger binary (about 100 KB bigger than 0.3.0). The Nano keys will still check the validity of the tokens addresses internally for extra safety. Another consequence of Ledger's recent firmware updates is noticeably slower addresses retrieval when plugging the key. That's an internal change in the Ledger key, so we cannot do anything to bring back the fast speed we could achieve with older firmware.<br />
<br />
As a reminder, BIP44 address derivation support is present in the wallet since 0.3.0. If you are using a key initialized in an older Ledger Live version, the derivation path would be different and in order to make the wallet recognize your key, you need to click on the "(Legacy)" label (we will improve that UI in further versions).<br />
<br />
Batch transactions were introduced in 0.2.0, they now work for any ERC-20 tokens in addition to ETH. They can be accessed from a contextual menu using a right click on an ETH account.<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="/images/blog/wallet040-3.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="763" data-original-width="1238" height="246" src="/images/blog/wallet040-3.png" width="400" /></a></div>
<br />
<br />
<span style="font-size: large;">TREZOR Key</span><br />
<br />
The RED Wallet has updated the firmware support:<br />
<br />
<ul>
<li>Wallet v0.3.0: Compatibility with firmware 1.7.1+</li>
<li>Wallet v0.4.0: Support for the latest firmware of the Trezor key. 1.8</li>
</ul>
<br />
TREZOR model T is fully supported on macOS. On Windows 7, if the key is not recognized, you need to install the <a href="https://wallet.trezor.io/#/" target="_blank">TREZOR bridge</a> first.<br />
<br />
<div class="separator" style="clear: both; text-align: center;">
<a href="/images/blog/wallet040-5.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img border="0" data-original-height="551" data-original-width="968" height="227" src="/images/blog/wallet040-5.png" width="400" /></a></div>
<br />
<span style="font-size: large;">Bug fixes</span><br />
<br />
<ul>
<li>FIX: Ledger key does not work on Windows in some cases.</li>
<li>FIX: crashes in some cases when using Ledger key on Windows.</li>
<li>FIX: only ledger key is usable when plugging both ledger key and trezor key.</li>
<li>FIX: trezor-driver context name is wrong.</li>
</ul>
<br />
<br />
<span style="font-size: large;">Download the RED Wallet 0.4.0</span><br />
<span style="font-size: large;"><br /></span>
<br />
<div style="text-align: center;">
<a class="dl-button" href="https://static.red-lang.org/wallet/dl/win/RED-Wallet.exe" style="color: dark red;">Windows 7/8/10 <el style="color: black;"> [494 KB]</el></a>
 <a class="dl-button" href="https://static.red-lang.org/wallet/dl/mac/RED-Wallet.zip" style="color: dark red;">macOS 10.1x <el style="color: black;"> [491 KB]</el></a>
</div>
<br />
<br />
Just click on the executable to run it (extract the .app file first on macOS), no installation or setup process required. Plug in your Ledger or TREZOR key and enjoy a smooth and simple experience!<br />
<br />
If you want to check if your RED Wallet binary has been tampered with in any way, you can simply drag'n drop the wallet executable on our <a href="https://red.github.io/bincheck/" target="_blank">binary checking service</a>. If it's legit, the screen will turn green. If it turns red with a warning message, please notify us on <a href="https://gitter.im/red/blockchain" target="_blank">Gitter</a> or <a href="https://twitter.com/red_lang" target="_blank">Twitter</a> at once.<br />
<br />
<u>Only download the RED Wallet app from this page, do not trust any other website for that</u>.<br />
<br />
Enjoy!<br />
<br />
{{< /rawhtml >}}