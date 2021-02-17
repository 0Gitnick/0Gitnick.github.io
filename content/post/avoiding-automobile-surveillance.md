---
title: "Avoiding Automobile Surveillance"
date: 2020-12-16
tags: ["privacy", "society"]
summary: "Your car is probably spying on you and sending your data to private companies and the state. Connected cars are a relatively new threat to personal privacy, one that is getting _worse_ and doesn't get nearly enough attention. Find out how the surveillance happens and how to fight back!"
draft: false
---
## Internetification of Everything
Over the past few decades, there has been increasing "internetification" of everything. The [Internet of Stings](https://stallman.org/articles/internet-of-stings.pdf) has infected refrigerators, watches, televisions, and even light bulbs. As it turns out, shoehorning internet connected computer chips with [proprietary](https://www.gnu.org/proprietary/) code into everything increases their attack surface making society more vulnerable to [hacking groups](https://www.wired.com/2015/07/jeep-hack-chrysler-recalls-1-4m-vehicles-bug-fix/), foreign governments and Big Brother.

Automobiles are no exception. They've also seen increased internetification. My own personal opinion is cars don't need wireless enabled computer chips, period. And I'm [not the](https://www.huffpost.com/entry/is-apples-carplay-a-kille_b_4905981) [only person](https://blog.1871.com/blogs/howard-a-tullman/tullman-why-smart-cars-are-stupid-2) to think connected cars seem like a bad idea.

For this post, I want to focus on avoiding mass surveillance of automobiles. None of the recommendations in this post apply to [work vehicles](https://en.wikipedia.org/wiki/On-board_diagnostics#Vehicle_telematics) or car rentals since you don't own those. This guide is _only_ for your own personal vehicle.

## Don't Buy a Connected Car
My first piece of advice is don't buy a connected car. By connected car I mean a car with wireless capability other than radio. Buy an old car instead. Old cars predate the connected features of new cars. Ideally buy a car that doesn't support wifi, bluetooth or cellular connections. If it has a touchscreen it's probably too new. If you need navigation, you can buy a cheap car phone mount and use your phone.

If you already own a connected car, the best advice I can give is to trade it in for an old car. Until then read the owner's manual and find out how to deactivate as many of the connected features as you can. __Never pair your phone with your car__. Disable bluetooth and cellular connections on the car if possible.

## Eliminate Remote Diagnostics
Unfortunately even some old vehicles have remote diagnostics systems that collect and transmit vehicle sensor data wirelessly to the dealership, insurer, manufacturer or [thugs](https://stallman.org/glossary.html#thug). I'll cover these by category starting with the dealership.

#### Dealership Tracking
Automotive dealerships have [GPS tracking devices](https://www.spireon.com/gps-auto-tracking/) attached to cars primarily to prevent theft. When you buy a car, assume it has one and make the dealership agree to remove it as part of the terms of purchase before you buy the vehicle. Once you've bought the car from the dealership, there's no reason they need GPS tracking on it.

The exception of course is if you bought the car on a loan. Then either the dealership or the lender may require the GPS tracker on the car until it's fully paid for. In that case you can remove the GPS tracker yourself or have it removed after the car is fully paid for.

#### Insurer Tracking
Car insurers promote [remote telematics devices](https://www.carzing.com/blog/car-insurance/car-insurance-tracking-devices/) to policyholders in exchange for lower rates. They use the [OBD interface](https://en.wikipedia.org/wiki/On-board_diagnostics) in your vehicle to send real-time data to the insurer. Empowering Big Brother in exchange for cheaper rates isn't worth it. Don't let your insurer install tracking devices in your car. If your insurer requires them, find a new insurer.

#### Manufacturer Tracking
General Motors includes [OnStar](https://en.wikipedia.org/wiki/OnStar#Use_as_surveillance_device) in its vehicles. OnStar is a telematics device capable of not only remotely surveilling GM vehicles, but also listening to live audio inside the car and remotely shutting the car down. Even if you don't have a subscription, OnStar can still track your GM vehicle. In fact they tracked vehicles that weren't even subscribed to OnStar services until they [reversed the decision](https://www.consumerreports.org/cro/news/2011/09/gm-reverses-decision-on-onstar-privacy-policy/index.htm) due to public outcry from privacy advocates. Luckily there are plenty of guides online for [how to remove OnStar](https://www.wikihow.com/Deactivate-OnStar) so they can't possibly track you.

SiriusXM also collects telematics. Unlike OnStar, there's no way to remove it I'm aware of. You can cancel your subscription, but SiriusXM can still collect telematics. The only solution is __don't buy a vehicle that has telematics providers you can't remove__.

#### Thug Tracking
Big Brother can also demand telematics information about your car from any of the above categories. This isn't theoretical. It happened with [SiriusXM](https://www.documentcloud.org/documents/3295672-SiriusXM-Satellite-Radio-Tech-Turned-Into.html). Thugs have used [OnStar](https://www.documentcloud.org/documents/3295668-Coleman-Motion-to-Suppress-Denied.html) several times to remotely shutdown car engines. [ATX technologies](https://www.documentcloud.org/documents/3295666-ATX-Technologies-vs-US-Monitoring-of-in-Car.html) was forced to provide thugs with a live audio feed from inside a car.

Thugs are still allowed to put trackers on cars with a warrant. I'm not going to tell you how to spot covert thug GPS trackers. That's avoiding _targeted_ surveillance which is out of the scope of this post. This post is only about avoiding _mass_ automobile surveillance.

## Safeguarding Onboard Diagnostics
Onboard diagnostics systems (OBD) in vehicles were introduced in the 1980s. The USA, EU and other countries have mandated [OBD-II](https://en.wikipedia.org/wiki/On-board_diagnostics#OBD-II) and [EOBD](https://en.wikipedia.org/wiki/On-board_diagnostics#EOBD) protocols for all vehicles sold.

#### Emissions Testing
If you have a gasoline engine and you're in the United States, OBD data is pulled from your vehicle when you get mandatory emissions testing unless you get standard tailpipe emissions testing done. To find out if you can get only standard tailpipe emissions testing, you'll have to call and ask local emissions testing sites and check state regulations.

If the emissions testing site uses proprietary OBD scanning software, then it's possible that your data gets collected and sold to insurance companies by the OBD software vendor. If the testing site uses a handheld OBD scanner, it's still _possible_ that the data is eventually pulled off and sold if the handheld scanner connects to vendor software on an internet connected computer. The OBD-II interface has `Mode $09` which retrieves uniquely identifiable information like the [VIN number](https://en.wikipedia.org/wiki/Vehicle_identification_number). So if the OBD data does get sold, the data brokers know exactly whose vehicle it belongs to.

I've never heard of OBD data being involved in a data breach before. I don't have any information about what software is used by emissions testing sites. I'm just speculating. The only reason I have for thinking OBD data collection does happen at emissions testing sites through software vendors is because it can and it's profitable. Even if my speculation is true, you still have to get emissions testing done. I only mention emissions testing data collection for completeness and awareness, not because you can do anything besides political activism to prevent it.

#### Auto Repair Shops
When you take your car to a repair shop, one of the first things they're going to do is check the OBD-II interface for error codes. It's the same issue as before with emissions testing. The uniquely identifiable OBD data is exposed to potentially proprietary programs used by the car repair shop.

The difference is you don't have much choice in emissions testing. When it comes to auto repair, you have some choice. There are [free software diagnostic tools for OBD-II](https://github.com/fenugrec/freediag) that don't collect and sell your data. You'll need [an adapter](http://freediag.sourceforge.net/Supported-Interfaces.html#supported) supported by your vehicle to use them. It's up to you to make sure the adapter will work before you buy it. If you want to repair your vehicle yourself, then that's the end of it.

If you need the auto repair shop to repair your vehicle, you can relay the results retrieved from your free software tools to them while requesting they don't use their own proprietary OBD scanning tools.

## Networked Electric Vehicle Charging Stations
This section only applies to fully electric and hybrid cars. I've already made a post about [networked EV charging stations](/networked-ev-charging-stations). Just so this post is self-contained, I'll reiterate:

> There are two types of EV charging stations: networked and non-networked. The networked ones require you to sign up on the web with your real name, credit card information, address, and car make and model. You have to agree to the terms of service and privacy policy. After signing up, you receive a swipe card in the mail. Because you have to swipe an ID card to use networked charging stations, the network (Chargepoint) knows who you are, where you charged your car, when, and for how long. Non-networked charging stations don’t require you to use an ID card, so they can’t collect any personalized data on you.

Don't use the networked charging stations. Use the non-networked ones or just use your own charging cable instead.

## Automatic License Plate Readers
Automatic license plate readers or [ALPRs](https://www.eff.org/pages/automated-license-plate-readers-alpr) are cameras that capture all license plate numbers that pass by. There isn't anything you can do about these besides political activism against them. Purposely obscuring your plates from these cameras might be illegal or cause you to get tickets. Even if there's nothing you can do, I still think it's important to be aware of ALPRs.

## Consumer Surveillance
It may be possible to infer where you drive based on consumer surveillance alone. As a final piece of advice to further improve your vehicle's location privacy, follow the tips in my post on [avoiding consumer surveillance](/avoiding-consumer-surveillance).

## Political Action
When I make posts on how to avoid surveillance, what I'm trying to do is build resistance to tools of mass surveillance. At the end of the day there needs to be both technological and political changes to protect drivers' data. I offer temporary workarounds for avoiding surveillance until the dangerous trend of increased surveillance reverses itself. Society needs to start being _proactive_ rather than _reactive_ to corporate and government surveillance. I don't know when or how or if the trend of increased surveillance will be reversed, but I'll continue writing about ways to resist surveillance until I no longer need to.

At some point resisting mass surveillance becomes impractical. I understand my advice isn't always easy to follow. Choosing privacy can get expensive and time-consuming. And it's already hard enough to get people to use anti-surveillance tools that are _easy_ to use, let alone follow a guide like this that requires lots of effort. Part of the function of these posts is to show the ridiculous lengths one must go for privacy in today's world. You don't have to follow all the steps in this guide. My practical advice is just do what you can. Remember, if all you do is cancel your insurance tracking, that's a win for privacy and a blow to Big Brother.

If you have any more details or suggestions that I missed send me an [email](mailto:nicholasjohnson@posteo.org). If you want to help support my site [send a donation](/about#donate). I hope you found this post valuable.
