# Technical tips every tester should know

Firstly a word about this blog, its inception and its purpose.

I'm not good at blogging. I've tried it over and over and I've never managed to keep it going for more than a year or 
so. So I had the bright idea of using peer pressure to make me blog more often and so the bloggers club was born. Every 
couple of weeks I'll rely on other people to think of ideas for me to blog about and pressure me to publish. I'm 
basically using tribal instincts as a hack to overcome my laziness, hurrah. 

The topic this week is a technical tip every tester should know. 


Now this is pretty hard because so many technical tips won't be portable. If I throw out Bash tips, windows users will 
be left without something helpful. If I reveal secret web testing techniques then there will be embedded testers 
without something to use and so on. As such I've got to make a choice: Do I write something very general which might 
help many people, or something very specific which helps a smaller subset of people but will actually be useful?

I'm going to cheat. I'll do one sort of general one, and one much more precise one. Hah! Who writes the rules now? 
(It's you Dominic, it was always you and who are you talking to?)

So, on to the tips!

General technical tip: 

Where possible start the system under test from a command line you can read the output from, you'll be amazed at how 
many errors, warnings and other such goodies are thrown into the stdout for programs which are not normally meant to be 
started from the command line. For much of this I'll be using Firefox as my example, because it's open source and well 
documented. Here you can see what's output to the terminal when I run Firefox from the terminal. Now most of these 
errors are not worth bothering about, right until the time when they are and you see the one error which gives you the 
information you need to pinpoint the bug you've been chasing. 

![Firefox showing the silent errors](tech_tip_pic1.png)

On most systems this is actually fairly easy as installed applications get added to the Path or are installed in a 
location which is already on the Path, Macs are the exception but you can normally find the path to the binary in 
`/Applications` if you've installed it though a dmg.

What will surprise you, possibly, is to learn that many applications have command line options which are completely 
hidden from normal GUI, for example, Firefox can be loaded with different locales specified to normal, which as a 
tester can be incredibly useful. Make a habit of acquainting yourself with the various options of the applications you 
use most often and it'll pay you back in spades. 


Specific technical tip:

If you use a Bash terminal at all, you should look into learning the history expansion commands. 
A Bash terminal is the default command line on most common Linuxes and OSX. There's a raft of "shortcuts"
in Bash that let you do all manner of things by combining an exclamation mark with another character.

We'll start with the extremely excited `!!`. This is immensely useful as it runs the previous command again. Now some of
you might be thinking "But I can just hit up and then enter for that" and you can. But `!!` is much more than that. it
inserts the previous commmand at the point in the new line where you put the double exclamation mark. 

For example:

![The power of !!](tech_tip_pic2.png)

Bonus tip here, you'll notice I've wrapped the double exclamation mark in back ticks. This inserts the output of the 
enclosed command into the command you're writing. So rather than typing commands, getting the output and then copying 
and pasting, you can embed it directly in your command. Beware though, this could lead to all manner of unintended side 
effects! Be sure you know pretty well what it is that you'll get out of a command before encapsulating it!

Next up is the `!$` command, which inserts the last _argument_ from the previous command, great if you want to do 
multiple operations on a single file, like so:
![Create, fill, rename, but only type the file name once!](tech_tip_pic3.png)

Finally, if you ever find yourself filling in the same command over and over and `ctrl+r` and searching is too slow, 
you can always just use `!<start of command>` to fill in the command again. 

Enjoy the commmand line!

If you want to talk  to me about this, you can reach me here on Github or on Twitter @Testing_crafty


### Recruitment: 
Looking for a job in Cambridge (UK)?
I’m currently hiring for a second to help me steer and lead testing efforts at Geospock. The product is geospatial and temporal databases on a massive scale with attendant analytics and visualisation platforms. The testing problems are non-trivial, but interesting and engaging. Much of the testing is done by the developers, with the test role being more helping developers decide what to test and implementing frameworks and infrastructure to help the developers test. The test areas range from database testing, API testing, web testing to infrastructure testing and testing the limits of systems at massive scale.

We’re expanding this year as customers increase and the likelihood is that any new tester on my team would be mainly involved in helping create testing strategies and automation for customer deployments. Office culture is generally relaxed and fun, and we’re improving our facilities as we grow (new kitchen, games room, coffee machine coming shortly). We also have a good pension, dental, health and work from home is not unusual. Variable height desks for all and Mac or Linux as standard (Mac is more useful for a tester as we _do_ need to test against Safari). Languages we use are Java, Kotlin, Python3, Javascript, Ruby,  Scala, Erlang. You do not need to know all of these. Familiarity with and a modicum of experience in any scripting language would be great, anything beyond is a bonus. 

It’s cloud based mainly, so think AWS, Azure, Google Cloud etc. again you don’t need to be an expert in any of these, I’d never used them when I arrived. Familiarity and comfort with a Unix shell of some flavour would be a definite advantage as SSHing into a cloud machine to pull syslogs or tweak a set up is quite common.

If this rambling set of words hasn’t put you off you can read the official spec [here](https://geospock.com/jobs/software-test-engineer/)