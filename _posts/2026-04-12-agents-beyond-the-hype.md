---
layout: post
title: 'Agents Beyond the Hype: Architecting Autonomy'
tags: [software_engineering]
cover-img: "/assets/img/SE_header.png"
---
Generative AI (doesn't that term feel like such an antiquated one now?) and LLM-powered agents feel as big a technological leap as the internet was for humanity, and for good reasons. Finally, the dream of artificial intelligence is materializing. You no longer need to train your own model to solve your specific problem, we now have for the past 4 years general-purpose AI which is multi-modal, capable of reasoning and using tools.

"As big as the internet was", of course, comes with the same level of risks, and the biggest of them all is: being misunderstood for a silver bullet for a business's (and more generally huamnity's) problems. Rumbling under the torrential flood of agentic fully-autonomous magic-like hype declarations, demos and releases is a an undercurrent of failures, wake up calls and reality checks that most are not really ready/willing to look at yet, since we haven't milked this hype enough yet.

First let's agree on what we're talking about here: when a tech CEO is talking about agents today, they're most likely talking about a fully autonomous agent that needs nothing but an instruction and some integrations to get you a "done job". When a software engineer is talking about a coding agent, they're most likely referring to Claude Code, OpenAI Codex or Google Gemini CLI. Regular people? They think ChatGPT is an agent. Hah.

You will see the definition of an agent require:
- At level 1: tool use (calling APIs, essentially)
- At level 2: chain-of-thought (aka sequential planning and execution)
- At level 3: autonomous agency (asynchronous execution, self-correction, state persistence aka "memory")

So do "interactive" or "semi-automated" agents qualify for what most would call "agent" (as opposed to a classic chatbot or a coding assistant)? I don't think so, I have seen the definition shift with time and right now most people I talk to define it as this idea of an enabled AI that "is living and breathing" and "figures it out and does it itself" - implying the idea of autonomy and memory as the end goal.

That will be my definition for "agent" going forward in this post.

Why is it then that whenever we get a demo of an agentic framework someone inevitably shows us an LLM "summarizing their agenda for the day" (I swear I must have seen this one a dozen times from different providers)? Isn't it a bit telling that the pitch comes down to "We've replaced 15 seconds of cognitive effort with 45 seconds of LLM latency and a $0.12 API bill"? Why does this feel so much like [the Mechanical Turk](https://en.wikipedia.org/wiki/Mechanical_Turk)?

# The false promise

In a nutshell, *1)easy 2)unbiquitous automation* is what's being promised here. Sure it can summarize your calendar, but it can do much more if you want it to. Literally everything possible for you to do with a computer today. No really, that's really what these things ~~could~~ *can* do.

## Easy Automation

"As an agent user, I would like my agent to do my chores, so that I can go for a walk and be happy". Implement this one, Claude.
This is the weight of the expectations here: It is in principle possible, but I have and everyone here has been provided access to the Zapiers and the Microsoft Power Automate and we found it such a chore to literally go and figure out the formalism and draw a workflow then input variables and link systems and services, who wants to do *that*? Can't I just tell it what to do?

Well - you can now, it can understand what you want (or a version of it), and if you connect it enough, your agent can also do it for you. But how much "telling it what you want" are you ready to do?
<the more you tell it what you want the more annoyed you are but the more informed it is>
How reliably will it understand what you want?
<the more you give it instructions the more confused it may get>

So for now we're stuck with glorified workflow management software with an "LLM" step as a nice new addition (instead of say coding a custom processing step), so basically classic BPM/workflow management and automation with "easy to make" NLP steps baked in.

We don't have "an agent that makes agents" yet. Sure we do have it, you must have heard of "subagents", but these are not it.

## Ubiquitous Automation

Connect your calendar, connect your Hubspot, your Salesforce, your SAP, your bank API, your robot vacuum cleaner app, your coding assistant, everything you can connect (and the list is rapidly growing) and you will have ubiquitous agency. It makes all the sense in the world, and yet it doesn't: you mean hand over all my keys to an agent run by some business somewhere and just trust them with my life? No I'll host my own. Oh wait, what do you mean it can accidentally delete everything and has done it in multiple highly publicized instances? Ok I will restrict it from certain types of operations. But then it won't be able to do things for me.

# The reality

By all measures, and beyond simply headlines and sales pitches, agents are here, and here to stay and become the new default.

Is it working? Are we getting easy ubiquitous automation? When it works, why? In which cases? When does it not work? - Same as digitalization, botched planning and rushed execution.
The token tax and why it's ok: it'll eventually get cheaper.

3) The comfortable yet risky "connect everything you have": when did it ever become ok to hand over your whole digital life and levers to a business you don't run and nobody is asking what it's doing with them?

4) Is there a path forward? Yes: adapting our architectural thinking and retooling our stacks.
a) agentic authN/authZ tools: gateways protecting critical resources and actions with "ask a human"
b) alignment: still not there, but reasonably possible via adversarial prompting/validation steps of LLM on LLM
c) get back to architectural basics: ask the what before the how, something too many people seem to be forgetting.
d) roadmap for learning and getting to building: a suggested path (daily drive coding assistants, start creating some jobs on a sandboxed environment like Dify or OpenClaw etc., follow the tooling releases and grow into real proven usecases - still do not give un"policy proxied" access)

5) On a forward-looking angle: I don't think LLMs are "it". I think Yann LeCun's new initiative is "it". Looking into more fundamentally sound approaches instead of predicting the next character bigger and faster is what will take us to the next level. And of course quantum, but that's quite a distance away.