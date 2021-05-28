# The Naming Project

Hello. The only thing you need to know about me is that I am a very old, very lazy, and very grumpy engineer who has set out on one simple mission.

> To solve naming things in computer science once and for all.  

# The Naming Problem                                                                                                                                                                                                                                
In my long career of working in computer science I have had to solve many problems that have impacted the global tech industry. However -- there has been one very simple problem that has remained in every computer science conversation I have **ever** had. 

> What do we name _this_?

# The Goal 

The goal of the project is to offer a set of tools and utilities that do 1 simple thing:

 > Create a set of deterministic tools that given the same input, will always yield a unique name given a set of constraints. 

# The Code

Introducing `libdname` which does one simple thing. 

Given an arbitrary input, a human pronouncable deterministic name will be produced.

The internal library is effectively just a bijective sha256 implementation with a library of pronouncable words. The implementation against various domains in computer science is where `libdname` will truly shine.

Given a mac address -> you get a name.
Given a kernel config -> you get a name.
Given a volume ID -> you get a name.
Given a docker image -> you get a name. 
Given a sha of a code base -> you get a name.

By identifying a static (unchanging) component of your system - you can now generate a unique name at runtime.


# The Hashing Mechanisms 

Given an input, we will need to do two things to produce a name. 

 1. Generate a unique hash (we are starting the project with [sha-256](https://en.wikipedia.org/wiki/SHA-2) for obvious reasons.
 2. Generate a unique name from the unique hash mentioned above. 

# The Constraints 

 - All names must be composed of `UTF-8` unicode characters
 - All names must be determinstic based on input. 
