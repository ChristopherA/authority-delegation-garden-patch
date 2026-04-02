---
created: 2026-04-02
reviewed: 2026-04-02
brief_summary: "Cleaned transcript of Mark S. Miller's keynote at ActivityPub Conference 2019, Prague. Covers object-capability security model, Horton protocol for accountability, four-level intermediation taxonomy, pet name systems, cold-start trust problem, and Agoric's smart contracting vision. 77 minutes including Q&A."
tagline: "The Horton Talk — Miller's definitive presentation on robust openness for federated social systems"
cleanup-level: medium
source-format: generic
ai-transcription: "Unknown original transcription tool — raw text with speaker labels, no timestamps"
ai-processing: "Medium cleanup (App: Claude Code, Model: Claude Sonnet 4.6)"
---

- is_a::[[Transcript]]
- derived_from::[[Miller (2019) Architectures of Robust Openness]]

# Miller (2019) Architectures of Robust Openness — Transcript

## Introduction

**Christine Lemmer-Webber:**

So probably for me, the only thing more exciting than ActivityPub Conf itself happening right now is having Mark Miller as the keynote for ActivityPub Conf. I admire Mark for a number of reasons, one of which is that he's the only person I know who's extremely well-informed and also still seems optimistic about the future of humanity.

I had a conversation with him once where we were walking around and talking about some of the standards work that he's done. I said, "Do you think that some of that standards work" — because Mark's done quite a bit on JavaScript standardization — "was a distraction from your main goal of advancing security in this space?" And Mark said, "Oh no, I think I'm very proud that the last 30-plus years I've managed to stay focused on the vision and everything's culminating right now."

I wanted to give a little bit of history about what Mark's background is and how it relates to this space. First of all, Mark Miller was one of the main people in Xanadu, which was a precursor to the World Wide Web that we have today and informed many of its ideas. Maybe even had a lot of ideas that were better than what we ended up getting. Sometimes things are just before their time.

But I think where the journey really starts here is the Agoric Papers that Mark Miller wrote in 1988, which laid out a really out-there vision for a society of distributed computational machines where humans are in that loop of computation — and it really is a society. But my understanding is Mark didn't know how to build that society of computing machines when he first wrote it. Is that correct?

**Mark S. Miller:**

That's correct.

**Christine:**

He ended up learning that through his friend Norm Hardy, who introduced him to the idea of object capabilities. Mark, for over 30 years, has actually carried the torch of object capabilities and kept that community together for a long time without people really realizing why it was important. I think we're seeing a real acceleration of interest in it right now.

Another thing that's very relevant — I showed that video, that dancing guy and that other guy's face, yesterday — that was Electric Communities Habitat, which was a distributed online virtual world that allowed for secure collaboration in the late 90s. Those ideas survived in the programming language E.

When I was first told about E, I was already somewhat interested in object capabilities. My friend Asheesh Laroia, who was working at Sandstorm at the time, said, "Yeah, but everybody who's really interested in object capabilities is really excited about E." I tried looking at the E website and I was like, "What the heck is this thing?" I could not make sense of it initially. It really took until we met in person and Mark patiently explained a lot of ideas and drew out some of the things and said, "You need to see these things animated." You're going to see some of Mark's animations of these things live.

Aside from all of that, you actually use Mark Miller's work every day, because Mark has been pivotal in the extraordinary accomplishment of making JavaScript the only language that's gotten better over time rather than worse. A lot of that is because many of the good ideas in JavaScript actually came straight from E. For example, promises in JavaScript are straight out of E, and many other things as well. Mark has also been heavily involved in the development of WebAssembly.

Now Mark works at an organization called Agoric, which describes itself as the leader in smart contracts, and it really is the leader there. But I think a lot of people in this community probably have a misunderstanding of what smart contracts are because, due to Ethereum, most people parse smart contracts as being code that runs on a blockchain. It's not quite that — it's really about enabling secure collaboration between untrusted entities online. The work precedes blockchains by about 25 years.

Meeting Mark in person was in many ways a life- and career-changing event for me. It set a new track along the things that I thought was possible. I was interested in object capabilities, but in many ways I often dismissed them because I thought all these ideas look really good on paper but they're not usable. I kept coming up to Mark and saying, "Yeah, object capabilities are really great, but they can't do this thing." And Mark would say, "Oh, we actually already figured that out. Here's how to do this thing." And I'd be like, "Oh, okay... but they can't do *this* thing." And Mark would say, "Oh, we figured that out too." And I'm like, "Oh man, this next thing solves another 10 problems I had." That was a long series of engagements, and Mark was very patient with me.

One of the biggest breakthroughs — for those who know, object capabilities are about reference- or possession-based authority, the same way that your car, historically at least, didn't care who was driving it. Whoever had the key was able to turn it on and make it run. But human beings care a lot about identity. Who do you decide to give a car key to? And it seemed to me that object capabilities just didn't have any way to deal with this. Mark really changed my mind when we started talking about pet names and then about Horton — hence the Dr. Seuss reference. It turns out all these ideas can tie together, and when we tie them together, it opens us up to things we didn't know we could do before.

We have an opportunity to expand far beyond merely the kind of social network stuff we've seen in Web 2.0 — Twitter and Facebook and such — to something way beyond that. But we're going to need the ideas that Mark and his colleagues have been working hard on in order to do that.

Oh wait — I'm not going to hand over the microphone yet. I wanted to say one more thing. This is a real personal request. When Morgan and I sit down in the evenings, what we do for fun is read and drink tea, because we're boring people and we like being boring people. Very frequently, this is the book I end up reading. Do you recognize this? Can you say what this book is?

**Mark:**

This is my PhD dissertation.

**Christine:**

Could you read out the title?

**Mark:**

I've got to say, the number of people who recreationally sit around and read the dissertation is probably fairly small. *Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control.*

**Christine:**

Here's where it's really selfish. Mark, you know what a big fan I am. Can I have your autograph? Anywhere is good. Oh, but let's keep the water out of it. Can we get some napkins?

*[water spill, laughter]*

Luckily, it dispersed in a pattern that did not hit anything that would be seriously affected. And see, him signing — perfect, because he gave us a chance to clean up the water.

**Mark:**

How strategically we pre-planned that.

**Christine:**

Object capabilities are all about being able to prepare for making plans together and even being able to deal with the limited amount of damage when plans go awry. So, Mark, please give us some information.

## The Cooperation-Safety Tradeoff

**Mark:**

Thank you, Chris. That was an extraordinary introduction. I want to say that this 30-year journey was also a journey with many other people who were very much collaborators with me. Too many people to list, but I want to call out in particular: the Agoric Papers were co-authored with Eric Drexler, and Dean Tribble has been the closest partner with me through many phases of the journey, going back to Xanadu, going back to the origin of promises, and through today as co-founder of Agoric.

So today, let's talk about architectures for creating decentralized social networks that are both robust against attacks and open to strangers.

Tens of thousands of years ago, humanity lived in systems that were neither robust nor open. We were huddled together in small tribes where within the tribe we had nice social systems of cooperation with people that we knew. You can think of those as islands of green fields of cooperation in this vast sea of poisonous violence — violence both from predators and from other people that were generally assumed to be hostile and often were.

Over time we learned to invent systems that enabled us to cooperate better with each other — various patterns, various new institutions — and over time the cooperative networks between us grew through the phase transition to where they became the spanning networks that covered the world. These vast networks of cooperation becoming this world-covering green field of cooperation with isolated pockets of violence remaining.

It's very surprising to people to understand just how cooperative the world has become and in particular how non-violent it has become. We're all very aware of how violent it remains, but when you actually do a good comparison with history, today our world is extraordinarily less violent than it's ever been.

On this wonderful world of mostly non-violent cooperative interaction, there emerged a new level of abstraction — the online world. The world of the internet, the web, email. In its young days it was also this very pleasant worldwide friendly cooperative framework in which almost all interactions were pleasant and we could approach it with this simple, open-minded expectation of cooperation. And then a new form of problem started growing on the online world.

## Physical vs. Online Security

To understand the nature of the new problems we're facing, we need to understand the difference in security between the physical world and the online world.

One example that many of us might remember: in the physical world, we always had the problem of junk mail. It was a perpetual annoyance we all put up with — we would pick up our mail and then manually sort through and throw away all the junk mail. But it was feasible. With the coming of email we had many benefits, but we also had this explosion of spam. Something changed such that suddenly it was no longer feasible to manually sort through our incoming mail and throw away the junk.

There are two fundamental differences between security in the physical world and security in the online world.

In the physical world, we cannot build impenetrable walls. We can build stronger and stronger walls, but for every stronger wall there is a stronger degree of force that can penetrate it. By contrast, in the online world we have cheap, perfect boundaries. Our hardware gives us address space boundaries which we use to build operating systems. Our memory-safe programming languages give us object encapsulation. Modern cryptography gives us cryptographic primitives which are close enough to perfect for most purposes — most breaks in cryptographic systems are not due to weaknesses in the cryptographic primitives. So as far as just an isolation mechanism, when all you're trying to do is create a boundary, these mechanisms are perfect.

But the other fundamental difference is bad news for the online world. In the physical world, an attack takes scarce resources of the attacker. If nothing else, it takes some of the attacker's attention. People who make safes talk about work factor — the effort the attacker needs to engage in to overcome the defenses. If the expense of the work factor is greater than the value of the valuables in the safe, you're winning.

In the online world, the attacker can use automation to multiply their attack by billions at no cost to themselves. To the degree there's any cost at all, it's often a cost that the attacker arranges for the victims to pay — the victims' resources are used to spread the attack. As a result, a very small number of bad actors is able to multiply their bad activities by billions and flood the world again with poison.

The danger is that we react to that flood of poison by retreating back into fortresses — isolated communities where we have nice friendly interaction within the community but we're cut off from the larger world and we're not welcoming to strangers. That would be a tremendous tragedy for us to lose this sense of friendly worldwide cooperation.

There's always a tradeoff curve between cooperation and safety. In the early days of the internet, we were all naively cooperative with each other, not knowing that the nature of our cooperation left us unsafe. We didn't know it because no one was attacking us. As the attacks started increasing, the danger is that we simply go to the other end of the tradeoff curve and acquire our safety at the cost of sacrificing our cooperation at a distance.

What we need to do instead is lift the tradeoff curve. We can never get rid of the tradeoff, but if we lift it, then for the same amount of safety we can engage in more cooperation; for the same amount of cooperation we can engage in it in a safer manner.

## Access Control Paradigms: Identity vs. Authorization

One form of unsafety we've become familiar with is the unsafety that comes from centralized systems. Speaking here at ActivityPub, building decentralized social systems, we're aware of the dangers that come from centralization and we want the benefits that come from decentralization.

In any social system, a key issue is designation — how do you name things? How do you indicate something that you're talking about? Decentralized naming means we cannot rely on a central naming authority. But we want names that are free from impersonation, so no one can seem to be you. If someone can seem to be me in talking to my buddy, then they can phish my buddy into interacting with the attacker.

But we want to solve the impersonation problem without centralized naming authorities, because centralized naming authorities create a censorship problem. If we rely on DNS rooted in ICANN or certificate authorities or the phone company, then if our name is due to their activity, they can take it away from us. We want names that no one can take away from us and names that no one can prevent someone from communicating with us if they know our name and we want them to.

By analogy with another decentralized system that has shown these two security problems are simultaneously solvable: an account in Bitcoin is keyed to a public key. The holder of the account knows the corresponding private key. Impersonation resistance means no one else can generate a private key with the same public key, and therefore no one else can spend your money. And because you generated the key pair yourself, using it in a system that is itself decentralized, no one can stop you from spending your money. When you cross a border, no matter what the capital controls are, if you've memorized your keys, you can still cross and no one can stop you from taking your wealth with you effectively. We want the same kind of security and decentralization for our knowledge and ability to communicate.

So there are two fundamental safety problems we need to solve, two basic approaches to operating in a safe manner, which I divide into proactive and reactive. Proactively, we want to engage in activities such that we're safe by construction — we operate in such a way that by default we're not creating unnecessary dangers. But sometimes we'll mess up — we'll hand out authority inappropriately — so we need reactive damage control, the ability to react to bad things happening and recover.

The core of any security paradigm is its access control paradigm. There are two fundamental access control paradigms: the authorization-based paradigms, for which the main example is object capability, and the identity-based access control paradigms, for which the main example is access control lists.

Access control lists are the ones you're familiar with because all of our industrial operating systems are based on identity-based access control. The key thing about identity-based access control is that all access decisions are rooted in the question, "Who are you?" You perform an action, the action is tagged with your identity, and then depending on who you are, the action is either allowed or disallowed. This has many intuitive benefits but also many problems, and there's a long literature on the problems. The strength of this paradigm is its support for reactive damage control, but the problems make it very poor at proactively building safe arrangements.

## Object Capabilities Explained

Object capabilities, on the other hand, have their advantage very much on the side of proactively building safe arrangements. As Chris mentioned, the car key is a perfect example. The car key is a right — a bearer right. I have the right by holding the key. If I want to lend Chris the ability to drive my car, I just hand him the key. I don't have to tell my car that Chris is now able to drive it. The result is that we can delegate individual authorities in a fine-grained and piecemeal manner, in a flexible manner, and do it in a way that supports the Principle of Least Authority — the principle that each agent, both other people and software agents executing on our behalf, is given the minimal authority that they need to carry out the request we're making. By minimizing how much excess authority we give them, we minimize the potential for abuse.

But sometimes we will give out too much authority, sometimes we'll give authority to someone we regret having given it to, and then we need to react to having gotten ourselves into that bad situation. So what we need to do is build a system that has both of these strengths.

With these two foundations, there are really three logical ways to go about this.

One: we can start with the foundational mechanisms of access control lists and use those mechanisms in a surprising manner to support the benefits of capabilities. There have been some very good systems that have done this — Polaris, Plash, and BitFrost. They're interesting and worth studying. If you're stuck with access control foundations, it's worth engaging in those techniques. But these systems have problems under composition. They don't compose well, and they only help one more level deep, then they stop helping.

Two: in the 1970s and 1980s, there were a variety of hybrid capability systems. This is an intuitively obvious approach — build foundations that have both the object capability mechanisms and the access control list mechanisms, and an action is allowed only if it is allowed by both sets of rules. Unfortunately, these systems also showed problems under composition. In some ways, combining the attributes gave us the worst of both worlds.

So really, there's only one thing left to try: start with pure object capability foundations, and then try to build the attributes of the right-hand column by creating patterns of object capability use to get those benefits. That's the Horton work that I'll be explaining today.

But first, since it's unfamiliar, I'm going to explain object capabilities themselves. I want you to pay a lot of attention to the visual language I'll be using on this slide because I'll be reusing it throughout the rest of the talk.

I'll be explaining object capabilities in terms of objects of an object-oriented programming system because it's the best and closest analogy. But I want to emphasize that object capabilities are an abstract logic that can be built on many different substrates — object capability hardware, object capability operating systems, live cryptographic protocols, certificate systems — but I'll stay with the terminology of objects because it's closest to the logic we're familiar with.

In this diagram, the circles A, B, and C are three objects, and the thin arrows are object references — pointers from object to object in a memory-safe language where they're protected pointers, unforgeable. In these initial conditions, object A has a reference to object B, A has a reference to object C, and B does not have a reference to C.

In this situation, object A can execute code like `B.foo(C)`. Another way of describing this: A is sending the message `foo` with the parameter C to B. The parameter C is a copy of A's pointer to C. A is able to do this because A already has a pointer to B and A already has a pointer to C. And when B receives the message, B now has a pointer to C.

The main difference between objects and object capabilities is that these messages sent on these references are the *only* means by which an object can cause effects on the world outside of itself. The references — the thin arrows — are the permission system. In the initial conditions when B did not have a pointer to C, B could not invoke C, could not send it a message, could not provoke whatever activities would follow. A, by invoking B, both exercised its permission to invoke B and granted B permission to invoke C.

This has all of these nice benefits, but from the perspective of reactive damage control, when used directly it has the problem that all activity is anonymous. Object C, when it receives a message, doesn't know if the message came from A or from B.

The obvious approach might be to tag the message somehow or enable stack introspection where C can ask "was this message sent by A or B?" But there's a problem with that approach — essentially the hybrid capability approach. Objects are ephemeral. They come and go with great velocity. By the time somebody looks at what happened and decides that a particular message should in retrospect be judged as abusive, there is no object A anymore. Object A has already gone away, and so has object B. Attributing is pointless.

But providing permission at the granularity of individual objects is what enabled us to proactively build a system that was highly safe to begin with.

## Responsible Identity and the Horton Protocol

So what we need to do is separate the granularity at which we grant permission — which wants to be as fine-grained as possible — from the granularity at which we assign responsibility for bad actions. We need to retroactively say, "Alice, the larger unit — let's say a person — these objects executing on Alice's behalf have sent messages that in retrospect we judge to be abusive, so we're going to stop accepting messages from Alice."

These large-grain responsible identities can be people, corporations, or other organizations. The key thing is that they have a lifetime and an identity meaningful to a human being who's looking at the abuse and making a judgment. For the rest of the talk, I'll identify responsible identities with individual human beings.

Proactively, when abuse has not happened yet and no one has made any damage control decisions, we want a system that just operates as a simple object capability system in which object A — that happens to be run by Alice — can send a message to object B — that happens to be run by Bob. Before any abuse has happened, we want A to act as if it's pointing directly at B.

But what actually happens to enable reactive damage control is that the message doesn't immediately go all the way to object B. Rather, it goes to Alice's outgoing sentry. The sentry first asks, "Do I still make use of Bob's services?" Since no damage has happened yet, the answer is yes. But the sentry still records that we're asking Bob to deliver the `foo` message to B. Notice that we're recording Bob as the responsible entity even though at the object level we're sending the message to B.

Having recorded that, we send an encoding of the message over to Bob's incoming sentry, which first checks, "Do I still honor Alice's requests?" Since no abuse has happened yet, the answer is yes. But Bob's sentry still writes down that we're about to deliver the message `foo` to object B on behalf of Alice, so that in retrospect we can decide to hold Alice responsible.

With all that bookkeeping done, we now proceed to deliver the `foo` message to B. I'm going to use this graphic — the identity tunnel — as shorthand for that system of sentries for the rest of the talk. Every time you see this graphic, you should understand that there is an object at each end acting as a sentry for the respective parties.

There have been systems built on these principles. The Scoop system at HP Labs — Secure Cooperative File Sharing — was a decentralized file sharing system where various parties could arrange to propagate file updates to each other and keep track of permissions. If I find that a particular file of mine has become full of garbage and I can see that the update came from Marcus, I can decide to cut off Marcus's further access. I'm holding Marcus responsible.

## Units of Responsibility

But what is the unit that I'm holding responsible? It's a little too simple to say the unit is simply Marcus the person. These spheres represent our units of responsibility in the system.

Alice the human interacts with the system by interacting locally with her software running on her machine — assuming a fully federated system here. She interacts with that software through her local user interface. Her software then sends messages over the network to Bob's software, which renders through Bob's user interface information that Bob the human can react to.

If Bob is getting abusive messages from the Alice unit, Bob doesn't need to know or care whether these abusive messages are coming because Alice is running malware or because Alice has turned evil. In both cases, Bob will hold Alice responsible for the bad action of her objects. Not a moral judgment — if Alice is running malware sending the bad messages, it's not Alice's "fault" in some sense — but Bob has to hold Alice as a whole responsible in the absence of any other evidence.

## Pet Names and Naming Integrity

With this picture we can now better understand the issues in doing a decentralized naming system with integrity.

There are several different languages being translated between. If Alice wants to send a message to Bob giving him permission to turn a lamp on and off — what Alice sees through a user interface has to be human-meaningful, something she can feasibly understand. Her local software translates this into an internal language — messages between her local objects with a representation of which lamp the permission is being conveyed to. That gets translated into a cryptographic message where there's a cryptographic representation of permission to use the lamp, which not only designates the lamp but actually provides the permission. Bob receiving that cryptographic permission is now able to use the lamp, whereas otherwise he would not have been.

When received by Bob's software, it gets translated back into the internal language of objects, then rendered into Bob's user interface, where the concrete representation might be different than what Alice sees. We don't care about that. What we care about is that they both mean the same thing — the lamp that Alice meant to give to Bob, when Bob receives it, he knows that it's the lamp that Alice meant.

To achieve this, we need a naming system with three key properties. It has to be free of impersonation — no one can appear to Bob to be a different Alice than the one Bob thinks of as Alice. It needs to be censorship-resistant — we cannot depend on an external centralized naming authority. It needs to be human-meaningful — these names have to show up in user interfaces, so any user interface that tries to identify something by showing a human being a big cryptographic key is a failure. And it needs to be globally meaningful — like a cryptographic key, it can go anywhere on the network and in a context-independent manner grants authority.

Zuko's triangle is the insight that there is no one kind of name that can have all three of these attributes. However, we can have kinds of names that have any two of the three. And we're already familiar with a naming system that shows us how to get all three by having multiple kinds of name, where each kind only has two out of three but the naming system translates between them.

We all have phones with contact lists. The name we place into the contact list is our pet name — the name we privately choose for the various parties we're communicating with. Even when we communicate with them, they never know what our pet name is for them. When Alice calls Bob, she looks up "Bob" in her contact list. Her software translates between her contact list and the phone number. The phone number is a numeric address that's not human-meaningful but, imagine instead a cryptographic key. When Bob receives the call, his software translates in the other direction, from the address back to the pet name.

## Introductions and Corroboration

In a social network, the interesting other objects for Alice and Bob to talk about are not lamps but other people. Before we get into the technical details, I want to mention something that happened to me this morning on the way to ActivityPub, which is I called Uber and then something amazing happened. Somebody that I've never met before showed up in a car I've never seen before, and I got into that car. Also, from the driver's perspective, something amazing happened — they stopped the car and somebody they've never met before walked up and opened the door, and the driver drove off with that stranger in the back seat.

Why does this work so well that we're starting to take it for granted? Because Uber, in the role of Alice, has communicated to both Bob and Carol enough information that they can authenticate each other. "Authenticate" doesn't mean that Carol knows precisely who Bob is. That's not the question she's asking. The question she's asking is: "Is this the Bob that Uber meant to introduce me to?" And likewise Bob is asking: "Is this the Carol that Uber meant to introduce me to?"

In our system, Alice sends to Bob a message using her pet name for Bob in the "to" field. But the key thing is she can use her pet name for Carol in the body of the message, and her software knows to translate it. She's telling Bob, "Meet Ms. Smith" — because Ms. Smith happens to be Alice's pet name for Carol. That turns into an object-to-object message sent into the identity tunnel. The meaning of that introduction message is that Alice is asking Carol to provide Bob access to Carol's object C.

Carol might never have heard of Bob before, but here's Bob's identity in the introduction message. She sets up an identity tunnel for Bob's use, gift-wraps Bob's end in such a way that only Bob can unwrap it. When Bob unwraps it, he knows only Carol could have wrapped it. Carol returns the wrapped gift to Alice, who uses it in a message through Alice's identity tunnel to Bob. Bob unwraps it, recreating the meaningful message whose parameter is now carried over the new identity tunnel by which Bob and Carol hold each other responsible.

But at this point in the protocol, does Carol really know that Bob is independent of Alice? The answer is no, and necessarily no. In any such system, Carol has to wonder whether Bob is a pseudonym for Alice. Whatever bad behavior Bob engages in, Carol has to hold Alice responsible for it as well.

It's still meaningful for Carol to hold Bob responsible and to do all the bookkeeping for that. Let's say Carol and Alice have a history of good interactions, so a minor bad message from Alice would cause Carol to demerit her sense of Alice's trustworthiness by one, but not to cut off access. On the other hand, if a bad message comes from Bob — Carol has no history with Bob — one bad message is enough to cut off Bob's access, but Carol should still demerit Alice's access by one. Suspect that Alice might be starting a pattern of abuse, but know that Bob might be independent.

Secure Scuttlebutt, a decentralized social network based on pet names, shows us the right basic approach: only joint introductions corroborate independence. When multiple different people have all introduced Carol to the same Bob, that gives Carol significant evidence that Bob is independent of any one of them. When Dave performs a second introduction between Carol and Bob, that gives Carol evidence that Bob should be treated as independent of both Alice and Dave, and the same introduction also gives Bob evidence that Carol should be treated independently.

## Cold Calling and Welcoming Strangers

So we've shown how to build a decentralized, federated social network with naming integrity, where names are not subject to either impersonation or censorship. We've done it through what Chris described as networks of consent — introduction messages that players have chosen to do to introduce people they know to each other. The introductions are meaningful because they're coming from people you know.

Have we succeeded at building a system that is welcoming to strangers? In many ways yes, but in some fundamental ways, not yet. Object capabilities have the slogan: only connectivity begets connectivity. If you have two isolated subgraphs, they remain forever isolated because no one can introduce them. This can degenerate into fortresses — the phenomena sometimes called the "old boys' network," where a stranger coming from the outside has no way to knock on the door of a community they'd like to participate in.

We want to add a cold calling primitive. I mean people in the network want to be able to say, "Here's the inbox — here's the separate inbox at which I will accept messages that don't come from an introduction."

We need to understand the danger of publicly providing such an inbox. The problem with spam was the lack of marginal cost — the lack of any scarcity per attack on the part of the attacker, enabling the attacker to multiply their attack by billions at no cost. The thing that prevented the *explosion* of the junk mail problem — not the irritation, we still got junk mail — was the stamp. The stamp is a small marginal cost per message. For a normal friendly cold call, a small number of stamps is not an undue burden. But if you want to send billions of such cold calling messages, then suddenly a cost per message becomes significant.

PetMail was a prior decentralized federated social network that operated with these principles. As you can guess from the name, it was also a pet name system with corroboration logic, but furthermore it had open public inboxes for cold calling with a per-message cost — using CAPTCHAs. A CAPTCHA is a perfectly fine way to cause per-message overhead if CAPTCHAs still worked. Given the state of artificial intelligence, we should assume CAPTCHAs cannot continue to work, and pretty much they don't already. Some mechanism still needs to successfully cause a marginal cost to the attacker.

The nice thing about stamps — about money transfer — is it also compensates the victim. As Chris mentioned yesterday, if people are cold calling me with messages I'm not interested in, well, they've paid for the privilege and I've benefited by receiving their payments.

## Architectures of Robust Openness

What these patterns are doing is enabling us to figure out how to successfully cooperate with strangers, allowing us to extend our networks of cooperation to the point that these large-scale networks of worldwide cooperation through federated decentralized systems are the ones that cover the world — and to beat back the abusive activities back into isolated lakes of poison within this vast landmass of green fields of cooperation.

It's not a perfect solution, just as it wasn't in the physical world where violence continued to happen. There will still be people at those peripheries who have to engage in skepticism. But the hope is that this overall system of networks of consent, cold calling with immediate feedback, attribution, and the ability to engage in reactive damage control can be at least the first step towards the patterns we need to escape from our fortresses and cover the world with decentralized networks of cooperation.

So we've rebuilt an identity-based system for reactive damage control on top of our object capability basis. How did we do compared to identity-based access control systems people are familiar with?

Like them, requests were tagged by the identity of the requester so you could hold the requester responsible. Unlike them, we've also done the record-keeping to hold the *responder* responsible. When Alice's software makes the `foo` request to Bob's software, Alice records that she's holding Bob responsible for how his software reacts. And we're assigning responsibility for introductions — so Carol, when she receives abusive requests from Bob, can not only hold Bob responsible but understand the introduction structure by which she came to know Bob, and hold Alice responsible to a reduced extent.

Together this is an architecture of robust openness. We've achieved naming integrity with no naming authorities. We have a skeptical aggregation strategy where Bob's bad activity is still aggregated into Alice, but a corroboration-driven disaggregation strategy where Carol can learn that she can hold Bob separately responsible. And by supporting cold calling with a small cost to the sender, we have made the system open to strangers. A stranger, once entering the system, no longer has that initial cost — they are now within these networks of consent and can proceed to interact without paying further cold call costs.

And now I'll take questions. Thank you.

## Q&A

**Audience Member 1:**

It feels like programming an object capability system is like learning a new language, a human language. How would we go about learning object capability programming idioms such as composition and decomposition?

**Mark:**

Well, I'll give a flip answer first, which is you can do what Chris and Morgan are now doing recreationally — read my dissertation.

But more seriously, the first thing is to pay attention to user interface design, so that the users of a system built according to these principles do not have to understand the principles in an articulate manner in order to use it safely and successfully. To make the appearance of them through the user interface something which is intuitive at very little effort — ideally intuitive out of the box.

Chris mentioned yesterday that a group from Rebooting Web of Trust, including Chris and I and including you, are co-authoring a paper on specifically how to bring these issues out into the Mastodon user interface — to create a Mastodon-like experience that can be understood without having to sit through this talk, understood intuitively, to provide the naming integrity properties that we're advocating.

With regard to object capabilities themselves, leaving aside Horton — the language of object capabilities, the basic ideas, the patterns — are very similar to those that object-oriented programmers engage in. The abstractions with which object capability programmers create security patterns like Horton are very much along the lines of how object-oriented programmers create patterns of objects to express higher levels of abstraction.

We found repeatedly that people coming from object-oriented programming can take up object capability programming very quickly. What we've also found is that people coming from other security paradigms take up object capabilities less quickly, because the difference in the arrangement of computation and identity is a bigger burden than the difference between object-oriented programming for functionality versus object capability programming for both functionality and security.

Learning object-oriented programming was something that took the world 20 years to do, so there is definitely a big language learning burden there — but that's a burden that for many tens of millions of programmers is already behind them.

I should mention that my company, Agoric, is building a decentralized object capability system on top of an object capability runtime for JavaScript. JavaScript will seem surprising, but I've been on the ECMAScript committee since 2007. I got the enablers from E into the JavaScript standard to enable JavaScript to be used as a safe object capability programming language. That immediately opens up the ability for programmers to write security patterns using both object patterns they're used to and a language that's familiar to them.

**Audience Member 2:**

You teased this with the Agoric innovation. Could you put it not in a developer context but in the context of your presentation as a whole — the role of the company?

**Mark:**

What does Agoric do? At Agoric, we're building support for smart contracting that can realistically be used in large-scale collaborative networks of commerce and complex voluntary cooperative interaction that we hope to span the globe — to bring the world economy online through these primitives in such a way that we provide the benefits of rule of law to everyone cheaply.

Kate Sills just did a talk that's going to be up on YouTube called "Can Blockchains Provide Rule of Law?" There are something like 4 billion people in the world who do not have the benefits of rule of law because of the expense of lawyers and human adjudicators. Even in countries that have the rule of law, it's often practically out of reach because the cost of using the mechanisms is too great. A smart contracting fabric can enable those benefits at incredibly tiny costs — by eight orders of magnitude.

We can make the contracts unambiguous because they're code, not prose to be interpreted by humans, and uncorruptibly executed because they're running on computers that the mutual parties to the contract can trust.

Since I said "blockchain" — to us, a blockchain is only one of many platforms. We're building a decentralized distributed smart contracting fabric on top of JavaScript that runs in a blockchain-independent manner, but also across chains and non-chains, across both public and private systems, so that it can be a fabric of cooperation of maximum reach.

To us, the important thing about a blockchain is that it's a mutually trustworthy computer — a program running on a blockchain has worldwide credibility that it executes according to what the code says. For some contracts that's very valuable. Many contracts are local, don't need public blockchains, don't want the public visibility. Any other arrangement the cooperating parties can come to for mutually trusting the platform is adequate for participating in the overall fabric.

## Closing Remarks

**Christine:**

I think we got to wrap it up. I want to elaborate on one point: the one thing that's really important to make clear is that object capability programming is just normal programming. If you remove global state, it's just argument passing between functions. It doesn't require object-oriented programming — you can do it in functional systems. It's literally just that your variable references are object capabilities and you pass them between functions. That's it.

So with that said, we have an unconference to prepare for. We have 12 minutes, though we have scheduled an hour for lunch and we can do a little bit of rearrangement. Many people have thankfully already written down topics they'd like to propose. We have post-it notes representing the rooms and times. As a community, you should negotiate with the other people who've written things they're interested in and try to collaboratively rearrange the schedule so that people are mostly happy and able to go to the things they're excited about. So let's get to it!
