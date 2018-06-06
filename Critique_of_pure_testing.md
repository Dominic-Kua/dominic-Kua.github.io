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

### Contact me
If you want to talk  to me about this, you can reach me here on Github or on Twitter @Testing_crafty

### Recruitment: 
Looking for a job in Cambridge (UK)?
I’m currently hiring for a second to help me steer and lead testing efforts at Geospock. The product is geospatial and temporal databases on a massive scale with attendant analytics and visualisation platforms. The testing problems are non-trivial, but interesting and engaging. Much of the testing is done by the developers, with the test role being more helping developers decide what to test and implementing frameworks and infrastructure to help the developers test. The test areas range from database testing, API testing, web testing to infrastructure testing and testing the limits of systems at massive scale.

We’re expanding this year as customers increase and the likelihood is that any new tester on my team would be mainly involved in helping create testing strategies and automation for customer deployments. Office culture is generally relaxed and fun, and we’re improving our facilities as we grow (new kitchen, games room, coffee machine coming shortly). We also have a good pension, dental, health and work from home is not unusual. Variable height desks for all and Mac or Linux as standard (Mac is more useful for a tester as we _do_ need to test against Safari). Languages we use are Java, Kotlin, Python3, Javascript, Ruby,  Scala, Erlang. You do not need to know all of these. Familiarity with and a modicum of experience in any scripting language would be great, anything beyond is a bonus. 

It’s cloud based mainly, so think AWS, Azure, Google Cloud etc. again you don’t need to be an expert in any of these, I’d never used them when I arrived. Familiarity and comfort with a Unix shell of some flavour would be a definite advantage as SSHing into a cloud machine to pull syslogs or tweak a set up is quite common.

If this rambling set of words hasn’t put you off you can read the official spec [here](https://geospock.com/jobs/software-test-engineer/)
