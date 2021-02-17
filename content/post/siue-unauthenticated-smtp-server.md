---
title: "SIUe Unauthenticated SMTP Server"
date: 2020-09-21
tags: ["computing", "SIUe"]
summary: "American colleges and universities are institutions with some of the weakest cybersecurity where you would expect better. This makes them easy targets for hackers. The reason is they don't have strong incentives to do better. Unless having poor cybersecurity is going to lose money, business as usual will continue and unauthenticated email servers will stay online."
draft: false
---
## Email Server
During my last semester at [SIUe](https://siue.edu), one of my professors demonstrated spoofing an email using an unauthenticated SMTP server (smtp.siue.edu) on the university network. I believe the server is still present on the network despite being reported multiple times to IT. It isn't accessible on the public internet, only through the university's network that all students have easy access to. Non-students could also gain access to the network fairly easily while at the university and therefore have access to the email server.    

The email server has no authentication whatsoever. You don't have to offer any credentials to send emails. You can't read others' emails, however. This means you don't even need to be a student to send emails. As a non-student, you can access the email server through Telnet and send emails as any student, professor, faculty or staff member. With that, you can send out emails to any email lists. This unauthenticated server has been present on the network for years according to other students I have talked to.    

I hope the server gets taken off the network, but this underscores a larger issue. American colleges and universities are institutions with some of the weakest cybersecurity where you would expect better. This makes them easy targets for hackers. The reason is they don't have strong incentives to do better. Unless having poor cybersecurity is going to lose money, business as usual will continue and unauthenticated email servers will stay online.
