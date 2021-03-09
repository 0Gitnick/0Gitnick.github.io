---
title: "[Video] Is Your Keyboard Spying on You?"
date: 2021-03-09
tags: ["videos", "computing", "free software", "privacy"]
summary: "Your keyboard is one of the most important things to secure in desktop _and_ mobile environments, yet it is often overlooked. TheHatedOne has some suggestions on which keyboards are safe to use."
draft: false
---
Your keyboard is one of the most important things to secure in desktop _and_ mobile environments, yet it is often overlooked.

## Mobile
If you're on a mobile device, chances are you're using a "virtual" keyboard. A virtual keyboard is just an on-screen keyboard instead of a physical one. The problem is many available keyboards send your keystrokes to a remote server by default. Even the stock keyboard may do this. Even if you're using the secure messaging app Signal, some big company could still be collecting everything you type through your keyboard app. Watch TheHatedOne's video to find out how to secure your Android keyboard.

[[Video Link]](https://redirect.invidious.io/watch?v=vCRX0MZm2KI)

The same advice goes for custom keyboards on iOS: If you're using a custom keyboard, __use free software!__

## Desktop
TheHatedOne does not mention _physical_ keyboards. I have two pieces of advice for those:

1. Do not use a wireless keyboard (or mouse).
2. Do not use a programmable keyboard.

#### Wireless Keyboards
The problem with _wireless_ keyboards is in the name; they send keystrokes wirelessly to the USB receiver. It's often impossible to _verify_ that wireless keyboards securely encrypt traffic. Even the keyboards with strong encryption are vulnerable to replay attacks which could be used to exploit the target machine. Even if a strong encrypted wireless keyboard is immune to replay attacks, it could be vulnerable to spoofing. Even with strong encryption, replay immunity and spoofing immunity, it's _still_ possible to log the _frequency_ and _timing_ of keystrokes using statistical analysis to determine which keys are being pressed at which times. As a final very _minor_ issue, if AES is ever broken you'll need a new keyboard.

This isn't conjecture. Replay attacks and keystroke logging have already been demonstrated. It's best just to have a wired physical keyboard (and mouse) to avoid all these problems.

#### Programmable Keyboards
The second concern is _programmable_ keyboards. The problem with them is also in the name; they are programmable. If your computer can upgrade your keyboard firmware, then an attacker could embed viruses in your keyboard if your operating system is ever compromised. Then every time you reinstall your OS the virus could be reinstalled via your keyboard. If you have a fancy RGB keyboard controlled by drivers on your machine _or_ you have G-series keyboard macros (G1, G2, G3, etc.) you might consider using a different keyboard that _isn't_ programmable. You don't want a keylogger embedded into your keyboard itself. So just use a non-programmable keyboard and program macros inside the actual program where you want to use them. There's no reason I can think of that a keyboard would need to have embedded macros anyway. Just embed your macros in the program or OS configuration itself.

## Conclusion
For the vast majority of computer users, these measures should be enough to secure your keyboard. 
