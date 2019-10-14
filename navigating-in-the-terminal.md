# Navigation in the terminal 

The command line is quite intimidating at first. It's a prompt with no hints as to what you can 
do in it or how to work it.

By default most terminals will open in your _home directory_. Now if you don't know what
a home directory is, it's normally named the same as your account and is in `/home` on Linux,`/Users` on mac and 
`C:\Users` on Windows. 

So now you're there, what do you do? 

Well if you're anything like the majority of us you use directories to organise your files, they're sometimes
called folders, but the meaning is the same. They're the hierarchical organisers of your filesystem. 

So let's start with the basics. The big three consumer desktops have a `Documents` folder in them so let's start with
getting there. On Linux open the application opening menu and type `terminal`, on macos do the same thing but 
in Spotlight. On Windows you'll need to install the Windows Subsystem for Linux (TODO: insert instructions
 here.) Once you've brought your terminal up you should be looking at something like <screenshot here> 
 
So let's go into the Documents directory, time to use the Change Directory command, or cd.
 Type `cd Documents` and hit enter. Most terminals will reflect the
updated path in the prompt, but you might not see it if you're in a pure Bash shell. If you ever want to know 
where in the file system you are, you can use the `pwd` command, this outputs the present working directory
to the terminal's "Standard output". What you can see there, probably something like `/home/dom/`

A brief aside on the terminal's outputs. There's two major ones, standard output (1) and standard error (2).
The reason I've numbered them there is that you can actually redirect these outputs to files or file like objects.

This can be very handy if you want to only put the errors into a file, and not see them in the terminal. 

But back to `cd`, this command has hidden depths, you can actually cd to a regular expression*, your previous 
directory, your home directory, all with shortcuts. So, let's look at that. Hit `cd` and you should end up back
in your home directory. Now let's get back into Documents with `cd *ments` which as you can see is taking 
anything before `ments` and then passing it to cd. You can use the bash shortcut to home `~/` as part of a 
directory's path too. This leads to chimaera commands where you can be in `/home/dom/Documents` and want to 
go to, say a log directory for today that you know ends in `2019-10-10/` so you can `cd ~/logs/*2019-10-10`.
Now to go back to the previous directory? Just `cd -`. 

`cd` is a basic command and you can use it naïvely to just change directory, but it has history, relative paths, regular
expression powers and can be much more powerful than it appears at first!



*Regular expressions or "regex" are patterns of strings and symbols which match to patterns in text.