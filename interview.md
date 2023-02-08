# Interview project

## Interview questions

* Tell me how you use computers in your teaching.
* Does anything stand out as deficient?
* What do your students best respond to when using computing?


## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

For my interview, I chatted with my mom, who teaches middle-school math. I thought her perspective on computing in the classroom would be interesting for building a DSL. During the call, she described how frustrating it is how students just jump to the correct answer instead of going through all the work required to reach that answer. She also noted how students can get tempted to do other things while working on the Internet. In my view, we could take both of these priorities and build a DSL that makes sure students follow the right steps for solving math problems while minimizing digital distractions. 

The need is that many students focus solely on what the right answer rather than following the steps that are needed to get there. I think that a DSL that has students go through all the steps of a set of inputted problems would help them practice the work it takes to get to the right answer. In this DSL, you could input a problem in plain English (ex. 7+5), and the language could parse this input, determine the proper steps to get to the right answer, and then have the user complete these steps. The students and teachers likely have very little experience in CS, so the language will need to be as simple to use as possible. In terms of math experience, the students' level of understanding for the proper steps varies, but hopefully they will all walk away with a better understanding of how they should show their work!

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL would be appropriate here because teachers already have a lot going on, so a simpler learning curve means that more teachers would actually have the time to figure it out and use it. It addresses the need by giving students an interactive mathematics tool while being automatically-generated to reduce the workload for teachers.

### Why you?

_What excites you about this idea? How did you come up with it?_

I think that parsing a given math problem (within a fixed set of templates like multiplying, factoring, etc) on a conceptual level would be an interesting programming challenge. You'd have to do your research to find the best way to tackle something like any given multiplication, then you need to encode that logic and have the language follow the proper steps and wait for user input. This idea arose pretty naturally from the interview I did.

### Domain

_Describe the project's domain in five words._

Working through simple math problems!

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

The user would have a set of functions that they could script within a file. The core function could be QUESTION, and it could take a problem keyword followed by the math itself. For example, QUESTION("add 7+21") or QUESTION("factor x^2+4x+8). This would be a good way for the DSL to operate because it is very intuitive, and the language would just have to be robust enough to parse and interpret that input.

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When the program runs, it would run in a terminal window, waiting for student input. It would need to function such that the student could only advance once they had finished each step of a given problem. It would be really cool if the program could bring up certain visual elements like graphs if needed. I would also like it to provide hints for the user if they get stuck on a certain step. 

One error that would definitely come up is if the DSL cannot parse what the student has written in the program. Because of the audience, such error messages would have to be as simple as possible (ex. Only numbers please!) Another error would be if a student tries to break the program through something like a buffer overflow attack. The code would have to be well-designed such that these vulnerabilities do not exist.

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be very easy to write out problems that are within the supported types, even for someone with no prior coding experience. It should be possible to add support with other libraries like matplotlib for visualizations. It should be very hard to add your own supported problem types, because you would need to add your own parsing and logic to make that happen. 

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I think the obvious point of comparison here is mathematics software like Wolfram Alpha, and even AI tools like ChatGPT. These are DSLs in my mind because they focus on the domain of mathematics and you communicate through a mathematical language to get answers. For these languages, I like how simple they are to use, where you can just input the problem and it will interpret it for you. While these can walk through a math problem in some detail, they just present the steps instead of forcing the user to work through them themselves, so I think that that part can be improved. 

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

### Scope

I think that I would spend about 25% of my time on "language" and 75% of my time on "systems".

_How big an idea is this? How ambitious is this project?_

To complete this project, you need (1) a parser that can intuit what kind of problem was inputted (2) logic that builds the steps for which a student should complete a problem and (3) presents this to the student in an engaging and usable fashion. I could see this project getting out of hand if you went really in-depth on quality of life features (for both the teachers who are scripting and the students who are interacting with the finished product) or tried to support too many problem types. But if you stick to a small set of supported problems then I think this project would be manageable.

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

I think this would be a cool project because it could have a real impact on students if done properly - it's not something more technical or abstract like my other proposals and I respect that. This might not be a good idea if I get too bogged down on implementing the parsing and the logic, distracting from the language design.