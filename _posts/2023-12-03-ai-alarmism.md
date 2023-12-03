---
layout: post
title: 'AI alarmism and why it's wrong'
tags: [software_engineering]
cover-img: "/assets/img/SE_header.jpeg"
---
As our product offering with Troutwood neared completion and full-scale is becoming on the horizon, one of the biggest topics that takes center stage on my desk as the CTO is information security: can someone access data they're not authorized to? Can someone tamper with data? Can someone deliberately (or not) cause catastrophic failures to our systems and apps?
So I have been doing a deep dive in the topic, all while following the accelerating AI developments and conversation around them.
One recurrent theme has been AI safety, namely: will an AI go rogue and "maximize paper clips"? Will a "panic-attack-inducing" "Roko's Basilisk" implement the Abrahamic religions' version of hell through a Matrix scenario?

Every day I see opinions and speculations piled on, starting from Elon Musk's sensational doomsday declarations on the dangers of AI to the signed letter requesting a slow down of AI development to the many many voices in the industry putting an inevitable doomsday 5 years, 10 years and even 1 year in the future. Most prominent speculations however don't even begin to tackle this rationally or factually.

What I noticed in those speculations is a mystical approach to AI that completely forgets all of its reality, a program running on a computer somewhere, extrapolating what it can and can not do, sometimes ingoring that outright and assuming that by some magic the AI can bypass the laws of physics and the reality of computer systems limitations and interfaces.

I tried to reflect on the topic and boil it down to its most basic components: how would an AI ever gain enough power to become a threat?
1. Let's assume the worst case scenario: that the AI misinterprets a good goal and diverges into destructive maximization of that goal, or conversely that it is given a malicious goal that it sets out to meticulously and optimally execute.
2. Let's also be generous and assume the AI has infinite memory, as in: like a human being, from the moment it's given that goal, it can keep a short term and a long term memory that serve to have it "thinking" and reacting live to changes in context and random inputs and developments. This what AI researchers call the "planning" capability.

It's clear then that the last step to world destruction would be for the AI to act on its goal and the plans it laid out to execute it. And in here lies in my opinion what should be the core of the matter: the issue is not a matter of AI intentions, it's mainly a matter of IT security.

An AI seeking to enact any sort of change in the world, beyond the confines of its memory, disk and processor access would have to:
1) Trick a human into doing its bidding via social engineering
2) Use its internet interface to gather resources, deploy scams, get people on Fiverr or other services to perform tasks for it
3) Take over networks, build and propagate malware that allows it to control networks and devices all over the world and eventually either cause a lot of damage or leverage


1) IT security is still our best defense: limit access, limit authorized actions. Caveat: vulnerabilities
2) AI is still the answer: leverage "dumber" AI agents to execute while the "big brain" plans and another "big brain" checks for potential risks and stands in as a cop
3) bureaucracy is a defense mechanism. Large scale acts of destruction inevitably hit a wall of access to levers of power that are strictly controlled. If an AI were to want to declare a business and act through it, it can't. Caveat: systems fail
4) prioritize real risks: cyber-physical systems

AN AI CANNOT DO WHAT WE DON'T ALLOW IT TO DO
We: humanity must unite, a code of ethics must be created, a code of labeling AI actions is necessary
Allow: there must be a standard for controlling AI-labeled actions. A ubiquitous standard stating levels of access and authorized actions for each level of access for an AI would be useful. If an AI of level 3 it's allowed access within a network with cyber-physical devices, it must not do X, Y or Z, if 