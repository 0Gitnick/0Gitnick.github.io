---
title: "Site Update 002"
date: 2020-11-13T04:59:22Z
tags: ["info"]
summary: "Find out what's new on my blog."
draft: false
---
The RSS feed on my site works again. I'm not sure how long it was broken. I generate this site using relative URLs in order to accomodate I2P, Tor and Zeronet users. That inadvertantly caused the XML for RSS to also use relative links. RSS doesn't support relative links because it has no way of knowing the URL from only the XML data. I patched it so the XML now uses absolute links.    

Sorry to anybody using RSS! ¯\\_(ツ)_/¯
