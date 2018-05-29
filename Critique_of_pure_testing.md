# A critique of pure testing

It's a commonly held idea that testers are always the best people to do testing or to lead testing efforts. I'd like to 
offer a rebuttal to this, testers are not always the best person to test or lead testing and in some cases could miss
 important things due to a lack of knowledge. 
 
Now let me clarify this, I'm not saying you can do better testing without a tester in the mix. I'm not saying that 
testers shouldn't test. What I'm saying is that there are features, bug fixes and designs that should be tested, or the
testing effort led by a domain expert.  

As testers, we often tend to the generalist and shy away from the specifics. This is normally an asset, we've got enough
 knowledge to test across the breadth of the application or the depth of the stack. However there are times when a 
deep knowledge of the area under test is needed. Perhaps you're about to release a new proprietary data format, or you're
testing something where a deep statistical significance is needed. Perhaps you've got a new algorithm needing a 
performance test and you need to have inputs and environments to actually check it beyond simple big O complexity?

This is where a domain expert is handy. Sometimes this is the person who wrote the feature, and despite the long standing
mantra that you shouldn't let the author test the feature, they can certainly lead the testing. You, as a tester might
have an idea about the surface layer of any of these problems, but a domain expert might know things that you couldn't
think of, like timing attacks, or the difference in how code is executed on different CPUs or browsers. 

Of course sometimes a tester isn't the right person to test because of the opposite problem, they have simply too much 
knowledge to effectively test as a user would. This isn't a simple case of remembering to not use shortcuts, but can 
be much deeper, I had an issue last year where I was discounting a slow load time, because I understood the shape of 
the network traffic, so I accepted a 2-3 second long load time when I really shouldn't. Luckily, or rather by design, 
I had passed some of the testing to our pre-sales and product management who didn't have the knowledge I did. They
correctly pulled us up on the slow loads and we changed how we accessed our back end resources, leading to a less 
complete early load, but a much better user experience.

Testers are often the best for leading and running tests, but not always. Be prepared to take a step back and let 
someone else drive when it makes more sense for that to happen. But don't feel that you can't ask questions or give
suggestions. We're employed to help testing, but not necessarily to do everything!