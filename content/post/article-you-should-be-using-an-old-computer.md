---
title: "[Article] You Should Be Using an Old Computer"
date: 2021-01-22
tags: ["articles", "computing", "free software", "society"]
summary: "There is a war being waged on general-purpose computing. Every year manufacturers come up with new ways to make your computer harder to repair thereby increasing e-waste. Every year software companies make their ecosystems more locked down giving you less and less control over your own devices. To _not_ use an old Thinkpad is to be on the wrong side of this war."
draft: false
---
I was going to write my own post about this subject until I discovered Luke Smith, a GNU/Linux technology Youtuber, already wrote an article about it.

\[Link Below\]  
[https://lukesmith.xyz/articles/oldcomputer](https://lukesmith.xyz/articles/oldcomputer)

His reasons for recommending an old computer (specifically Thinkpads) are:

* New computers are unnecessary for most people
* New computers are expensive
* New computers are slim and break easier
* New computers are impractical to repair yourself
* New computers contain a potential backdoor

You can read his article for more details on each point. I have a few comments to make. Smith cites processor-intensive video rendering as a reason you might need a newer computer. There's also training/running neural networks, mining digital currency and some exhaustive search algorithms. But again the average person won't be doing those things.

## Intel Management Engine
Smith also claims the Intel Management Engine (Intel ME), the hidden processor in every modern Intel chip, is a government backdoor. This isn't yet proven but the code in Intel ME is proprietary and secret, so it should be treated as a _potential_ intentional backdoor. _At minimum_ it's a [security hazard](https://www.eff.org/deeplinks/2017/05/intels-management-engine-security-hazard-and-users-need-way-disable-it). Smith notes that AMD processors have basically the same problem.

The potential backdoor is really the crux of the ethical problem. Even if you don't care about the price and you never drop your computer and you never replace any parts there's still the potential backdoor. __Intel ME is always on even when your computer is turned off. It can't be removed. No one knows what it actually does and Intel won't tell us. We know it has full control over system memory and it can connect to the internet.__ If you're at all tempted to use the [nothing to hide argument](https://rationalwiki.org/wiki/Nothing_to_hide) I only ask that you apply that same logic to Intel. If Intel has nothing to hide, why can't they show us the source code for the ME? Why keep it secret? Why not allay all fears of a backdoor once and for all by releasing the source code? Unless of course it is in fact a backdoor.

Maybe you're above nothing to hide though. You understand privacy is a human right. But, you reason, the Intel ME isn't a big deal because an interested government could find out what they wanted to know some other way. Besides even without ME there's other embedded software that, however unlikely it is, could possibly also have backdoors. All that's beyond your "threat model" anyway. This goes back to a previous post I made. By using the _least_ potentially backdoored computer possible, you [raise the bar on privacy](/raising-the-bar-on-privacy) (and freedom!). That's a cause we _all_ need to be fighting for irrespective of threat models.

## RetroFreedom
The next most obvious question is "Where do I buy a computer without a backdoor?". I recommend [RetroFreedom](https://retrofreedom.com/) (formerly Minifree). [Leah Rowe](https://vimuser.org/) operates the site. She maintains the [Libreboot](https://libreboot.org/) project, a free as in freedom alternative BIOS that ships with the old Thinkpads she sells. You can purchase products with cryptocurrency and several addons and upgrades are offered. I don't mind the markup in price since I know it goes toward an important free software project. I can personally attest to the quality of the laptops from RetroFreedom. I've bought several laptops from there running exclusively free software and I'm very satisfied.

## Free Software
I would never again use a nonfree laptop to do my everyday personal computing. I've given up videogames since all the popular titles are nonfree requiring me to run the Winblows operating system. [I quit my job](/why-i-left-its) to avoid promoting proprietary software. [I dropped out of college](/the-tipping-point-rejecting-windows-zoom-lockdown-browser-and-the-lockdown-monitor) so I didn't have to use invasive proprietary malware. Too many people have told me I'm too extreme. I care too much about free software. Life is just too short to be so picky. But to them I would say this:

What does it say about society that the only way to get a non-backdoored laptop is to buy from a specific set of computers that are around 13 years old, replace the WiFi card, use special equipment to flash the BIOS with Libreboot/Coreboot and replace the operating system with GNU/Linux? Or pay someone else to do the procedure.

Further, what you have to realize is there is a war being waged on general-purpose computing. Every year manufacturers come up with new ways to make your computer harder to repair thereby increasing e-waste. Every year software companies make their ecosystems more locked down giving you less and less control over your own devices. To _not_ use an old Thinkpad is to be on the wrong side of this war. __I do not want to live in a world where I don't have control over what I buy and cannot repair it__.

__Most people living in 1st world countries today are far too complacent__. I can't emphasize this enough. So when people ask me why I care so much, why I've given up _so_ much, I look at them in bewilderment. Why _don't_ they? If people like them don't start caring soon we're going to live in a dark world where computer users are totally subjugated. The 13 year old Thinkpads suffice for 95% of use cases for now but that won't always be true. Proprietary threats are looming. Change needs to happen now, not 10 years from now. So use a free laptop even if it's inconvenient because it's not getting any easier.

## Privacy
There's also the whole privacy issue of having a potentially backdoored laptop. A college professor once told me privacy is dead. As if it were just a fact of the modern era and I hadn't realized it yet. As long as there are people like me are around privacy is _not_ dead. I will _never_ accept a world without privacy. I will resist backdoors into my computer. I'll tell you another thing. It wasn't all the free software people that inspired this in me. It was the haters. Those who said it didn't matter, privacy is dead, it's unwinnable, I should just give up so my life is easier, etc. So please tell me any of those things. The naysayers keep me motivated. I don't waste my time wondering whether free software is a fight we can win. It's a fight we _must_ win. As long as there's _any_ chance of winning, and even if it _seems like_ there's not, we _must_ try.

You don't need to quit your job and drop out to create change. All you have to do is create a rift. Get people to take notice. Force them to act by being unmoving in your commitment to free software. You won't be popular. And you'll be told you're wrong _a lot_. You might even start to doubt yourself. But let others say whatever they want and stay strong anyway. You have an advantage they don't: the knowledge that you're doing the right thing. You do have power. Those in power would like you to think that you don't, but you do. Wield it wisely.
