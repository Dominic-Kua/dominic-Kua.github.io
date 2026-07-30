# AI on the edge

## Why not just use the app?

Everyone, their grandmother and their friend's dogwalker's web designer is using an LLM every day in one form or another. Sometimes it's intentional, but quite often it's not. It's the AI summary in a web page, it's a chatbot on a website to help you return some goods, or set up a new account. 

But all these LLMs need to run somewhere. Most of them live in great big data centres in on rack upon rack of machines who have made upgrading a simple gaming computer nigh on impossible for anyone of normal means in 2026. That means nearly every time you interact with them, your information, your data is leaving your machine and heading into the cloud. 

Normally we'd think this is fine, we do it every time we make a search, but then things like [this](https://www.bbc.co.uk/news/articles/cly5qgjk5ywo) happen and suddenly we remember what data sovereignty is and why we need it. 

But wait, I hear you cry, how does this affect me? I'm still going to _have_ to use those chatbots, those search results and everything. Yep, but you don't have to use cloud models all the time for everything. 

Now, I've worked in software for well over a decade now, closing in on two, and I know first-hand what a gamechanger the LLMs have been in the last year. And let me tell you, the moment I got my grubby little mitts on a claude subscription, I immediately thought "Why can't I do this locally?"

For you see, I am an ancient beast, and I remember the days when everything was local. Like a captive elephant, I remember the wild freedom of my youth. Sure I enjoy not needing to host a server for everything, but there's just something satisfying about having something running completely locally. In fact I took this to an extreme and had my macbook running a local LLM hooked into claude code while I was on a flight this year. Completely offline, but still producing code. It made me feel smug. I'm here to let you know that you can feel smug too. I can teach you how.


## So, how can I feel smug then?

Let me preface this by saying, I've only really set all this up on a mac with Apple silicon. Technically it should all work on any OS/architecture, but I haven't tested it and Apple silicon brings unified memory, which is a massive boon for this. Instead of needing a 16GB graphics card, I can just use my 16GB M1 pro macbook pro. So while I'm anything but an Apple shill, they're materially better in this case.

Firstly you need to look at what you're working with, what you want to do, and how you want to do it. The market for local LLM solutions has exploded, because there's nothing quite like having a $20 subscription change to a $6000 bill (thanks, Github for subsidising me!) to really get the creative juices flowing. 