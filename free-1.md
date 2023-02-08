# Free project 1

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

I work in a physics research lab that studies how colloidal crystals change over time, where I do simulations work. I'm the only one in the lab currently that comes from a CS-heavy background, and our simulation code base has a steep learning curve (due to how many have worked on it over time). A DSL that covers a subset of the sim code base would strike at the heart of what makes these simulations useful while making it a much easier tool for other researchers to use in the future. I would be helping current labmates as well as those in the future who want to do simulations. Typical members of our lab aren't too familiar with using the simulations, but after this DSL they should be much more familiar with it, and will hopefully have enough confidence to give the full code base a look!

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate here because it makes the simulations accessible to a wider audience of Mudders who don't have as much experience in coding. As previously mentioned, the existing code base is dense and expansive, and if it were easier to use more students could use it to study our systems instead of experimental work (which takes a lot of time and skill and the needed materials are pretty expensive).

### Why you?

_What excites you about this idea? How did you come up with it?_

As this is my last semester in the lab, I'd love to do something that caps off my time working there. Additionally, I've been thinking about our code base a lot recently, as I'm in the process of teaching other students in the lab how it works. I could see a language like this being useful not just for those students, but for prospective labmates who want to get a sense of what our work entails!


### Domain

_Describe the project's domain in five words._

Simulating disorder in colloidal crystals!

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

One could either write out commands in a script or use the language on the command line. There would be set commands for setting an appropriate crystal lattice for particles to lie on initially (LATTICE), for running the simulation (RUN), for visualizing the simulation data (SHOW) and for exporting the data (EXPORT). I think this would be the right way to interact with the DSL because it focuses in on the core parts of the simulation, while not being too involved nor too brief.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, it will execute all the functions in the script in the order you wrote them. In terms of user interaction, you could either choose to view the simulation result frame-by-frame in real time or just let it run in the background without a visualization. Some errors that could occur include invalid saving names and running out of system resources. The error messages from the host language might be useful enough, but if need be I can edit them to be more clear.  

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be simple to do all of the typical things that our simulations currently do - generating starting particle positions, running sims, visualizing the results, and so on. It should also be easy to save your simulations results as a set of points that can be moved into other languages to be processed further. I would also like to make it possible but difficult to expand this language, in the vein of Steele's advice that languages should be designed within a 'pattern' to allow for further expansion if desired. It should also be possible but difficult to wrap the DSL in a GUI environment that makes it even easier to use.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

The only example that I could find is called MDL from [a conference paper from 2007](https://www.researchgate.net/publication/220696642_MDL_A_Domain-Specific_Language_for_Molecular_Dynamics). I liked how this language had lots of different options for the simulation types you could run, along with structuring the simulation parts into a few distinct parts similarly to in my syntax section (physical(),
approximations(), output(), and execute()). For addressing the need of a DSL for general-purpose particle simulations, I think it does a good job. However, I wouldn't mind seeing the syntax simplified further. You would need to have some familiarity with C/C++ to use that language, when I think that is a bad fit for some researchers.

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think that I would spend about 35% of my time on "language" and 65% of my time on "systems".

### Scope

_How big an idea is this? How ambitious is this project?_

I think that this idea would be fairly ambitious. There's a lot of underlying code that supports the simulation workflow - code that generates particle positions, that actually runs the simulations, that visualizes the results, and that saves the results appropriately, to name a few examples. But because I have a lot of experience writing code within this domain, I can leverage some of my existing code as templates for the functionality, so with the reduced planning on that front the workload should level out to be something more manageable.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This would be a good idea for my project because it would be focused on a domain where I have a lot of experience. It would also be a useful tool for those to get a better understanding of the work that our lab does. It might not be a good project because the scope is rather narrowly focused on what our group needs instead of a more general molecular dynamics DSL. 