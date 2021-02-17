---
title: "On Blockchain"
date: 2021-01-06
tags: ["computing"]
summary: "Can blockchain live up to the hype? Can its problems be fixed? What is its future? What about DAGs? What is the future of cryptocurrency? I have several predictions."
draft: false
---
Blockchain is a topic I've had thoughts on for a while now. I just never got around to writing about it. There's no shortage of wild, baseless assertions in the "crypto space" about the future of blockchain. I want to clear the air by speaking sensibly about blockchain. In accordance with my theme of not assuming prior knowledge, check out the [video](https://invidious.snopyta.org/watch?v=SSo_EIwHSd4&dark_mode=true&autoplay=1) below if you're unfamiliar with blockchain.

<div style="position: relative; width: 100%; height: 0; padding-bottom: 51%;">
  <iframe style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;" src="https://invidious.snopyta.org/embed/SSo_EIwHSd4" frameborder="0" sandbox allowfullscreen="true" referrerpolicy="no-referrer"></iframe>
</div>

I'm going to talk about blockchain in the context of cryptocurrencies. Henceforth understand when I use the term "blockchain" I really mean blockchain as used in cryptocurrency. I know there are other potential use cases but I have to limit the scope of this post or it won't end. Now while I have plenty of criticism for blockchain, first I have to give the devil his due.

## Blockchain's Successes
#### Cryptocurrency Markets
For starters the multi-billion dollar cryptocurrency market may not exist without blockchain. Even non-blockchain based cryptocurrencies reference the blockchain based Bitcoin in their whitepapers. While there _are_ functioning non-blockchain cryptocurrencies, they might never have been conceived without the initial inspiration from Bitcoin. Bitcoin is _still_ the most valuable coin and it _still_ uses blockchain. As I write this, it's nearing an all-time high of $30k USD per 1 BTC.

#### Smart Contracts
Shortly after Bitcoin [Vitalik Buterin](https://en.wikipedia.org/wiki/Vitalik_Buterin)'s blockchain based [Ethereum](https://ethereum.org) cryptocurrency hit the scene featuring [smart contracts](https://en.wikipedia.org/wiki/Smart_contract). Smart contracts are programs that automatically run on top of a blockchain. They enable decentralized exchanges, [ERC20](https://en.wikipedia.org/wiki/ERC20) tokens, [CryptoKitties](https://en.wikipedia.org/wiki/CryptoKitties), decentralized cloud storage payment, governance, and digital contracts. These use cases are only possible because of the security assurance blockchain provides.

#### Darknet Markets
Since cryptocurrencies enable anonymous irreversible transactions with no middlemen, they are used on [darknet markets](https://en.wikipedia.org/wiki/Darknet_market) which otherwise wouldn't exist. Some say darknet markets have done more to prevent drug-related violence than the DEA ever has. Those same markets also sell guns, stolen credit card details, and hackers for hire. It's hard to say one way or the other if they are an overall force for good. But darknet markets are _only_ possible because of the anonymity of blockchain.

Blockchain is a powerful, transformational technology still relevant twelve years after the [Bitcoin whitepaper](https://bitcoin.org/bitcoin.pdf) was originally published. Love it or hate it, there's no denying its influence on cryptography, pop culture and finance.

## Blockchain's Failures
You'll notice I still use blockchain to accept [donations](/about#donate) for this website. That's because I know of no better way to accept anonymous online donations. The moment I know of a better way I'll update my donation methods. If [GNU Taler](http://www.gnu.org/ghm/2020-january/taler.pdf) ever gains popularity, I will use it instead. In any case, I've given the devil his due, so now I'll move on to the problems with blockchain. And blockchain _is_ fraught with problems.

#### Blockchain Doesn't Scale
Blockchain's biggest problem can be summed up in one word: scalability. To make sense of blockchain's scalability problem, [CAP theorem](https://en.wikipedia.org/wiki/CAP_theorem) is a great place to start.

##### CAP Theorem
CAP theorem says you can have no more than 2 out of the 3 qualities in a __distributed data store__:

1. Consistency
2. Availability
3. Partitioning

In any distributed system, partitioning is a given. Blockchain _must_ tolerate arbitrary dropped or delayed messages in the network. Partitioning and network failures are just the reality of computer networks. The only choice left is between consistency and availability.

Consistency can't be sacrificed either. Nodes must agree on which blocks are included in the blockchain otherwise you don't have a blockchain. But that means the blockchain is sometimes unavailable. That's a big problem because if you're trying to perform a transaction, you can't have the client program telling you to come back later. No one would use that cryptocurrency.

To resolve this, __blockchain makes a tradeoff between consistency and availability__. Blockchain is _eventually consistent_. As the blockchain grows, nodes are guaranteed to _eventually_ agree on new blocks. In the Bitcoin blockchain large transactions are considered final after they reach 6 blocks deep in the chain. Transactions deeper than 6 blocks are _consistent_ across nodes.

As for availability, nodes in the Bitcoin network have a mempool. A mempool or transaction pool is where transactions wait to be included in a block. Any given transaction will find its way into a block which will eventually become a finalized block so long as the Bitcoin network isn't congested. The catch is Bitcoin can only perform about 3-7 transactions per second. Faster coins can handle tens or hundreds of transactions per second, but they all have some transaction limit due to the CAP theorem.

None of this is to say that cryptocurrencies can't scale. On the contrary __a scalable cryptocurrency with infinite transactions per second is inevitable as long as the crypto space continues advancing__. All it says is blockchain (distributed data store) can't scale up the way a cryptocurrency eventually must (infinite transactions per second). The logical conclusion is when an infinitely scalable cryptocurrency comes along it won't be blockchain based, at least not if that blockchain is a distributed data store.

#### Blockchain is Slow
A problem that arises out of blockchain's scalability problem is __blockchain is slow__. It takes time to finalize transactions. If transaction volume is very high, it can take an _indefinite_ amount of time to finalize a transaction. It could be hours or days. Even the fastest blockchains are torturously slow given high enough transaction volume. If you're buying goods at the supermarket that's useless. The cashier isn't going to stand there for 20 minutes waiting for your transaction to confirm. And they aren't going to take the risk of letting you leave before it confirms since you could perform a [double-spend](https://en.bitcoinwiki.org/wiki/Double-spending) in the meantime. If you pay a high fee so your transaction confirms quickly, you just drive the fees up for everyone, making the currency unusable.

I can hear blockchain enthusiasts objecting saying blockchain _can_ be fast because of "layer 2" solutions like the [Bitcoin lightning network](https://en.wikipedia.org/wiki/Lightning_Network). A layer 2 solution means not all transactions need to be included in the blockchain. If 2 parties transact frequently, they can establish a "payment channel" on the blockchain, perform transactions with instant confirmation off-chain, then confirm the final amounts on-chain after the payment channel expires. Once you and your favorite coffee shop have a payment channel open speed is no longer an issue.

My response to layer 2 solutions is that while they greatly _improve_ transaction speed, they doesn't _solve_ the fundamental problem. Instead of being limited by transactions per second blockchain becomes limited by payment channels per second. You still can't have infinite payment channels opened per second because that has to occur on-chain. In that case it's not _transactions_ that are slow. It's _opening/closing transaction channels_ that's slow. Layer 2 solutions will never scale infinitely when layer 1 is still subject to the CAP theorem.

#### Blockchain Price is Volatile
Another failure of blockchain that has nothing to do with scalability is price volatility. The price of Bitcoin for example changes dramatically. The market just can't decide how much Bitcoin or any other blockchain is worth. This makes blockchain a bad [store of value](https://www.investopedia.com/terms/s/storeofvalue.asp).

There are several economic theories about what gives something value. Like fiat currency, blockchain isn't backed by a commodity. It's backed by a combination of confidence, expectation, practical utility, [past value](https://wiki.mises.org/wiki/Regression_theorem) and because geeks think it's neat.

_Stablecoins_ are the exception to blockchain volatility. They keep the value of the coin constant. They are backed either by _other blockchains_, _fiat currency reserves_, or some _commodity_ like gold bars. But all of these solutions are problematic.

##### Other Blockchains
Backing blockchain with other blockchains is problematic since it pushes the problem of price volatility onto another cryptocurrency. It just passes the buck to someone else making for bad [coupling](https://en.wikipedia.org/wiki/Coupling_%28computer_programming%29).

##### Fiat Currencies
Backing blockchain with fiat currency is also problematic because fiat-backed stablecoins are _dependent_ on their fiat counterparts which in turn depend on large financial institutions and governments, effectively linking the success of the cryptocurrency with the success of the fiat currency. For maximum decentralization of power and independence, cryptocurrencies shouldn't be dependent on fiat in that way. It also passes the buck of price volatility to the fiat currency. This is bad because some fiat currencies have been even more volatile than Bitcoin!

##### Physical Commodities
Backing blockchain with physical commodities is problematic for a few reasons. Someone has to hold the commodity. Who's entrusted to do that and how is it decided? Furthermore, the reserves of the commodity have to be regularly audited for confidence in the value of the coin. The value can't be trusted any more than the auditing process. The auditing process must be decentralized and setting up a _decentralized_ auditing process everyone can trust would be highly complex. It's also _terrible_ coupling since the cryptocurrency is dependent on an external physical process carried out by people.

##### Digital Commodities
Backing blockchain with _digital commodities_ (not other cryptocurrencies) seems viable. Digital commodities are things like _processing power_, _disk storage space_ and maybe _smart contracts_. The advantage digital commodities have over physical ones is they can be audited automatically in a decentralized manner by the network rather than by people. They don't create unnecessary complexity or coupling. And they don't pass the buck onto another currency.

Therefore price volatility isn't an inherent problem of blockchain since blockchain can be backed by digital commodities. Of course there are other reasons blockchain continues to be volatile pricewise besides lack of "inherent" value. But those are _social_ problems related to blockchain. They don't necessarily have _technical_ solutions. For that reason I don't consider price volatility an inherent problem of blockchain. It's only a long-term problem for blockchains that don't back their coin with a digital commodity, which just happens to be most of them right now.

#### Blockchain Wastes Energy
Now onto another problem with blockchain that isn't an inherent problem but is serious enough to deserve a mention. _Energy usage_ is a problem for the subset of blockchains that are based on [proof of work](https://en.wikipedia.org/wiki/Proof_of_work). Proof of work wastes tremendous amounts of energy. Whenever I bring this up, proponents of proof of work immediately counter by saying the work isn't wasted because it's used to secure the blockchain. But this argument is circular. The blockchain only needs to be secured by spending energy because that's how it was set up. There are alternatives for securing blockchain that don't require such massive energy consumption. One of those alternatives is [proof of stake](https://vitalik.ca/general/2020/11/06/pos2020.html).

Saying that proof of work doesn't waste energy when proof of stake uses almost no energy in comparison and gets the same job done is like cutting your lawn with scissors one blade of grass at a time and saying it's not a waste of time because it gets the grass cut meanwhile you have a working lawnmower in the garage. Given, proof of stake is _newer_ than proof of work so we didn't always have a lawnmower. Scissors were the only option for a while. But it's 2021, we _do_ have lawnmowers now and there's no excuse to continue using scissors to cut the grass.

#### Blockchain Isn't Private
Every cryptocurrency that exists except [Monero](https://en.wikipedia.org/wiki/Monero_(cryptocurrency)) fails to provide users with privacy. The sender, receiver and amount transacted are all publicly visible to everyone. While there are no real names on the blockchain, online services link Bitcoin addresses with real people, deanonymizing Bitcoin. It also means Bitcoin isn't fungible.

Monero ensures that no one looking at the blockchain can see the sender, receiver or amount of a transaction by default. Monero still uses proof of work but there's formally verified [research](https://eprint.iacr.org/2018/1105.pdf) from 2018 showing that there's no contradiction with having both proof of stake and privacy. Privacy isn't an inherent problem of blockchain. It's just something most blockchains unfortunately aren't implementing.

## Blockchain's Inherent Problems
The only problem _inherent_ to blockchain is scalability. Speed is related to scalability so it can be considered as the same problem. But it's a fatal one. Blockchain cannot overcome its scalability problem. This is why blockchain is poorly suited for cryptocurrency. A new architecture is needed.

#### What About DAGs?
Cryptocurrencies that use directed acyclic graphs (DAGS) like [Iota](https://www.iota.org/) and [Nano](https://nano.org) do not solve the scalability problems plaguing blockchain because DAGs also require every node to see every transaction. Therefore CAP theorem applies and the same scalability and speed problems arise.

#### What About X Data Structure?
If it qualifies as a distributed data store (i.e. every node has to see every transaction) the CAP theorem applies and it can't scale infinitely.

## Why Infinite Scalability is Necessary
Some readers might think I'm making too big a deal of scalability. After all, there are cryptocurrencies that have layer 2 scaling solutions allowing thousands of transactions per second. Isn't that good enough? Isn't it committing the [black or white fallacy](https://yourlogicalfallacyis.com/black-or-white) to say that infinite scalability is necessary?

No. _Finite_ scalability isn't sufficient for a very simple reason. As I said before there will eventually be an _infinitely_ scalable cryptocurrency, a cryptocurrency capable of infinite transactions per second. And there's no reason to think that infinite scalability is in contradiction with any of the other desirable properties of cryptocurrency. Perhaps in the short term cryptocurrency projects that don't scale infinitely can compete with ones that do. They may _temporarily_ have some edge. For instance the first infinitely scalable cryptocurrency might not be as _private_ as Monero, so people will still use Monero. It might not support _smart contracts_ like Ethereum, so people will still use Ethereum. The price might not be as _stable_ as Tether, so people will still use Tether. But those are all problems that can eventually be solved. In the long term, cryptocurrencies that don't scale, no matter how high their maximum [TPS](https://en.wikipedia.org/wiki/Transactions_per_second), won't be able to compete with ones that do scale infinitely.

That's why _infinite_ scalability is vital for the long-term success of a crypto project.

## The Future of Blockchain
For a blockchain to scale every node can't see every transaction. Nor can every node see every open channel if you have layer 2 scaling. The moment you have not all nodes seeing all transactions you're no longer talking about a blockchain. You may be talking about _multiple independent_ blockchains, but that's not _a_ blockchain. In that sense blockchain can't scale.

If you combine my statement from the previous section that infinite scalability is vital for the long-term success of a crypto project and the fact that blockchain can't scale, you get my answer to the question of "Does blockchain have a future in cryptocurrency?". The answer is no. Blockchain has done well for the past decade and innovated and brought billions in investment into cryptocurrency which is all great, but it has no long-term future in cryptocurrency. I'll generalize that and say globally synced data structures (distributed data stores) have no long-term future in cryptocurrency.

That's all I have to say about blockchain. Now I want to broaden the scope to cryptocurrency in general. So let's talk about what the future of cryptocurrency might look like.

## The Future of Cryptocurrency
The market isn't going to be flooded with thousands of cryptocurrencies forever. Investors will _eventually_ realize that most cryptocurrency projects can't deliver on their promises and they will pull their money out. The fate of around 90% of cryptocurrencies is failure. Eventually there has to be a "thinning out" of cryptocurrencies and a consolidation of effort among projects that are making the most progress. Given that reality, my advice to cryptocurrency developers is this:

Developers in the crypto space need to reassess which projects are still worth investing time and effort into. While there are billions of dollars invested in the crypto space, interest is high and universities are teaching blockchain, it would be wise to focus research and development on the projects with the _best_ prospects for future success.

For example, [Monero is superior to Bitcoin](https://www.monero.how/why-monero-vs-bitcoin). It has [private transactions](https://www.monero.how/how-does-monero-privacy-work). Bitcoin doesn't. It has a [fairer proof of work algorithm](https://web.getmonero.org/resources/moneropedia/randomx.html). It has a [tail emission](https://www.getmonero.org/resources/moneropedia/tail-emission.html) so miners will always be rewarded. Bitcoin doesn't. Compared to more modern cryptocurrencies Bitcoin is pure garbage. Development effort in Bitcoin should therefore be redirected to Monero or for that matter any cryptocurrency with better prospects.

You might say the same thing about Monero. It will never scale unless it abandons blockchain. That most likely will never happen. Shouldn't research and development effort be redirected to a project that _will_ scale? And that's a fair point. I think about it by dividing cryptocurrencies into the following categories:

#### Next-Gen Cryptocurrencies
The cryptocurrency projects _most_ worth investment, research and development are those with real prospects of infinite scalability since scalability has been _the_ issue for a decade now. The other desirable qualities for a cryptocurrency are easier to add later but scalability is something that has to be designed for _from the beginning_. I'm not talking about temporary layer 2 scaling solutions that are only band-aids to the problem. Layer 2 solutions actually prove my point that in order to achieve _infinite_ scalability it can't be an afterthought. Scalability has to be baked into the design from the very beginning. I would place [Safe Network](https://safenetwork.org) in this category.

#### Useful Cryptocurrencies
Then there are projects in use today that work well and are likely to continue to be useful in the short-term (a few years), but they don't scale infinitely. They won't be viable long term. Investing time and effort into them _isn't_ a waste since they serve a useful purpose _now_. [Monero](https://www.monero.how) is a perfect example. It offers privacy. [Ethereum](https://ethereum.org) offers smart contracts and proof of stake. [Nano](https://nano.org) offers feeless instant transactions and decent scalability.

#### Outdated Cryptocurrencies
And then you have projects that have been important in the past, but should probably be abandoned now. They have _no_ unique properties that make them especially useful. They aren't making any major innovations. It's probably a waste of time to develop for them other than critical bug fixes. I'm looking at [Bitcoin](https://bitcoin.org), [Bitcoin Cash](https://www.bitcoincash.org), and [Litecoin](https://litecoin.com).

#### Vaporware
Finally there are the projects that are going _absolutely_ nowhere. They are held up by marketing and the illusion of progress through smoke and mirrors. They trick gullible investors and sometimes themselves into thinking they are the next big thing. When you look closely at their whitepaper and fundamentals it becomes clear their solutions don't work in the real world. [Iota](https://www.iota.org) is in this category. It's centralized, yet it has been promising decentralization for years with no way to get there. When evaluating these kinds of projects, remember Hanlon's razor:

> "Never attribute to malice that which is adequately explained by stupidity."

## Crypto Optimism
After dishing out so much criticism of blockchain and the crypto space, I want to end on a positive note. I'm actually very optimistic about the crypto space. With so many different cryptocurrency projects, things can seem like a chaotic mess. But out of the ashes of a thousand failed projects and lost savings will rise a phoenix. That phoenix is the first decentralized, infinitely scalable, fast, value stable, energy efficient, private cryptocurrency. It might take a long time to get there, but the mere technical possibility has me confident we will see it come to fruition. It will accomplish what Bitcoin originally set out to do.

Blockchain will be seen as a prototype, a stepping stone that kicked off something greater. There will be other "stepping stones" along the way. But scalability and the abandonment of globally synced data structures has to be the first. The other issues with cryptocurrency have only been solved in the context of globally synced data structures that don't scale. Those solutions won't necessarily translate over to a scalable context. When infinite scalability is finally achieved, we will hit the next milestone toward [Satoshi Nakamoto](https://en.wikipedia.org/wiki/Satoshi_Nakamoto)'s original vision of a decentralized, digital, free (as in freedom) financial system available to everyone but owned by no one.

_That_ is something to get excited about.
