---
layout: post
title: 'The Hidden Architecturally Significant Requirements'
tags: [software_engineering]
cover-img: "/assets/img/SE_header.png"
---
Desiging software architectures is a widely covered topic by now, from lengthy books to quick Youtube videos and Medium posts. The process usually looks like this:

1. collect business requirements
2. derive some functional requirements (but don't dwell on them too much - although you actually should)
3. derive *especially* your NFRs (Non-Functional Requirements)/ASRs(Architecturally Significant Requirements) and specifically your QARs (Quality Attribute Requirements)
4. draft a notional architecture design
5. take the notional design through rounds of review/experimentation and refinement
6. validate
7. develop a detailed design
8. implement

There will be variations on this list but the above is meant to be a combination on which most developers/architects would have a basic consensus. You may think detailed design is unnecessary, no problem. You may think architectural experiments are a waste of time and resources, fine. As it very often is, software architecture is rife with zealotry to the different schools of thought, generalized personal experiences marketed as absolute truths, but also sensible and objectively valid criticism. Again, all good, but we won't dwell too much on that here as it's not the purpose of this post. As a practitioner of software architecture who also sometimes gets into "comment-section-style" discussions about it, I've had these discussions way too many times, and have come to the inevitable conclusion that it's like martial arts, everyone will do them (sometimes marginally) differently and refuse to accept that other styles may be better in some ways and think their style and master is the best ever for no tangible reason.

![](/assets/img/HiddenASRs/zushi_osu.jpg)

What I wanted to discuss here is more of subtle subset of requirements that I have consistently observed being either ignored or deprioritized for various reasons, when most of the time they present very risky ones that need to be deliberately analyzed and factored into architectural decision making.

I will name them: Simplicity, Reasonable Cost and Dev Team Match.

# Simplicity

Simple = simple to understand, simple to implement, simple to operate

Insufficient for scale, but open to extension

using higher level design primitives as opposed to using low level design primitives

the desire to use all we know/to learn a new tech by doing

the psychological barrier: while simpler may actually be more elegant in many cases, it is in some cases worse, but in many others just not an option because it "reflects badly" on how smart an architect is. I design a simple system therefore I'm simple-minded, or so it goes in the background. It's one of those performance anxieties that we all have at some point, before we start realizing that what matters most is how well a design does the job, and nothing else really matters.

# Reasonable Cost

Cost is a complex question, so to simplify it I will structure it along the lifecycle using an example: Let's assume you're out to develop a classic SPA which offers some asynchronous processing (transactions, deliveries, etc.) - by now it is a widely covered pattern and you already know that we will need some static web UI hosting, some auth, some API gateway/reverse proxy with all the bells and whistles (DNS, logging, analytics, etc.), backend logic, some DB, some storage and some message/task queue and workers.

I literally was too lazy to make my own deployment view so here goes:

and here's what you get (with some variation):

I am always surprised to find out that many architects would go the most DIY route with technology choice/deployment view for each of these elements of the stack. It would be understandable in some highly-constrained scenarios, but in most pretty relaxed contexts (no business constraints on platform, infrastructure and tools) it is often counter-productive to DIY.

I am also surprised by how much effort 

Implementation: out of the box vs own dev

Operation:

Maintenance:

Support:

Solution A, Solution B, cost for each, actually necessary cost for the current vs future requirements

Scalability is a moving target, not constant

# Dev Team Match


# Stylish But Unnecessary

Yes, yes. Many voices out there are telling you this, and I will add one more: don't overbuild, don't build for QARs you don't have but your "developer spidy sense" tells you you need them.
This isn't a warrant to get sloppy, this is rather a warning against writing a library nobody will ever use on your (or your employer's) dime. It's a great development exercise, it's fun, challenging, and interesting, but very often unnecessary unless the mission statement was *explicitly* to build a library with actual existing dev teams that are waiting to use it. Otherwise it's stylish but unnecessary. Some great examples of this can be found in "beautiful code" (link here).