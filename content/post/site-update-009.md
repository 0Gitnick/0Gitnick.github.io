---
title: "Site Update 009"
date: 2021-02-21
tags: ["info"]
summary: "Find out what's new on my blog."
draft: false
---
## What's New
I haven't posted anything for a while and I've been working behind the scenes to make improvements. Here they are:

* Output RSS content as _full_ post content rather than mere content summaries for better accessibility to RSS users.
* Move the custom inline CSS to the external stylesheet.
* The site's [Github](https://github.com/0gitnick/0gitnick.github.io) and [Gitlab](https://gitlab.com/0gitnick/0gitnick.gitlab.io) CI workflows that host the [site mirrors](/about#Site_Mirrors) have been fixed. Before, I was locally generating files and uploading them as a single commit. Now, I upload the source files and let the remote servers do the work.
* Launch Gitea server on new subdomain https://git.0gitnick.xyz to host site content and theme for better organization and transparency in generating the site. The reason I did not go with Savannah as I planned in my last site update is because Savannah has _very_ strict licensing requirements. Since my site is forked _and_ I might fork more projects in the future, I'd rather not spend hours fixing license text before I can even upload the project. I have no problem with meticulously licensing my own work. It would just be too demotivating to do that for someone else's work.
* Write content summaries for every post. This was very tedious but worth it. It makes the site more aesthetically pleasing and much easier to follow. It's my own fault for not doing this from the beginning.
* Add Ethereum address and tokens for more donation options.

## Future Plans
* Add [Gemini](https://gemini.circumlunar.space/) support. The modern web has so many problems: tracking cookies, [proprietary client-side Javascript](https://www.gnu.org/philosophy/javascript-trap.html), non-Unix philosophy, [browser fingerprinting](https://coveryourtracks.eff.org/), [DRM](https://www.w3.org/TR/encrypted-media/) as a standard, etc. [Gopher](https://en.wikipedia.org/wiki/Gopher_%28protocol%29) is 30 years old and has suffered decline. [Gemini](https://gemini.circumlunar.space/) is more modern avoiding the limitations of Gopher and the pitfalls of the modern web.
