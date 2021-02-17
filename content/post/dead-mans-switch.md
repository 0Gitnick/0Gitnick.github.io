---
title: "Dead Man's Switch"
date: 2021-01-27
tags: ["computing"]
summary: "The dead man's switch is a powerful self-defense tool that is automatically triggered when the human operator dies. It is your insurance policy that contains digital dirt on your aggressor."
draft: false
---
## Definition
There are _many_ kinds of dead man's switches (abbreviated here as DMS). The DMS's this post is concerned with are [software-based](https://en.wikipedia.org/wiki/Dead_man's_switch#Software). More specifically this post is concerned with what I will call Wikileaks/Mr. Robot style DMS's.

[Wikileaks](https://wikileaks.org/) is a non-profit that has a history of publishing highly classified news leaks obtained through anonymous sources. In order to protect the leaks, some are prereleased in encrypted form with the decryption key rigged to self-publish in case the operations of Wikileaks are obstructed in the meantime.

DMS's are also used 3 times in the TV series [Mr. Robot](https://mrrobot.fandom.com). One is first used by [Elliot Alderson](https://mrrobot.fandom.com/wiki/Elliot_Alderson) threatening to leak [Fernando Vera](https://mrrobot.fandom.com/wiki/Fernando_Vera)'s drug supplying operation to protect his dealer sweetheart [Shayla](https://mrrobot.fandom.com/wiki/Shayla_Nico) ([S1E6](https://mrrobot.fandom.com/wiki/Eps1.6_v1ew-s0urce.flv)). The second is in the form of an email from [Trenton](https://mrrobot.fandom.com/wiki/Trenton) to Elliot hinting how to undo the 5/9 hack ([S3E8](https://mrrobot.fandom.com/wiki/Eps3.8_stage3.torrent)). The last comes again from Elliot threatening to leak information to hurt the antagonist [White Rose](https://mrrobot.fandom.com/wiki/Whiterose) ([S3E10](https://mrrobot.fandom.com/wiki/Shutdown_-r)).

There are 2 key elements common to the DMS's I've referenced so far:
1. A person or group that stands to lose something if private information is published.
2. An adversary that rigs private information to self-publish unless deactivated.

Now I'll consider the potential uses for such a device.

## Use Cases
#### Self-Defense
The first use case that comes to mind for a Wikileaks/Mr. Robot style DMS is _self-defense_. If you learn something others want to keep private, you could be in danger. You "know too much". From organized crime to classified government documents the most obvious way to deal with someone who knows too much is to have them killed, assuming you have let's say a _highly questionable_ moral compass. Dead men tell no tales.

A DMS is a way of turning the "knowing too much" problem on its head. It's especially useful for dissidents and independent journalists that regularly find themselves pitted against powerful multinational corporations, [the state](https://www.theguardian.com/us-news/2020/dec/07/florida-police-raid-data-scientist-coronavirus) and [large criminal enterprises](https://en.wikipedia.org/wiki/Jeffrey_Epstein). It can be used as a bargaining chip to protect yourself and those you care about. If anyone you care about is harmed the private information is assured to leak, so instead of "dead men tell no tales" it becomes "living men tell no tales".

__You should carefully consider before using one. They have the potential to be effective _only_ if used correctly__. You might ask __what is the value of the leak?__ The final time Elliot used one in Mr. Robot the threat of the leak wasn't devastating enough to protect him from White Rose. Elliot was only able to save himself by proving he had worth. It's also important to consider __how long will the leak hold value?__ After Vera's operation was over he stood to lose _nothing_ from Elliot's leak. Elliot was again saved only because of his value, not his DMS. The lesson there is to be thoughtful before using one.

#### Leak Defense
The next use case is to protect the leak itself. When the leak is obtained from an anonymous source it's disorganized and hard to read. So before Wikileaks publishes a leak they have to [curate](https://en.wikipedia.org/wiki/Data_curation) the content. But there's a danger that while they're doing that the leak could be seized or destroyed by an adversary. To mitigate that they can set up a DMS so the data will get published either way. Then the adversary no longer has any incentive to interfere with the data curation process.

#### Offense
As for _offense_, it doesn't make as much sense to use a DMS. Even though it _could_ be used illegally for blackmail or extortion it would only be _necessary_ if the offender was concerned about ending up in a situation where they can't leak the information. At that point they'd probably be more interested in self-defense than offense anyway. Unless there are circumstances I'm overlooking then Wikileaks/Mr. Robot style DMS's aren't very useful for offense.

For the rest of this post I'm going to focus only on the self-defense use case.

## Theory and Practice<a name="Theory_and_Practice"></a>
#### In Theory
In theory __the DMS represents a sequential, [noncooperative game](https://en.wikipedia.org/wiki/Non-cooperative_game) between 2 players__. Player 1 (the defender) chooses between leaking Player 2's secrets and doing nothing. Player 2 (the attacker) chooses between violence against Player 1 and doing nothing. Both players are assumed to be rational. Here are the payoffs for each strategy:

1. If Player 2 _commits violence_ then
    1. Player 1 loses 2 points (harm)
    2. Player 2 gains 1 point (retribution)
2. If Player 1 _leaks data_ then
    1. Player 2 loses 2 points (harm)
    2. Player 1 gains 1 point (retribution)

This point structure assumes both Players value retribution but not as much as avoiding harm. Both Players assume the other will adopt the strategy of maximizing their own points. Using the [Minimax](https://en.wikipedia.org/wiki/Minimax#Example_2) algorithm it can be determined that both Players will do nothing. Any other action would result in both players having less points. Points are represented for each Player in the format (P1,P2) in the decision tree below:

![decision_tree](/decision_tree.jpg)

#### In Practice
In practice there are a number of complicating factors. Player 2 may not know exactly what the leaks contain making it impossible to value the _cost_ of violence. Player 1 can create the _perception_ of cost but in reality not even set up the switch _or_ set one up incorrectly so it doesn't work _or_ simply forget to deactivate it thus triggering it. Player 2 may find a way to disarm it. To account for the real-world outcomes you would need a much larger decision tree. And even then what are the chances that both players act rationally? So don't think that a DMS is guaranteed to be effective.

## Setup
If you still want to configure a DMS the first thing to consider is how to format the data you wish to include.

#### Luks2
If you're gathering data to be included in the leak on an ongoing basis then you should probably use an encrypted disk image file. I recommend using [LUKS2](https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup) for the encrypted disk image. There are plenty of tutorials out there on how to use it so I won't be going over that in this post. To leak the data is easy. Just publish the encryption slot passphrase.

#### GnuPG2
If instead you already have all the data you're ever going to leak then you can just create a [Tar](https://en.wikipedia.org/wiki/Tar_%28computing%29) archive encrypted with [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard). [GnuPG is awful](https://secushare.org/PGP) so you might consider other file encryption methods as well. It doesn't matter that much so long as you use free software. 

#### Content Distribution
Once your encrypted archive is prepared you'll need to distribute it to others. Wikileaks "insurance" files were distributed through torrents. In Mr. Robot email was used. There's no standard for this. It's completely up to you how you do this part. The important part is anyone that would want a copy knows about the leak and can get a copy.

#### VPS Setup
Now comes the part of the setup where you need a server machine to actually trigger the DMS. __If you're using a DMS there's no reason not to make it as secure as possible__ because securing it from a state-level adversary is only a few steps extra versus securing it from a mobster. I won't cover how to secure your personal computer but if you're using a DMS you should at a minimum have [full-disk encryption](https://en.wikipedia.org/wiki/Full_disk_encryption) enabled with a strong password.

To get started use an anonymous VPS since you shouldn't have physical access to the server. If you have physical access an adversary could also gain physical access and permanently disarm the switch. So the first thing you need to do is acquire [Monero](https://www.monero.how/). Then use Tor Browser to [purchase a _foreign_ VPS](https://www.getmonero.org/community/merchants/#hosting) with the Monero, but don't give the VPS provider your true credentials. You can ssh into your VPS with the command `torify ssh <user>@<server>`. Then you should [harden your ssh configuration](https://stribika.github.io/2015/01/04/secure-secure-shell.html) and [put sshd behind a Tor v3 Hidden Service](https://medium.com/@NullByteWht/how-to-set-up-an-ssh-server-with-tor-to-hide-it-from-shodan-hackers-eda93927a742) so a [MITM](https://en.wikipedia.org/wiki/Man-in-the-middle) can't locate it. Once all that's done you're finally ready to set up the actual DMS.

#### Cron
There is free software that automatically configures a DMS, but it's equally as easy to set one up yourself. Simply write a script that checks for the existence of a file and schedule it to run at regular intervals using [Cron](https://en.wikipedia.org/wiki/Cron). If the file exists, delete it. If the file does not exist, your script should execute a separate script that publishes the passphrase or private key needed to decrypt the data. It's up to you _where_ you publish the decryption key. Just be sure to test it first with a _fake_ key.

Here's what such a script might look like:
```bash {linenos=table}
# File: /home/<user>/trigger.sh

FILE_DISARMED=/home/<user>/disarmed
LEAK_SCRIPT=/home/<user>/leak.sh

if test -f $FILE_DISARMED"; then
    rm $FILE_DISARMED
else
    ./LEAK_SCRIPT  # publishes private key etc.
fi
```

The script for disarming the switch might look like:
```bash {linenos=table}
# File: /usr/local/bin/disarm.sh

FILE_DISARMED=/home/<user>/disarmed
GREEN='\033[0;32m'
CYAN='\033[0;36m'
NC='\033[0m'

if test  -f $FILE_DISARMED; then
    printf "${CYAN}ALREADY DISARMED.${NC}\n"
else
    touch $FILE_DISARMED
    printf "${GREEN}SUCCESSFULLY DISARMED.${NC}\n"
fi
```

Those two scripts are the most important. Don't forget to set their permissions as executable. Next you need to decide how often you want the switch to be triggered. You can set it to be as frequent as you wish but remember if the switch isn't deactivated each time before trigger.sh runs it will publish the private key. The last thing you want is to accidentally trigger the switch. Phoenixnap.com has a great [knowledgebase article](https://phoenixnap.com/kb/set-up-cron-job-linux) on using Cron. Here's an example that triggers the switch monthly at 00:00 hrs:
```plaintext
@monthly /home/<user>/trigger.sh
```

And finally the client command to disarm the switch is:
```bash
torify ssh <user>@<address.onion> disarm.sh
```

#### Reminder
As an added bonus you could use Cron to schedule a script notifying you before the DMS is triggered. For instance if the DMS needs disarmed on a monthly basis you could write a script that emails you a week in advance a reminder to deactivate it. Again a DMS is _only_ effective if you _don't forget to disarm it_, so I wouldn't create a DMS without a notification script.

That's it. That's all you need to set up your own DMS. 

## Popularity
You don't hear about Wikileaks/Mr. Robot style DMS's being used very often. I assume that's because of 3 reasons:

1. They require knowledge of GNU/Linux, encryption tools and scripting
2. They require continuous maintenance
3. They don't occur to most people to use

In my view __DMS's are woefully underused and they should be more common especially with dissidents, protest organizers and investigative journalism organizations__. The fact that Jeffrey Epstein didn't have a DMS before he "[killed himself](https://en.wikipedia.org/wiki/Epstein_didn%27t_kill_himself)" is almost beyond believe. A man with his wealth and criminal connections should've had one. He could've privately paid someone to set it up _for_ him.

I think about how his situation might have turned out differently if he would've set up one. Assuming he didn't commit suicide it could have protected him long enough to call out other rich and powerful people involved in sex trafficking. But it goes farther than Epstein. There are lots of situations where wealthy individuals and those with computer skills could have set up a DMS to protect themselves but apparently didn't think to do so.

As I said before [one should be careful before using a DMS](#Theory_and_Practice). Using one is tricky in practice but it still seems like they could get far more use than they tend to. I'm generally in favor of them since they seem to be primarily used for preventing violence and protecting socially important leaks. Like any tool they can be misused for nefarious purposes. Based on present usage though, if they were used _more often_ in the future, I estimate that, on balance, they would be ethically and socially beneficial.
