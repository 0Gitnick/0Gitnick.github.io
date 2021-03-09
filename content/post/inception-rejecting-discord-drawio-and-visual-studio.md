---
title: "Inception - Rejecting Discord, Draw.io, and Visual Studio"
date: 2020-03-30
tags: ["computing", "free software", "SIUe"]
summary: "This is my free software story. In the spring of 2018, I took software engineering at [SIUe](https://www.siue.edu). Software engineering is a junior level CS course. In my view, it serves as preparation for the more demanding two semester development effort that is the senior project. I'll call the professor, \"Professor X\" to preserve anonymity."
draft: false
---
## Background
In the spring of 2018, I took software engineering at [SIUe](https://www.siue.edu). Software engineering is a junior level CS course. In my view, it serves as preparation for the more demanding two semester development effort that is the senior project. I'll call the professor, "Professor X" to preserve anonymity.
    
## Story
### Project I
The first project was for the purposes of getting everyone accustomed to using Git and Redmine and working in a team as well as doing some documentation. We were put in groups of three to four and given the task of writing a fairly simple program with a GUI and some basic functionality in C#. I remember being very anxious upon forming a group because I knew my group members would likely want to use [Slack](https://slack.com) or [Discord](https://discordapp.com/) or some other popular proprietary walled garden messaging platform. Luckily for the first project of the class, my three group members were not thrilled, but were willing to undergo the inconvenience of downloading and using [Riot.im](https://riot.im/) / [Matrix](https://matrix.org/).
    
#### Communication  
It was awkward and uncomfortable to be the only person in the group refusing to use Discord when everyone else very quickly came to a consensus on it. Peer pressure is a real thing. But after explaining my reasons, I was able to win over the group after a few days and get everyone using Riot. I even got everyone to exchange their device keys over email so we could all have an encrypted group chat. The peace of mind of having an encrypted room and using free software instead of having our group messages data mined and sold as would have been the case with Discord cannot be overvalued for me. I didn't really win the group over by convincing them with the benefits of encryption and free software. I think they just wanted to get the project moving along and saw the easiest way forward was to adapt to me. So I got past the first hurdle.
    
#### IDE
I don't recall the specifics of the program, but it probably had some buttons and text boxes and would have been similar in difficulty to a graphical desktop calculator application. Our group did the required UML diagrams. The only thing left was to code the classes we diagrammed. This is where the trouble started for me. Professor X's project specification I believe was handed down from Professor Y who died unexpectedly. So Professor X was standing in for Professor Y teaching with his slides. Unfortunately I've heard Professor Y had a love for Windows and his project specification required everyone to use Visual Studio.
    
At this point I got worried because Visual Studio is proprietary software, and it was a battle with my conscience to use it or not. I definitely wasn't willing to install it on my personal machine. So instead, I found Monodevelop and was able to use it to complete project I. We still had to use Winforms for the GUI part which was awful, but at least I was able to avoid Visual Studio. The members of my group installed and used Visual Studio on their personal computers. So far, I had been able to completely avoid proprietary software.
    
### Project II
Project II was a similar story to project I except that I was in a group of three instead of four. This time, we were assigned a project called Cougar Delivery. The specifications outlined a delivery service we had to make software for. The delivery service software had to perform tasks such as tracking shipments, generating performance reports and cost of business charts, allow clients to order shipments and generate routes for shipping packages for the shipping business. It had many more requirements, so I won't list them all. But the idea was a single graphical application that enabled all the business operations related to running a delivery business. Realistically, this would have been divided up into several applications that handled general aspects of business such as finances, tracking, client and employee login systems and permissions, and more. But the point of the class was documentation and design rather than implementation.
    
#### Communication
Again, it was awkward asking everyone to use Riot when they had never heard of it. I had a hard time finding a soft way to propose using it when I wasn't willing to accept a proprietary alternative. But my two group members were willing to use it. I again was able to convince them to exchange device keys in person for an encrypted room. So far, all was well.
    
#### Documentation
And so we began our documentation. This time, I was not our project lead. Another team member had more time to work on the project, so he took the initiative. He was very diligent and before we had even started writing code, we ended up with an estimate of close to eighty classes total. We had polished UML diagrams for all those classes including package diagrams and UML class diagrams and a three tier architecture established before a single line of code was written. I was very satisfied with that. For my diagrams, I used [Dia](http://dia-installer.de/) and my teammates used [draw.io](https://app.diagrams.net/). Dia was difficult and annoying to use as far as alignment goes. It might have been due to my inexperience never having used it before, but I used it anyway for freedom. Draw.io is not free software. It uses proprietary Javascript and requires a software license to purchase the app. Nevertheless my teammates were able to at least export their diagrams in png format so I could see them using free software. Our project lead claimed to have used Dia before and said it was too inconvenient usage-wise.
    
The deliverables for the project were scheduled in such a way that we had to do all the documentation before starting the project, and continually revise documentation as the project went along. Our documentation was so effective that I trust we could've handed it to any other group in the class, and they would have been able to implement our entire design. Some of the documents were done using Google Docs regrettably. I strongly suggested using [Sandstorm](https://sandstorm.io/) instead since it is free software and doesn't require proprietary Javascript in the browser. That did not end up happening since I had other classes to worry about and we were crunched for time. If I could retake the class, I would have created a separate shared repo for documentation and used a word processor for editing instead. Our team lead did not see this as viable since he felt we needed to be able to see everyone else's changes in real time. There was a lot of talk about using Sandstorm, but I was never able to make it happen.
    
Another possible free software self-hosting alternative to Google Docs would have been an [Etherpad](https://etherpad.org/) instance, but public Etherpad instances did not have the plugins necessary for nicely formatting documents unless I self-hosted and installed them myself. And I guess I didn't have the time to set up an instance or something. But I did put a few hours of work in trying to get it working. It was very discouraging to be working so hard on something very tangientially related to our actual project. I wasn't able to move the group toward using Etherpad either. I ultimately ran out of time trying to make it work. I was the one pushing to use something besides Google Docs mainly due to its proprietary Javascript.
    
After I had been defeated unable to move the group to something besides Google Docs, I gave in to using Google Docs which I was able to use anonymously without an account. I just used the shared link. But I still had to run the proprietary Javascript in the browser which I now regret giving in to. This failure was very discouraging and harmed my motivation for doing the project. I discussed this extensively with the project lead but we weren't able to bypass the issue. After this failure, I didn't know the worse was still yet to come.
    
#### Testing Framework
We had to use a testing framework for the current project iteration to test our code. Of course our professor's hand-me-down specification and slides insisted that we use MSTest. I did some background research because it sounded proprietary. I found it was available for MonoDevelop, but when I went to install it, it asked me to read and sign a license agreement first. I believe it was proprietary based on the terms it was asking me to agree to when I tried to install it through MonoDevelop. I clicked decline. Instead of installing it, I dug in my heels and went to the professor after class. Regrettably, I did not mention the idea of free software very explicitly. Instead I talked about how I wasn't willing to agree to the terms so MonoDevelop could run the tests. He chuckled when I mentioned I wasn't using Visual Studio as the project requirements laid out, preparing for a potentially awkward conversation. And then when I mentioned not wanting to use the testing framework, he seemed perplexed. He told me I could write the unit tests and have a team member who has Visual Studio run them, thus bypassing agreeing to the license. This didn't satisfy me though, because it just passes the buck off to someone else. I definitely wasn't going to rely on my team members to agree to something I myself wouldn't. I let him know that I felt his idea didn't really solve the issue for me. I asked Professor X if I could use the NUnit testing framework instead, a libre library. He told me to ask the grader.
    
So I emailed the grader explaining in detail my ethical concerns about MSTest. He got back to me promptly admitting that he did not know about the ethical issue and would be willing to accomodate me given that NUnit could work in Visual Studio. It could, so I wrote my tests for our code using NUnit. I even rewrote some of our tests that had been written in MSTest into NUnit to increase the freedom of our project which wasn't too difficult. I had successfully dodged what could have became a freedom issue. I also discussed this with our group. They continued writing the unit tests using MSTest.
    
#### IDE
I thought I would be able to use MonoDevelop as before without any issues. I had solved the issue of the testing framework. What more issues could arise? The database. The instructions for the database in the database tier of our three tier architecture were written to explain how to use the SQL database in Visual Studio. It used libraries that only worked in Visual Studio if I recall correctly. This caused an inner conflict for me. I had never failed a class before, but I knew the professor wasn't going to rewrite the specifications in the middle of the project and it would be too much for the grader to try to get something else working and too much for me to research another solution. I talked about this issue ad nauseum to our group lead, who was sympathetic but tried to still convince me to just write the database anyway. I wasn't able to get him to really make sense of the freedom issue despite sending supporting links from the FSF website to explain my position. After heated debate, we eventually came to the compromise that I would only work on the part of our program that did not include the database. I would work on the other two tiers; the controller and graphical interface. I now regard this compromise as a mistake.
    
This still did not resolve the issue because I was unable to compile our program without having the SQL database that only worked in Visual Studio. I painfully forced myself to use Visual Studio in the university computer lab to write the project. This occurred with our team late at night all of us working furiously before the due date to get as much coded as possible and submitted. We were doing rapid trio programming because none of us had time until the last moment to work on the project. I was glad to have finished the project, but still giving in to using proprietary software did not sit well with me. I was ashamed of having given in but also understood my teammates would have had to give me a bad performance report if I outright refused to work on the project due to the database tier. So practically the choice was between failing and tacitly condoning Visual Studio by using it. I made the mistake of choosing to use Visual Studio to pass instead of putting my foot down and refusing and going to the professor again about the ethical issue. I think I didn't go to the professor again because I didn't want to inconvenience him too much to avoid another awkward conversation. I ought to have went immediately to the professor again to discuss the freedom issue. I passed the class with a good mark and accomplished the project, but still felt gross about giving in to proprietary software.