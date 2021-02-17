---
title: "Site Update 007"
date: 2021-01-09
tags: ["info"]
summary: "Find out what's new on my blog."
draft: false
---
## What's New
I provisioned a new TLS certificate from [ZeroSSL](https://zerossl.com). That's why there was some downtime yesterday on 0gitnick.xyz. By default [Caddy](https://caddyserver.com) provisions TLS certs from [Let's Encrypt](https://letsencrypt.org) with a P-256 public key. I [don't trust NIST curves](https://safecurves.cr.yp.to/rigid.html) so 0gitnick.xyz uses a 4096 bit RSA key now. As of the time of this post all other clearnet [site mirrors](/about#Site_Mirrors) use 2048 bit RSA which is also secure.
