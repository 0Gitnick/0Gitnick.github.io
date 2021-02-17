---
title: "Site Update 003"
date: 2020-12-09
tags: ["info"]
summary: "Find out what's new on my blog."
draft: false
---
## What's New
I removed the bootstrap JS that wasn't really doing anything. The site should load faster and use less data now. I created a new tag called "info" for all site updates. The about page has been compacted so it's cleaner and easier to read and not so long-winded. I also updated my PGP key to use Curve25519 instead of RSA. [PGP is awful](https://secushare.org/PGP). I still use it for email only because it's better than nothing.

This site allows you to get filtered RSS feeds for just the content you're interested in. For example, if you only want to read about privacy, then you can use [https://0gitnick.xyz/tags/privacy/index.xml](https://0gitnick.xyz/tags/privacy/index.xml) for a privacy feed or [https://0gitnick.xyz/tags/privacy/index.html](https://0gitnick.xyz/tags/privacy/index.html) for webpages. The category-centered feeds were broken with the same issue the aggregate site feed had last time with the relative URLs. They're fixed now.

The biggest change I made is reorganizing the [tags](/tags). I renamed some tags and added new ones. The reason I did that is I have in mind the readers who just want a particular type of content and the tags were disorganized before. If I'm not sure if a post should be assigned a certain tag, I err on the side of too many tags since not tagging it could mean some readers will miss a relevant post. It's better for readers to see a post they don't care about now and then and just delete it rather than miss posts entirely because I was too strict with tagging.
