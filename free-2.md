# Free project 2

## The user and a language

This section describes who the project would serve and why a language might be a
good way to meet their needs.

### What's the need?

_What need is met by your idea? Who are you helping? What is that person's
experience like now? What would their experience be like if you could help
them?_

My idea is for a DSL that lets you easily import election data (typically shapefiles for the borders of states/counties/districts along with corresponding election percentages) and visualize it in a pleasing manner. This DSL would help those who are curious about visualizing this kind of data, but lack the coding experience to get it done through typical means. Such people would be interested in politics (perhaps to an unhealthy degree) but had never made any maps of their own before. After my DSL, they would have made some maps of their own using real data, and would hopefully feel motivated to do more with the data they've found.

### Why a language?

_Why is a DSL appropriate for your user(s)? How does it address the need?_

A DSL is appropriate here because it would abstract away the many pieces that are typically required for this work. In something like Python, that would be a geospatial data management library like geopandas, a data visualization library like bokeh, and all the settings needed to make it look appealing. Election data is really cool, but generating your own maps can be a chore, and this DSL would fix that. 

### Why you?

_What excites you about this idea? How did you come up with it?_

I've always wanted a good excuse to dip my toes into analyzing political data. I've been interested in politics since I was a kid, and there's a wealth of things to do with it in CS/data science. This tool is the kind of thing I wish I had just to play around with in my spare time. I came up with it by thinking about my interest in gerrymandering and how it would be cool to visualize those kinds of results.

### Domain

_Describe the project's domain in five words._

Easily making political result maps! 

### Interface (syntax)

_How might the user interact with the language? What does programming look
like? Why is this the right way to interact with the problem domain?_

In the DSL, the user would have a small set of functions to interact with for importing their data, visualizing it on a map, and then tweaking options to their liking. The options would have to be a reduced subset from what you could do in a visualization library like bokeh in order to hold to the vision of a streamlined mapping DSL. I think this is the right way to interact with the DSL, because like my crystal simulation project proposal, you're breaking the domain up into slices that are not too big and not too small!  

### Operation (semantics)

_What might happen when a program runs? How does a program interact with the
user? What kinds of errors might occur, and how might they be communicated to
the user?_

When a program runs, it performs all of the commands and then visualizes the resulting map in a pop-up window. The map itself wouldn't be very interactive; if the user changes something in the script, they can run it again to see the results.

A very common error for people would be trying to import data that is invalid. This could be for a laundry list of reasons, but the error messages should clearly state the problem and explain what data types are supported. More specifics on the error would also be nice (ex. no id column that links election results to counties in the shapefile).

### Expressiveness

_What should be easy to do in this language? What should be possible, but
difficult? What should be impossible or very difficult?_

It should be easy to import valid data and use that data to generate appealing maps. It should be possible but difficult to expand the options available for adjusting how the maps are visualized. Lastly, it should be very difficult to do any sort of data querying in my language, because at that point you should graduate to something more substantial.

### Related work

_Are there any other DSLs in this domain? If not, describe how you know there
aren't and conjecture why not. If so, describe them and provide links. How well
do they address the need? Are there any particularly admirable qualities of the
language? Are there parts of the language you think could be improved?_

I couldn't find a DSL for political mapping specifically, but there are some for making general-purpose maps. For example, here's [a paper describing a DSL for web-based GIS](https://lbd.udc.es/Repository/Publications/Drafts/1569501806400_2019-APMDWE.pdf). It seems to handle creating GIS entities and layers pretty well. For this language, I like the similarities to SQL. As the GIS work is so data-driven, it makes sense to draw from another very data-driven language for the syntax. One critique I have of this language is that the scope of it is a little broad for a DSL, in my opinion. Because it's covering the whole of GIS, I have to wonder if the user would be better picking up software like arcGIS/QGIS with much better visualizations built-in. Maybe if the language focused on one particular application of GIS then it would be better. 

## The Project

This section examines whether the idea makes for a good CS 111 project.

### Suitability

_If someone were to work on this project, what percentage of their time would be
spent directly engaging in the **language** aspects of this project (e.g.,
making language design decisions), as opposed to "systems" aspects of the
project (e.g., implementing a complicated semantics that doesn't require a lot
of language design)?_

I think that I would spend about 45% of my time on "language" and 55% of my time on "systems".
### Scope

_How big an idea is this? How ambitious is this project?_

I think out of my proposed projects, this one is the most manageable. If Python is the host language, then the geopandas/bokeh pathway for visualizing this kind of data is pretty well-trodden. This would give me more time to focus on the syntax of my language!

### Benefits and drawbacks

_Why might this be a good idea for a project? Why might this not be a good idea
project?_

This would be a cool idea for a project because it lowers the barrier to entry for making political maps. One drawback with this project is that it is likely that existing tools would be more powerful (if a good bit harder to use), and the skills learned in my DSL might not translate. You're also limited in terms of the amount of data you can visualize without some kind of database in the back-end.