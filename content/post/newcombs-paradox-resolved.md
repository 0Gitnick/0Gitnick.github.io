---
title: "Newcomb's Paradox Resolved"
date: 2020-11-28
tags: ["philosophy"]
summary: "There is a _very_ subtle contradiction in the definition of Newcomb's Paradox having to do with free will. The \"choice point\" is _assumed_ to be after the predictor makes its prediction. In this post I demonstrate why that _can't_ be the case because it only makes sense to talk about a choice point _before_ the predictor's prediction."
draft: false
---
## Background
I "solved" [Newcomb's Paradox](https://en.wikipedia.org/wiki/Newcomb's_paradox) about 3 years ago if I remember right. I use solved in quotes because you don't really "solve" a paradox. Paradoxes only _seem_ to be contradictory at first glance. But, upon further inspection, they lead you to a new understanding of the problem where the paradox disappears. In other words, paradoxes arise out of a flawed or incomplete perspective. Newcomb's paradox in particular arises out of a misunderstanding of [free will](/free-will-is-incoherent-part-1).

## Telescoping Method<a name="Telescoping_Method"></a>
Before I give away the "solution" to Newcomb's Paradox, I want to talk about my method for solving philosophical problems in general. I call it the __telescoping method__. When I am confronted with a philosophical problem, the first thing I do is try to understand the _essence_ of the problem. To do that, I look at which _abstractions_ the problem uses. I break them down and down until the problem makes sense. Then, one by one, I build up the abstractions again so I can explain in words what the solution is. I've found it to be very effective for philosophy. I'll use Newcomb's Paradox to show how it works.

## Newcomb's Paradox
#### The Problem
Here's the problem from Wikipedia ([CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/)):

> There is an infallible predictor, a player, and two boxes designated A and B. The player is given a choice between taking only box B, or taking both boxes A and B. The player knows the following:
> 
> * Box A is clear, and always contains a visible $1,000.
> * Box B is opaque, and its content has already been set by the predictor:
>     * If the predictor has predicted the player will take both boxes A and B, then box B contains nothing.
>     * If the predictor has predicted that the player will take only box B, then box B contains $1,000,000.
> 
> The player does not know what the predictor predicted or what box B contains while making the choice.

#### The Paradox
Let's make it clear why this situation is a paradox before we attempt to resolve it. We are going to assume that the player is trying to maximize their profits. There are 2 strategies from [game theory](https://en.wikipedia.org/wiki/Game_theory) that you can apply to Newcomb's Paradox. 

The first is the [expected utility hypothesis](https://en.wikipedia.org/wiki/Expected_utility_hypothesis). It says you should take only box B. Its reasoning goes like this: Imagine you watched 1,000 philosophers play. Philosophers are split 50/50 on the issue, so about 500 would pick only box B, winning $1,000,000 and about 500 would pick both boxes, winning $1000. From a statistical standpoint, it's obvious you should pick box B.

The second is the [strategic dominance principle](https://en.wikipedia.org/wiki/Strategic_dominance). It says you should take boxes A and B. Its reasoning goes like this: After the predictor has made its prediction and either put the $1,000,000 in box B or not, it can't change the amounts in the boxes. Therefore, choosing both boxes will always yield $1000 more than choosing only box B. You should take both boxes.

At first glance, both of these principles seem very compelling. It's paradoxical because they offer conflicting advice. How can we resolve this?

#### Abstractions
##### The Infallible Predictor
As I suggested in the "telescoping method", we're going to break down the abstractions and make the problem more concrete. First, let's take note of the infallible predictor. Philosophically speaking, infallible predictors are really controversial. But we actually don't need an infallible predictor at all. Using basic algebra:

> Let p be the probability that the predictor is correct. Then:  
> `1000000p` is the expected value if you choose only box B.  
> `1000000(1-p) + 1000` is the expected value if you choose both boxes.
> 
> `1000000p > 1000000(1-p) + 1000`  
> `=> 1000p > 1000(1-p) + 1`  
> `=> 1000p > 1000 - 1000p + 1`  
> `=> 2000p > 1001`  
> `=> p > 0.5005`
> 
> Therefore the expected value if you choose only box B is greater than the expected value if you choose both boxes so long as the predictor is over 50.05% accurate, slightly better than a coin toss.

An AI system that can predict slightly better than a fair coin toss could create the Newcomb Paradox. Given what AI is already capable of, this is a realistic scenario. It also shows that the infallible predictor isn't the root cause of the paradox.

##### Intent
If it's not the infallible predictor causing the paradox, could the essence of the paradox have something to do with your intent? Newcomb's Paradox doesn't tell us that the predictor makes its prediction based on your intent. All it tells us is that the predictor is infallible. Therefore intent is irrelevant.

Even if your sincere intention is to pick only box B before the predictor makes its prediction, yet you change your mind and choose both boxes in the after prediction stage, the predictor will still correctly predict your choice and you will only win $1000.

##### Choice
We already examined the infallibility of the predictor and the player intent abstractions. They don't seem to cause the paradox. Perhaps the abstraction of choice is the problem? Newcomb's Paradox assumes it makes sense to talk about the player making a "choice" between 2 boxes and 1 box. But language to describe making a choice between several options is used in plenty of game theory problems. Even though I have shown that [free will is incoherent](/free-will-is-incoherent-part-1), using what I call "the language of free will" doesn't seem to be an issue for other game theory problems. Why then would it be especially problematic in Newcomb's Paradox? Allow me to defer to some dialogue between Neo and The Oracle from [The Matrix](https://en.wikipedia.org/wiki/The_Matrix):

> __Oracle__: Candy?  
> __Neo__: Do you already know if I'm going to take it?  
> __Oracle__: Wouldn't be much of an oracle if I didn't.  
> __Neo__: But if you already know, how could I make a choice?  
> __Oracle__: Because you didn't come here to make the choice. You've already made it. You're here to try to understand why you made it.  

Just replace Neo with the player and the Oracle with the predictor and it's the same concept. It seems we have found the essence of the problem. Free will is our leaky abstraction. The problem is the player can't really make a choice because, from the predictor's perspective, it has already been made. This leak can be ignored in most situations, but not with Newcomb's Paradox. The paradox arises _because_ we use language of free will. Talking as if others are free agents is built right into language. So what _can_ we say about Newcomb's Paradox?

#### The "Solution"
TLDR; choose only box B.

Long answer: There is a _very subtle_ contradiction in the definition of Newcomb's Paradox. Can you spot it? It says "The player does not know what the predictor predicted or what box B contains while making the choice". The hidden assumption there is that the "choice point" is _after_ the predictor's prediction. This is impossible. The abstraction of choice collapses after the predictor has made the prediction. If we have to pick a point in time where it still makes any sense to talk about a "choice" being made, it would have to be _before_ the predictor made the prediction. __The strategic dominance principle is _inherently_ tied to the idea of the player having a free choice _after_ the predictor made the prediction__. Therefore, it can't be the solution.

Meanwhile taking only box B is supported by mathematical expected value, which doesn't rely on free choice being available after the prediction. It just says "If you take only box B, you can _expect_ $1,000,000. If you take both boxes, you can _expect_ $1,000". There's no notion of free will there. It's a purely statistical argument. The strategic dominance principle only seems appealing because of the strong intuition of having a free choice _after_ the predictor has made the prediction. While [retrocausality](https://en.wikipedia.org/wiki/Retrocausality) doesn't actually occur in Newcomb's Paradox, it's not a bad mental model for thinking about the problem. Since the predictor is infallible, it has _effective retrocausality_. What the predictor did in the past is based on the box it already knows you're going to take. There's no real paradox, you just can't outwit the predictor even though your intuitions tell you that you "feel free".

You might think it doesn't make sense to prescribe players the strategy of choosing box B only, since they have "already made the choice" whether or not to take only box B. But, consider that by the same token, we have "already made the choice" whether or not to prescribe the player the strategy to take box B. So, it is equally coherent for us to prescribe the player to take box B as it is for the player to actually take box B. Saying there's no point in prescribing the player a course of action is akin to saying you'll just stay in bed all day since you have no free will. The "choice" to do nothing is _also_ not of your own free will. In other words, you're not escaping your lack of free will by doing nothing. We aren't escaping the lack of the player's free will by not prescribing them a best course of action as we don't have free will either. So, there's no reason not to tell the player to take only box B.

## Closing
Some of the points I've written down in this post come from my own intuition. I couldn't write a single methodology for how I come up with it all. In philosophy, it's hard to define a single methodology that can solve problems since each problem is unique and touches on many different things. Maybe some day someone will come up with an algorithm for doing philosophy. Although that would be equivalent to [finding an algorithm for truth](https://redirect.invidious.io/watch?v=leX541Dr2rU), so no one would be able to agree that it actually worked.

Nonetheless, the [telescoping method](#Telescoping_Method) is good for getting you on the right track. It can also lead you down rabbit holes. I would caution that you don't try to break down abstractions more than necessary. There's a reason we have abstractions. They make it easier to think. Once you start breaking them down, the conceptual complexity increases. For example, if instead of talking about boxes I started talking about the billions of atoms that make up the boxes, that just makes it harder to think about the problem. And it doesn't add clarity. Be careful not to do that unnecessarily.

Finally, in these dense philosophical essays, I welcome [criticism](mailto:nicholasjohnson@posteo.org). About half of philosophers think you should take both boxes, so don't get the impression that my opinion is the only one. If you think I'm wrong about the paradox, I'd love to get feedback. As always, thanks for reading and feel free to send a [donation](/about#donate) if you find my posts valuable.
