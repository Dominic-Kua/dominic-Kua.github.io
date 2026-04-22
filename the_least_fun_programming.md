# Progamming isn't fun any more

	I've been programming since I started with BASIC in the 1980s and I've enjoyed it deeply for forty years. I've learnt BASIC, TurboBASIC, Java, Python, z80 assembler one summer... And I've generally enjoyed it deeply.
This year I really encoutered a new way to write software,spec driven development. As everyone knows by now, llms have been getting much, much better at writing code over the last few years. At first, in say 2024, they were
mocked as being spicy autocomplete, not unfairly. Then a new wave of models came out in 2025 and people looked at them and saw them as about the same as a very enthusiastic junior developer. Doesn't always get it right,
but if you give it a very well defined, non-novel problem and let it loose, it generally came back with something that worked. Often it was either lacking in safeguards, or overly complex, but it did work and it passed
tests. 

Then in November of 2025, there was a step change in the power of the models. Suddenly you could give a model a fairly complex problem and it would solve it generally very reliably. A solid mid-senior level engineer now. 
That was when people started really looking at one engineeer dev teams, where a fleet of agentic LLMs would write the codebase and so , Spec driven development took its first steps in the broader engineering word. 
Frameworks such as BMAD, Spec-kit and OpenSpec started to appear, and with the new models they could turn tokens into products very quickly. 

Around this time I changed jobs, to a company that was going all in on AI. I was a bit hesitant, I hadn't seen the latest developments, and for me, AI was still at the spicy autocomplete/vibe coding stage. I was,
however, willing to learn. So I did a quick side project, cloning 2048 to run on my local network, hosted on a raspberry pi. I used Spec-Kit and it took me about an hour to get something that did, mostly, what
I wanted it to. It wasn't perfect, so I did another hour of prompting and got... soemthing that worked, even on mobile with touch controls. 

I was deeply impressed. I'd specified the tech stack (react front end, python back end), given it a descript as vague as I could. I literally told it to make a 2048 game and it knew what that was. I told it I wanted
a cosy cottagecore pallette for the colours and it delivered. In a couple of hours I'd produced something that would probably not have taken me more than a day to make, but it had been nearly all background tasks. 
That's the seductive part of SDD and agentic coding, you put in a few hours up front, but then you can just kick it off and let it do things in the background. You don't even need to read the code for little side projects.

But here's the kicker, you absolutely need to read the code for anything important. Because what agents and frameworks give you is a _very fast way to create technical debt_.