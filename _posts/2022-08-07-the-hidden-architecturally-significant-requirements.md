---
layout: post
title: 'Unmasking Overlooked Essentials: Simplicity, Cost, and Team Compatibility in Software Architecture'
tags: [software_engineering]
cover-img: "/assets/img/SE_header.png"
---
Designing software architectures is a widely covered topic by now, from lengthy books to quick Youtube videos and Medium posts. The process usually looks like this:

1. collect business requirements
2. derive some functional requirements (but don't dwell on them too much - although you actually should)
3. derive *especially* your NFRs (Non-Functional Requirements - a name I don't like for these)/ASRs(Architecturally Significant Requirements) and specifically your QARs (Quality Attribute Requirements)
4. draft a notional architecture design
5. take the notional design through rounds of review/experimentation and refinement
6. validate
7. develop a detailed design
8. implement
9. 7/8 feed back into architecture design updates

There will be variations on this list but the above is meant to be a combination on which most developers/architects would have a basic consensus. You may think detailed design is unnecessary, no problem. You may think architectural experiments are a waste of time and resources, fine. As it very often is, software architecture is rife with zealotry to the different schools of thought, generalized personal experiences marketed as absolute truths, but also sensible and objectively valid criticism. Again, all good, but we won't dwell too much on that here as it's not the purpose of this post. As a practitioner of software architecture who also sometimes gets into "comment-section-style" discussions about it, I've had these discussions way too many times, and have come to the inevitable conclusion that it's like martial arts, everyone will do them (sometimes marginally) differently and refuse to accept that other styles may be better in some ways and think their style and master is the best ever for no tangible reason.

![](/assets/img/HiddenASRs/zushi_osu.jpg)

What I wanted to discuss here is more of subtle subset of requirements that I have consistently observed being either ignored or deprioritized for various reasons, when most of the time they present very risky ones that need to be deliberately analyzed and factored into architectural decision making.

I will name them: Simplicity, Reasonable Cost and Dev Team Match.

# Simplicity

![](/assets/img/HiddenASRs/complex_machine.png)

Simple = simple to understand, simple to implement, simple to operate.

Complexity is the fastest way to fail, it inevitably balloons engineering, operation and support/maintenance costs. It's such a simple idea yet so elusive to many software engineers, especially those who lack experience or think "they have something to prove" by using the most cutting edge complex architectures to solve trivial problems and thus prove they're "knowledgeable". I was that guy at some point, but I quickly got out of that phase and understood it's very counter-productive and proves nothing in the eyes of someone who knows their stuff.

We all want to learn tech by doing, but as a professional who owes their employer and their client quality work, don't experiment on their expense. Meaning: it's okay to prototype using a new technology to you. It's not okay to stubbornly stick to a technology you want to learn all the way through implementation and delivery just for you to learn how to work with it, when there are better (and simpler very often) alternatives.

But I also take simplicity a step further: Design an architecture insufficient for costly ASRs first, but keep it open to extension and improvement later. I'll take as an example "scalability": Unless you're working for a unicorn that just figured out how to levitate matter without expanding energy and needs to scale overnight, you have plenty of time to scale out your architecture. This doesn't mean "use inherently unscalable architectures", no, this means "leverage scalable primitives", self-contained easy-to-scale-out containers, lambda functions, DB and storage services, etc. Implementing advanced scalability costs a lot, if you're trying to squeeze out every cent of cost while keeping your services responsive. Deferring that is a healthy practice for young products.

Another aspect of simplicity is "use higher level design primitives instead of low-level primitives", meaning: a service rather than a code module, a generic storage service rather than a specific DB system. This helps you focus on discovering the attributes you need them to display then choosing a technology and not being stuck under self-imposed constraints by moving to specific solutions too fast.

Simplicity is always the victim of a psychological barrier: while simpler may actually be more elegant in many cases, it is in some cases worse, but in many others just not an option because it "reflects badly on how smart an architect is". I design a simple system therefore I'm simple-minded, or so it goes in the background and in the hallways/chatrooms of big enterprises used to multi-million projects that deliver something an intern could've developed in a capstone project. It's one of those performance anxieties that we all have at some point, before we start realizing that what matters most is how well a design does the job, and nothing else really matters.

My tip is always: start simple, flexible, then grow from there. It's a path that allows also enough slack for you to adjust as you discover more requirements while implementing (because of course more will appear, make no mistake).

# Reasonable Cost

![](/assets/img/HiddenASRs/time_cost.png)

One mistake I always see being made is teams designing for multi-million daily active users when they will at most get a couple of thousand users a month, or designing "an everything software" for a very limited purpose, or "using design patterns" for a one-time piece of software that none will ever reuse. It's a choice that usually stems from loose requirements coupled with the desire to "copy the industry gold standards", embodied in reference architectures from the FAANGs of the world, who process tremendous workloads and support complex and large-scale use cases as opposed to the "mom and pop shop" that constitutes most of the IT industry.

I am also always surprised to find out that many architects would go the most DIY route with technology choice/deployment view for each of these elements of the stack. It would be understandable in some highly-constrained scenarios, but in most pretty relaxed contexts (no business constraints on platform, infrastructure and tools) it is often counter-productive to DIY. This could stem from the psychological barrier I mentioned under "Simplicity", but is in no case justified.

The issue here is usually <u>the wrong prioritization of ASRs and requirements in general</u>, spending most of your time and effort on the least valuable aspects of your solution.

In keeping with the "start simple" mantra, always look for solutions that implement the desired behavior before you go full speed into hacker mode. I'd rather someone bring me a personalized Wordpress website that fulfills the requirements than make a React app to do the same thing, when I never asked for that level of flexibility and it's not even coming in the future.

Yes, yes. Many voices out there are telling you this, and I will add one more: don't overbuild, don't build for QARs you don't have but your "developer spidy sense" tells you you need them.

This isn't a warrant to get sloppy, this is rather a warning against writing a library nobody will ever use on your (or your employer's) dime. It's a great development exercise, it's fun, challenging, and interesting, but in most cases unnecessary unless the mission statement was *explicitly* to build a library with actual existing dev teams that are waiting to use it. Otherwise it's stylish but unnecessary.

The above covers the personnel cost element, but this also applies to "not using a nuke to kill a fly", i.e. using reasonable architectural components (systems, services or sub-systems) in a justified and dare I say "minimalist" manner. The wrong technology choice in this respect results not only in high maintenance overheads, but also in high running costs and very costly scalability.

TO summarize, don't do "stylish but unnecessary". Success in Software Architecture is delivering necessary ASRs reliably.

# Dev Team Match

![](/assets/img/HiddenASRs/right_tool.png)

All things being equal, I would strongly recommend adopting stacks that work with your team's skillset than making small performance/any other ASR gains by pushing a new stack on them.

The highest cost component for a software project is personnel cost, widely accepted to be at least 40%-50% of the total project cost (as compared to infrastructure and equipment, software and licensing, and project-related costs such as training and travel). That means that the sooner you get to your highest productivity with a team the more cost effective. The shortest path here is to hire the right team to implement the right architecture, or design for the team you have in a more constrained environment.

Having your team work with a technology they're not familiar with is a high-risk venture, you can certainly expect more defects, slower progress, delays and overall lower quality work despite best effort.

Of course this has its limitations, so don't be shy to push back when asked to develop highly-constrained embedded software with a team of data scientists who have HPC clusters at their disposal all day every day and have no idea about low-level coding. But that's exactly the point: don't pick the wrong team for your project, and conversely don't design the wrong solution for your team (if you have no other choice).


# Conclusion

These three ASRs, you would have noticed, revolve all around the same topic: don't overdesign, don't overengineer, and don't overstretch what's feasible or necessary. If you stick to these recommendations, there's a good chance you will be able to build a solid architecture that is open to grow and evolve, without spectacularly crashing and burning.