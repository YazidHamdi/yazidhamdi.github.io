---
layout: post
title: '8 Annoying Bugs of Software Architecture'
tags: [software_engineering]
cover-img: "/assets/img/SoftwareArchitectureBugs/group-gpt.png"
---
For some reason I remembered the [Dangerous Animals of Product Management](https://www.productboard.com/blog/dangerous-animals-product-management-infographic/) today and kept wondering what a similar concept would look like for software architecture/architects. That prompted a whole sequence of memories from my previous roles, where I had to deal with multiple, sometimes great, sometimes annoying software architects. Going with the annoying theme, I turned it from animals to bugs, the champions of annoyance.

With the help of ChatGPT (I don't know much about bugs to be honest, real insects that is) I came up with 8 personas illustrating things I observed in the industry, and even generated some illustrations for them with ~~Bing Image Creator (a better Dall-E)~~ ChatGPT's new fancy image generation capabilities (2025 update).

![](/assets/img/SoftwareArchitectureBugs/group-gpt.png)

If the tone didn't already make this clear, this is a satirical post aiming to poke fun at stereotypical characteristics of software architects, of many of which I am personally guilty! Have fun and don't take it too seriously 😁

So here goes:

---

# 1. The Stubborn Mosquito
"Use my favorite stack... zzzz... use my favorite stack... zzz..."

![](/assets/img/SoftwareArchitectureBugs/mosquito-gpt.png)

I'm sure you know exactly what I'm talking about, the silver-bullet architect, the one who has a plugin/package/module/service of his stack for every purpose for which another better more-fitting less-obscure stack exists. This architect starts with the solution and works back into the design and requirements, which is, annoying, and not good.

# 2. The Bulldozing Beetle
aka. "jet-propelled Joey"

![](/assets/img/SoftwareArchitectureBugs/beetle-gpt.png)

Clients love him (or his promises of quick delivery), developers don't like him (and his recurrent "this is trivial, just use X" statements) and his inevitable changes of heart. Essentially an architect who likes to think he gets it right the first time, overcommits, pushes forward, only to discover issues and bulldoze an overcomplicated design to start a new one.

# 3. The Lurking Tick
"it'll work, trust me". "But what if?" - "no, I said it'll work, just trust me"

![](/assets/img/SoftwareArchitectureBugs/tick-gpt.png)

This architect embeds himself deep in the project by deferring all decisions to himself (because of I'm an architect dontcha know) and becoming a constant wall of feedback rejection against which business, dev and clients hit their heads. Like a tick, he refuses to move, and sticks to his position no matter how much resistance is applied.

# 4. The Micromanaging Ant
"okay how about when the user clicks button X and the popup has to be displayed?" - "buddy you're an architect, let the frontend dev handle that"

![](/assets/img/SoftwareArchitectureBugs/ant-gpt.png)

This architect is a developer's worst nightmare, one who intervenes in every single detail even the ones that have nothing to do with system attributes or architectural decisions. Everything affects performance, everything breaks scalability, that little frontend enum needs to be just right, those for loops need to be while loops, otherwise it doesn't work for his majesty.

# 5. The Flighty Butterfly 
aka. "will he won't he Willy"

![](/assets/img/SoftwareArchitectureBugs/butterfly-gpt.png)

This architect is puzzled, hesitant, decides something today, changes it tomorrow. Whether or not it's his fault is unclear, maybe an "Agile" boss is making him do that, maybe he's just a perfectionist too lazy to actually sit down, write all his thoughts down, then decide, instead of letting his lunch or drive home inspire the next change.

# 6. The Shortsighted Moth
"let's use Vue", "what for?" - "nah don't worry it's the most popular thing now"

![](/assets/img/SoftwareArchitectureBugs/moth-gpt.png)

This architect should probably not even be called that, since he basically just forces the latest (that he saw that morning on Hacker News or Dev.to) and greatest (well...) on every problem he encounters, don't even worry about "why", that's not how this works. He's best friends with the Bulldozing Beetle, and the sworn enemy of our next bug.

# 7. The Eternal Cockroach
"so the client wants us to update balance sheets to reflect transactions in real time" - "I've got a COBOL program for that, hang on let me find it" \*blows dust off an old IBM mainframe\*

![](/assets/img/SoftwareArchitectureBugs/cockroach-gpt.png)

As his name indicates, this architect survived every wave of technology without learning anything new, he hangs to old technology with all his strength and won't let go. In the best case scenario, he can write you a Pong Game from scratch using Pascal, in the worst case scenario, he just does a lot of lecturing and no coding in a cosy enterprise job he can't be fired from just for the sheer amount of severance the company would have to pay.

# 8. The Isolating Spider
\*knits for 6 months without sending an Email\* "heyyyy I thought I was supposed to be working on that, look at this full solution I made single-handedly in my corner"

![](/assets/img/SoftwareArchitectureBugs/spider-gpt.png)

The spider knits and knits, makes a wonderful web of services, artifacts, modules and runtimes, components and \*insert jargon here\*... And talks to nobody about it, in total isolation. The team either anxiously wait for a miracle (that may or may not happen), or moves on and just puts something together hastily to make the deadline.
You could also say that he chemically juices the insides of the company and slowly drinks them just like a spider.

---

Alright so there we go. Send in an Email chain you Eternal Cockroach! Tag a friend and let's see some sparks in the comments you Shortsighted Moth!