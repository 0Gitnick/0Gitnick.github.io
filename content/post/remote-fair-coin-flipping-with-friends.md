---
title: "Remote Fair Coin Flipping with Friends"
date: 2020-11-19T06:02:07Z
tags: ["computing"]
summary: "This post is mostly just for amusement. It's my half-hearted attempt at designing a cryptosystem."
draft: false
---
Suppose you and some friends want to flip a coin without meeting up. It has to be done over an [authenticated communication channel](https://en.wikipedia.org/wiki/Secure_channel) such as a secure messaging app. How can you do it such that nobody can predict the final result? I'll explain how to do it fairly. I'm well aware of common coin algorithms. This post is mostly just for amusement. It's my half-hearted attempt at designing a cryptosystem. More on that later.

## Coin Flipping
#### Flipping a Coin with a Friend
These are the steps for performing a single coin flip:

1. Flip a physical coin. Heads represents 0. Tails represents 1.
2. Append to the result of step 1 a space followed by a [nonce](https://en.wikipedia.org/wiki/Cryptographic_nonce) that your friend cannot easily guess. Never reuse the nonce. For tails, it will look like this:  
`1 munxpawrqoivzhujfxbxwcang`
3. Calculate the SHA-256 hash of the string in step 2 (in [Bash](https://www.gnu.org/software/bash/)):  
`echo -n "1 munxpawrqoivzhujfxbxwcang" | sha256sum`
4. Publish the hash from step 3 onto the authenticated communication channel.
5. Pause until your friend completes step 4.
6. Publish the result from step 2 onto the authenticated communication channel.
7. Pause until your friend completes step 6.
8. Calculate the hash of your friend's step 2 result comparing it to their step 3 result. If it doesn't match, then one of you has incorrectly computed the hash.
9. If the hashes match, remove the space and nonce from both you and your friend's step 2 results. Then [XOR](https://en.wikipedia.org/wiki/Exclusive_or) both results.
10. Convert the value from step 9 back to heads or tails as defined in step 1.

#### Flipping Multiple Coins with a Friend
If you want to flip multiple coins, you _can_ repeat steps 1-10 of the single coin flip, but that's very cumbersome. There's an easier solution. Suppose you and your friend want to flip N coins:

1. Flip N physical coins. Heads represents 0. Tails represents 1. Concatenate the coin flip results.
2. Append to the result of step 1 a space followed by a [nonce](https://en.wikipedia.org/wiki/Cryptographic_nonce) that your friend cannot easily guess. Never reuse the nonce. For the sequence heads tails heads tails heads, it will look like this:  
`01010 yabynkgpbfnagntyzvgvgmwaa`
3. Calculate the SHA-256 hash of the string in step 2 (in [Bash](https://www.gnu.org/software/bash/)):  
`echo -n "01010 yabynkgpbfnagntyzvgvgmwaa" | sha256sum`
4. Publish the hash from step 3 onto the authenticated communication channel.
5. Pause until your friend completes step 4.
6. Publish the result from step 2 onto the authenticated communication channel.
7. Pause until your friend completes step 6.
8. Calculate the hash of your friend's step 2 result comparing it to their step 3 result. If it doesn't match, then one of you has incorrectly computed the hash.
9. If the hashes match, remove the space and nonce from both you and your friend's step 2 results. Then [XOR](https://en.wikipedia.org/wiki/Exclusive_or) both results.
10. Convert the values from step 9 back to heads or tails as defined in step 1.

#### Flipping a Coin with 3+ Friends
It _is_ possible to perform a remote fair coin flip with 3 or more participants, but there are 3 caveats. One caveat is depending on how many participants you have, it could take quite a bit longer than the previous cases where you only have 1 other person. This is because everyone has to participate in the coin flip if everyone wants to ensure fairness. Otherwise the other participants can collude to manipulate the coin flip. The second caveat is you need to have a __robust__ authenticated group communication channel resistant to [replay attacks](https://en.wikipedia.org/wiki/Replay_attack) and other funny business such as messages being edited/deleted without indication and out of order message receipt. But maybe that's taking my cryptosystem too seriously. The third caveat is increased complexity. All participants will need to know how to perform all the steps and there's a greater chance someone doesn't do step 3 right. Regardless, here's how you flip a coin with 3+ friends:

1. Flip a physical coin. Heads represents 0. Tails represents 1.
2. Append to the result of step 1 a space followed by a [nonce](https://en.wikipedia.org/wiki/Cryptographic_nonce) that your friends cannot easily guess. Never reuse the nonce. For tails, it will look like this:  
`1 munxpawrqoivzhujfxbxwcang`
3. Calculate the SHA-256 hash of the string in step 2 (in [Bash](https://www.gnu.org/software/bash/)):  
`echo -n "1 munxpawrqoivzhujfxbxwcang" | sha256sum`
4. Publish the hash from step 3 onto the authenticated communication channel.
5. Pause until all your friends complete step 4.
6. Publish the result from step 2 onto the authenticated communication channel.
7. Pause until all your friends complete step 6.
8. Calculate the hashes of your friends' step 2 results comparing it to their step 3 results. If they don't match, then one of you has incorrectly computed the hash.
9. If the hashes match, remove the space and nonce from both you and your friends' step 2 results. Then [XOR](https://en.wikipedia.org/wiki/Exclusive_or) all results.
10. Convert the value from step 9 back to heads or tails as defined in step 1.

#### Flipping Multiple Coins with 3+ Friends
This is the most difficult coin flip: multiple coins with more than 2 participants. I think you get the gist of it by now and I don't really need to type all this out, but I will for completeness sake. Not much will be changed from the above steps though.

1. Flip N physical coins. Heads represents 0. Tails represents 1. Concatenate the coin flip results.
2. Append to the result of step 1 a space followed by a [nonce](https://en.wikipedia.org/wiki/Cryptographic_nonce) that your friends cannot easily guess. Never reuse the nonce. For the sequence heads tails heads tails heads, it will look like this:  
`01010 yabynkgpbfnagntyzvgvgmwaa`
3. Calculate the SHA-256 hash of the string in step 2 (in [Bash](https://www.gnu.org/software/bash/)):  
`echo -n "01010 yabynkgpbfnagntyzvgvgmwaa" | sha256sum`
4. Publish the hash from step 3 onto the authenticated communication channel.
5. Pause until all your friends complete step 4.
6. Publish the result from step 2 onto the authenticated communication channel.
7. Pause until all your friends complete step 6.
8. Calculate the hashes of your friends' step 2 results comparing it to their step 3 results. If they don't match, then one of you has incorrectly computed the hash.
9. If the hashes match, remove the space and nonce from both you and your friends' step 2 results. Then [XOR](https://en.wikipedia.org/wiki/Exclusive_or) all results.
10. Convert the values from step 9 back to heads or tails as defined in step 1.

## Rationale
10 steps just to flip coins seems like a lot. So why all the steps?    

Publishing the cryptographic hashes _before_ the plaintext ensures that so long as there's at least 1 honest participant, the final results can't be tampered with. An honest participant is defined as a participant that faithfully completes all the steps.    

The reason for the nonce is the following: It would be trivial to convert the cryptographic hash of just `0` or just `1` back into its plaintext value. That's why you need to append a random value at the end. The reason the random value must be a nonce is the same reason you can't just hash a `0` or a `1`. If you reuse the random value, then the other participant(s) could catch on that you use the same value every time and collude to manipulate the final result. The space just delimits the coin flip(s) from the nonce.    

XOR was chosen as opposed to AND because AND would obviously bias the result toward tails.

## Attack Vectors
#### Publishing Invalid Data
One attack vector against my toy cryptosystem is just using nonsense as the plaintext. This will fail because it can just be discarded by all other participants. If the plaintext is valid but doesn't match the hash, then the plaintext can again be discarded. This type of attacker won't be able to verify the coin flip as unpredictable, but that's their punishment for not following the rules.

#### Synchronicity Attack
A more devastating attack with no clear solution is when an attacker doesn't publish anything, stalling the coin flip indefinitely. The first intuition for solving this is to start a timer as soon as the first hash is published and after the agreed upon time has passed, the attacker is simply excluded from participating. But this won't work because the attacker can just publish _near_ the agreed upon time limit. Due to latency and asynchronicity of messages, if successful, some participants will count the attacker's contribution to the coin flip while others will not. Honest participants won't be able to agree on the final results. Therefore the integrity of the results will be compromised. Worse yet, it won't be possible for the participants to even detect this unless they all publish their final results and cross-compare everything. Even then, an attacker can just lie about their results confusing everybody.    

Another idea at resolving the integrity issue would be to designate a leader to declare which participants' contributions count. Therefore the leader would have to be trusted not to manipulate the results. But the whole point of the coin flip is you shouldn't have to trust the other participants, so a leader defeats the purpose of the cryptosystem.    

You might be thinking more democratically though. Instead of having a single leader who acts like a dictator of the coin flip, you have a democracy. Once some majority of the participants has contributed to the coin flip, simply compute the result then. Trusting the majority is better than trusting a single participant. But this also fails because it could just happen by coincidence that two contributions happen at the same time, or an attacker collides them on purpose. In that case some participants will count the attacker's contribution to the coin flip while others will count some other contribution. Honest participants won't be able to agree on the final results. The integrity of the results will be compromised yet again.    

## Why You Don't Roll Your Own Crypto
By now you should have begun to see why a more advanced "common coin" algorithm is needed. This is a cryptosystem that doesn't have a good way to prevent an attacker from compromising the integrity of the coin flip, or forever stalling it. Any attempt to solve this problem just ends up pushing it back a step. In other words, this cryptosystem I've created is hopelessly broken and the only way to fix it is a completely different algorithm. But I can get away with it because I can say it's just a toy cryptosystem for fun. It should never be used for any real-world application. Use a common coin instead. And it's also an example of why you should never roll your own crypto. Even when it seems foolproof, there's always weird edge cases that ruin everything. This post shows a neat thing you can do with friends and also demonstrates why you should always use established cryptosystems rather than inventing your own. I hope you enjoyed it.
