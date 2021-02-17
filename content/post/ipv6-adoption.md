---
title: "IPv6 Adoption"
date: 2020-12-25
tags: ["computing"]
summary: "There aren't enough IPv4 addresses to go around. IPv6 is long overdue. Find out how IPv4 still works and why we haven't fully transitioned to IPv6 yet."
draft: false
---
I try to make my posts accessible in the sense that I don't want to assume the reader has prior knowledge about a topic. So I'm going to explain a bit about IPv4 and IPv6 before I talk about how you can help with IPv6 adoption. If you're already familiar with IPv4 and IPv6 feel free to [skip](#IPv6_Adoption).

## IPv4
[IPv4](https://en.wikipedia.org/wiki/IPv4) stands for Internet Protocol Version 4. I'm not going to get into the OSI model and computer networking layers. It's enough to know that IPv4 is a protocol that defines how data is sent over the internet. IPv4 has a logical addressing system which allows packets to be routed from one computer to another. It's how your computer and the computer hosting this website can talk to each another. IPv4 specifies 32 bits per address which is about 4.3 billion logical addresses.

This was fine when the internet was small, but now the internet is massive and has more than 4.3 billion devices connected to it. This creates a problem since there are more devices than ways to address them. There are nuances like special addresses and addresses that are reserved but remain unused, but those aren't that important for our purposes. The problem is how can we route traffic across the internet since we've run out of internet addresses to hand out?

#### NAT
Welcome to [NAT](https://en.wikipedia.org/wiki/Network_address_translation). NAT stands for Network Address Translation. The main reason NAT exists is to solve the IPv4 problem of not having enough logical addresses for every device. NAT translates private IP addresses on an internal network to public IP addresses that can talk to other computers on the real internet. This allows several connected devices to share the same IP address, conserving logical addresses so IPv4 can still work. I won't go into detail on how this happens because it's not relevant, but it does have overhead. NAT is basically an ugly hack for the problem of not enough IPv4 addresses for each internet connected device.

## IPv6
[IPv6](https://en.wikipedia.org/wiki/IPv6) supercedes IPv4 using 128-bit addresses (340 undecillion IP addresses). It's the obvious elegant solution to the problem of not having enough internet addresses: use a protocol that has more addresses. It doesn't require NAT because each connected device can have its own IP address on the real public internet. Since the IPv6 address space is so huge, it's highly unlikely that IPv6 will ever be superceded for lack of internet addresses.

It also has other practical advantages to IPv4. As the name implies, it's a newer protocol drafted in 1998 whereas IPv4 was first deployed in 1982. IPv6 packets are easier for routers to process since the IPv6 packet is simpler than the IPv4 packet. This is consistent with the original vision of the internet where most processing happens at endpoints, not routers. [IPsec](https://en.wikipedia.org/wiki/IPsec) is mandatory whereas in IPv4 it was retrofitted. Network operators don't have to do port forwarding on the router or make firewall changes. Multicast addressing is simpler. IPv6 limits the size of [routing tables](https://en.wikipedia.org/wiki/Routing_table). [Mobile IPv6](https://en.wikipedia.org/wiki/Mobile_IPv6) is as efficient as regular IPv6. I could go on but the point is it's much better than IPv4 in every way.

## IPv6 Adoption<a name="IPv6_Adoption"></a>
ISPs and tech giants are slowly increasing IPv6 support. Ideally, everyone would use IPv6 and IPv4 would cease to exist. IPv4 has no practical advantages. It was superceded by IPv6 over 2 decades ago and the switch still hasn't completely happened yet. What's the problem? If IPv6 is better then why is adoption taking so long? The barrier to IPv6 adoption isn't so much at endpoints. By 2011 all major operating systems had support for IPv6. The problem is there often isn't a strong financial incentive for IPv6 adoption.

If you're an average internet user, you don't even know what IPv4 or IPv6 is. Unless your ISP enabled IPv6 for you then you probably don't have it. You can access all the internet resources you want without it anyway. Even if your ISP enabled it and your modem/router supports it, still many end-user devices and applications don't work well with it. If they do support IPv6, they also support IPv4 because IPv6 always runs alongside IPv4 with [dual stack](https://en.wikipedia.org/wiki/Dual_Stack). If you host any internet resource then all your users support IPv4. So why bother with IPv6?

#### Chicken and Egg Problem
IPv6 is still a clearly technically superior protocol. But IPv6 adoption is a classic [chicken and egg](https://en.wikipedia.org/wiki/Chicken_or_the_egg) problem. End-users don't adopt IPv6 because industry hasn't, so there's no practical advantages to it. Industry doesn't adopt IPv6 because end-users haven't, so there's no money in it. The problem with IPv6 adoption is creating the social inertia without immediate economic benefit. The easiest way to do that for most people is to call up your ISP and ask them to help you enable IPv6 for your home network. If you find that some internet services don't work with IPv6 then you can complain to those services about their IPv6 support. This creates social pressure from the end-user side to help speed up IPv6 adoption.

Whether you're a network administrator, provider of internet services or software developer, I encourage you to support IPv6 whether or not it will have any immediate benefit. You'll be helping the internet take its next step. You are the other side of the coin when it comes to IPv6 adoption. It's not a major selling point, but some users will appreciate it. We have to get over this chicken and egg problem of adoption. We can do that by going through a little extra trouble to help move the internet along. It has been 8 years since world IPv6 launch day and still the numbers for IPv6 adoption could be a lot higher than they are. Let's make it happen.

For updates on IPv6 adoption, check out the [World IPv6 Launch](https://www.worldipv6launch.org/blog/) site's blog. 
