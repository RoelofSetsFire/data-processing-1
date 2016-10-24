# D3: Implement an interactive multiseries line graph with D3

Note: there are plenty of links in this assignment so that you browse through a lot of examples to see what is possible in D3. This does not mean your visualization should look and work exactly like those in the examples. This is just for inspiration! Also do not blindly copy the whole code, always create your files from scratch.


## Part 1: Create line graph
Before you get started, take a look at these D3 examples of a [simple line graph] and a [multiseries line graph]. Note for the simple line graph, the
JavaScript is < 60 lines with whitespace. You are supposed to create a plot
from scratch, not just copy from the examples.

[simple line graph]: http://bl.ocks.org/mbostock/3883245

[multiseries line graph]: http://bl.ocks.org/mbostock/3884955

Now create a line plot using the D3 functionality. The line plot should consist of a single line (example: average temp per month for one year).
Make sure that you properly label the axes, that the plot has a title and that the data source is 
explained. Make sure that the date axis uses JavaScript dates, something that is
quite easy using d3.time.format function.

## Part 2: Add interactivity

As you already know the D3 selection.on function allows you to bind event listeners to DOM elements. 
Create a moving cross-hair (or [a dot]) by binding an event listener to the appropriate DOM element. 
Note that D3 also makes dealing with mouse coordinates quite easy, see d3.mouse, and that the D3 scales
have an invert function. 

[a dot]: http://fundvis-ywng.rhcloud.com/JPMProvident.html

Create a [pop-up] next to your moving cross-hair/dot in which you print the exact values of the variables (example: date and temperature). 


[pop-up]: http://tylernwolf.com/#/portfolio/corrdisp


### Submit 
Submit your completed files in a folder titled `d3line` containing `d3line.html` , `d3line.js` and
`d3line.css`.


##Part 3: Extend your graph to plot multiple lines for different years

Make sure you create a separate set of files to create the mutliseries line plot.

Start with creating a plot that shows not one but at least three lines. Those lines should be permanently visible on the plot (only if you are ahead of schedule you can try to add/remove the lines interactively).

Your plot should have the same interactivity as the just created single line graph.
Extend your new multiseries line plot with one more interactive element. Add an element of your choice that will allow you to toggle between the extra variable (see Part1 point 3). For example you can make a [drop-down] where you choose a variable (example: a year), a [button] or [list] that toggles between variables (example: two different years) or a [slider] to change the variable.

[drop-down]: http://bl.ocks.org/anupsavvy/9513382

[slider]: http://romsson.github.io/dragit/example/nations.html

[list]: http://charts.animateddata.co.uk/whatmakesushappy/

[button]: http://statick.org:3000/


### Submit 
Submit your completed files in a folder titled `d3lineExtended` containing `d3lineExtended.html` , `d3lineExtended.js` and
`d3lineExtended.css`.

[queue.js]: https://github.com/mbostock/queue

