# Design 3 - Github Commit Graph

In this design workshop you will sketch multiple solutions to visualize the commit graph and the branches of a git repository. 
Submit one document as a group which contains the analysis, sketches and the reflection with the final visualisation.

# PART 1 - ANALYSIS 

Time: 20 minutes

Take a look at various Github Network Graphs. Here are two examples [1], [2].


[1]: https://github.com/Caleydo/caleydo/network
[2]: https://github.com/CS171/CS171.github.io/network

* Think about how these networks are different. Analyze the “dimensions” of these networks. What are the relevant attributes (e.g., commits, users, branches, commit size, etc.) of these representations? What other attributes could be relevant in this graph? Write a list of all the attributes your visualization could show. 
* Are there different roles, i.e., different types of users who might want to achieve different things? Write a list of user roles. 
* Think about which tasks a user of your visualization might want to achieve. Write down a list of tasks. 
* Identify one role that you want to design your visualization for. Prioritize your task and attribute lists based on this role’s needs. 

# PART 2 - SKETCHING

Time: 30 minutes

Design two alternative visual representations for the Github Network. You should design for an interactive system, i.e., you should not assume that you have to fit all content onto paper. 
You can refer to Heer's article [Reading 3] for the examples of network visualisations, browse [D3 website], and feel free to use any other sources.

[Reading 3]: /readings/reading-3
[D3 website]: https://github.com/mbostock/d3/wiki/Gallery

Here are some questions to consider:

* Decide on which visual variable to use for which attributes of the visualizations. Consider the strengths and weaknesses of visual variables that were mentioned in Carpendale's article [Reading 1] (also briefly discussed in this week's lecture: [Process]). Use the strongest visual variable for the most important attributes of the data.
* Do you think it is necessary to represent every single commit as a separate node? Could you think of ways to aggregate this?
* Do you think that every contributor needs a “row”, as on the default network view on github? Could you think of a smarter way to summarize those? 
* Is a node-link diagram the appropriate representation? Or should you consider alternative graph representations?


[Reading 1]: /readings/reading-1
[Process]: /lectures/process


# PART 3 - Group Reflection 
Time: 40 minutes, or as long as you like. 

Take your analysis and ideas and discuss it again. Can you find a consensus? Come up with one visualization that you agree is ideal.
Reflect on the process that you went through to come up with your final design (refer to this week's lecture: [Process] for inspiration on design process).
