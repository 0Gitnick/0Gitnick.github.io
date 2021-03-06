---
title: "Back Up Your Data"
date: 2020-07-26
tags: ["computing", "free software", "society"]
summary: "This post is a public service announcement about backups inspired by the post I lost. I've had my own backups for over 5 years, and never have I lost any data from those backups. The following advice is meant for individuals, not a corporate or business setting."
draft: false
---
## Losing My Data
My motivation for writing this post is I accidentally deleted another unpublished post I put a lot of effort into. It probably had 6+ hours of work invested in it at least. And now, it's gone forever. Perhaps it's best put into the 5 stages of grief. At first, I denied it. I was sure I had it copied to my clipboard, saved in my text editor cache or history, but it wasn't. After that, I got angry that I could have accidentally deleted something I put so much work into. How could I make such a dumb mistake? I skipped bargaining. I was sad about it for a while. Then I reached acceptance, and decided to write this post instead.    

This post is a public service announcement about backups inspired by the one that got lost. I've had my own backups for over 5 years, and never have I lost any data from those backups. So I have a little bit of experience making backups. The following advice is meant for individuals, not a corporate or business setting.

## Why to Backup?
Backups are important because hard drives fail and get corrupted, phones break and get lost, and physical media degrade. Backups can help protect your important data.

## What to Backup?
How do you know which data should go into your backups? Here are two quick rules of thumb:

1. You would want the data back if you lost it or it corrupted (_it's worth something to you_)
2. Using a backup would take less time than recreating the data yourself (_it's worth the trouble to back up_)

I'll use this blog as an example. It uses the Hugo software to generate the site pages. I can [install Hugo](https://gohugo.io/getting-started/installing/) on any platform with a few simple commands. The cost of retrieving Hugo is _very_ low. If I lost it, I could recreate it by just reinstalling. I would get the latest version and it would work on whatever platform I happen to be using. If I made a standard backup, I would be stuck with the same version and the way it is packaged may not work across platforms. So, making a backup of Hugo would break rule #2 because it would take _more time_ to recover it from a backup than just reinstalling it.    

I could almost say the same about the template I'm using. Except I've made modifications to it to not include Goo-lag analytics and other things. I have it backed up because __#1__ I would need it back if I lost it and __#2__ making those modifications again would take longer than just restoring the template from a backup. The same goes for my site content. Rewriting it all would be a huge effort. As I write more posts, the effort only increases. So, obviously, I back up my site content because it satisfies rules #1 and #2.    

For most people, data that satisfies both of these rules are going to be old home videos, vacation pictures, resumés, portfolios, financial records, contact lists and password manager files. Those are generally data that are valuable and either can't be recreated or would be cumbersome to recreate.

## When to Backup?
If you don't already have a backup, create one right now. Don't wait. Your data could become corrupted at any time. If you don't have copies of it elsewhere, then you're just waiting for the inevitable to happen. Your digital media (hard drive, flash drive, SD card, CD/DVD) will eventually fail and you will lose your important data.    

Once you have your data backed up for the first time, you will need to create a backup schedule. A backup schedule is how often you want to back up your data. It can be weekly, monthly, yearly, etc. It doesn't have to be at regular intervals, but that's good practice. This decision should be based on how frequently you acquire important data and how important the new data is. If you record your daughter or son's first steps on video, you will want to back that up the same day or week probably. If you don't acquire important data often, you may want a yearly backup schedule.    

In my case, I have a blog. So far, I have averaged 2-3 posts per month. I put a lot of thought into my posts. Since losing just 1 post motivated me to write all of this, I don't want to even think about losing 2-3 posts at once. Therefore I should, at minimum, perform monthly backups so that I never lose more than 2-3 posts. Redundant copies of my posts are stored on web servers and Zeronet, but those are only posts that I have deemed worthy to publish. The ones I haven't published don't have redundant copies, so I should still perform monthly backups. That's an example of how to think about a backup schedule. It will be different for everyone since everyone has different backup needs.

## Where to Backup?
Where you back up your data is crucial. This gets into what is widely known as the 3-2-1 rule of data backups. You need 3 copies of your data, 2 types of storage media, and 1 offsite copy. You __must__ have an offsite copy in case of a disaster. If a fire breaks out in your home and you're gone, it will destroy your computer _and_ your external drive. So it's no good to only have data stored locally. Yes, you need local copies, but you must have a remote copy as well.    

Also, having 2 copies of your data on the same media does not count as 2 copies. It counts as 1 copy. One computer science student I talked to in the past did not understand that __[RAID](https://en.wikipedia.org/wiki/RAID) is not a backup__. One power spike and all your drives in your RAID system can fail simultaneously. It could get stolen. Do you trust yourself to never delete anything important by accident? You need _physically_ separate media for backups, not just _logically_ separate. This reduces the chance you will delete important data without catching the error first. Physically separate drives don't count if they are connected to the same system. For example, it doesn't matter if you have copies of your data on multiple cloud instances if those instances are through the same cloud provider. What if that cloud provider gets compromised and you lose both backups? So, use separate systems as well as separate drives.    

And finally, you need at least one air-gapped backup. If all your accounts and machines get compromised, you need a way to recover your data. Without that, your data could be stolen and held for ransom. To avoid this scenario, set up an offline backup in a different city, state, or country. The farther, the better. Your offline backup will probably be local since you can't access it remotely. Having a remote offline backup is inconvenient because it will be hard to maintain a frequent backup schedule. You could keep your offline backup as a micro SD card stashed between your phone and its case, or in your purse so it's always with you. This way, your offline backup, local backup, and remote backup are in 3 physically separate locations.

## Who to Backup?
It's important to know who is in control of the computer your backup is sitting on. If you use a cloud service provider to back up your data remotely, there are significant caveats. The caveats apply any time you are using hardware that is not under your control.    

For one, you have to trust the cloud service's security practices. If they get compromised, your data will be at risk. Are you willing to accept that risk? What if their database gets compromised? To eliminate this risk, you should __always__ encrypt your data before uploading it. I'll get to this topic in the next section.    

Another risk is that the data is modified either intentionally or by error. Encrypting the data will not prevent it from being modified maliciously. For that, you need authenticated encryption. Also, you may be limited on monthly bandwidth or file storage capacity. If you store a lot of data, that could quickly become expensive.    

Using a cloud service provider, you can only access your data at their leasure. Hopefully their system has good uptime. This usually isn't a big problem. But they will also have full control over how you access your data. They might only allow you to access it over a web portal. You'll want to make sure they run a service you can access using only free software such as [Nextcloud](https://nextcloud.com/) or [Etesync](https://www.etesync.com/). Preferably, they give you many ways to access it so you aren't locked in to a particular client program.

## How to Backup?
Now that I've covered the 5 W's (why, what, when, where, who), I'll cover the most important aspect of backups: How to do them. There is an endless list of software that can help with backups. One good rule is you should _always_ use [free software](https://www.fsf.org/about/what-is-free-software) for your backups. _Never_ use [proprietary software](https://www.gnu.org/proprietary/) for any part of the backup process. There's no reason for it and it will compromise your backup security.

#### Offsite Backup
The first part of the backup process is to decide which data you want to store. Then, you should decide how you want to handle the remote backup. If you use a VPS, you control _how_ you access your data, but all other caveats still apply. On a VPS, you can host your own service for the remote backup. As I said, there are a thousand ways to do this depending on your needs. If you like to keep it barebones, you can run a simple ssh server. If you are hosting a backup for more than just yourself, you may want to use an actual backup platform such as Nextcloud. There are several OS's that are built for the express purpose of backups from [FreeNAS](https://www.freenas.org/) to [OpenMediaVault](https://www.openmediavault.org/). It doesn't really matter which you choose as long as it's meets your needs and runs free software.

#### Encryption
Once you have your offsite service set up, it's time to perform the backup. The first thing you'll want to do before anything else is __encrypt your data__. For most people, you'll want to use [Veracrypt](https://www.veracrypt.fr). It's user friendly and cross-platform. For a guide on how to use Veracrypt, follow the [beginner's tutorial](https://www.veracrypt.fr/en/Beginner%27s%20Tutorial.html). Other encryption programs require using the command-line, decrypting the data to disk before reading it, or only work on GNU/Linux. For those reasons I won't use them in this tutorial. However, if you feel comfortable using LUKS or GPG, go ahead. Just know the trade-offs.    

This next step is optional, but I recommend it. Veracrypt does not perform authenticated encryption. Your data is still encrypted, but it could be maliciously changed by an attacker and Veracrypt won't know about it. The best way to prevent this is with an HMAC. On GNU/Linux, you can do this with a single command as long as you have openssl installed. It doesn't seem as easy to perform on other platforms. For your HMAC password, you can reuse your Veracrypt volume password. Copy the resulting HMAC value, then save it to a text file next to your Veracrypt container file. It should also go into your backups. When you retrieve your backups later, you can perform the HMAC operation on the downloaded container file checking that the result matches the value you saved before. This provides you file integrity. At this point, I recommend deleting unencrypted copies of your data on disk since there's no good reason to have them around.    

#### Finishing Up
Now your data is finally ready to go into storage. Upload the Veracrypt container file along with the HMAC text file to your remote backup system. Then copy your data onto external media such as a USB flash drive, external hard drive, or SD card. This will serve as your offline backup. You can store your third backup on the same computer you use to access and modify the data, or you can choose a different one so it's not taking up space. That's up to you. Just be sure to have at least 3 copies of your data, one of them at a remote location and one of them air-gapped. You could write a script to do the backups and check the HMAC for you.    

Finally, you'll want to decide on your backup schedule. To add to your backup, you can simply mount your Veracrypt container and add more files. If you ever run out of space, you can always create a larger container and transfer all your data there. I hope you found this guide useful. I didn't go into as much detail as I could have about remote backup solutions, but I think I covered what needed to be covered.    

If you've made it this far, thank you for reading. If you find my ideas valuable, then please consider making a donation. Details are on my [about page](/about#donate).
