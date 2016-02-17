# D3

## Problem 2: Implement a Line Graph with D3

For this assignment you will create a line graph based on the KNMI dataset (that we used last week).
Create a new HTML file that loads the D3 script (make sure that you have this file saved locally).
Create separte JavaScript file for your program.

Before you get started, take a look at [these D3 examples] for a simple line
graph and a multiseries line graph. Note for the simple line graph, the
JavaScript is < 60 lines with whitespace. You are supposed to create a plot
from scratch, not just copy from the examples.

[these D3 examples]: https://github.com/mbostock/d3/wiki/Gallery

The most convenient way to load your data set is to put in JSON format and to
then load it using the `d3.json` function. You can also use a CSV file, as long as you load your data from a separate file and use the proper d3 function to load it. Note that these loading functions take callbacks and that the
file loading is done asynchronously, so the data will only be available in
the scope of the callback. As an aside: if you want to load several files
that all need to be available before your program can run look into 
[queue.js].

[queue.js]: https://github.com/mbostock/queue

Now create a line plot using the D3 functionality, make sure that you properly
label the axes, that the plot has a title and that the data source is 
explained. Make sure that the date axis uses JavaScript dates, something that is
quite easy using d3.time.format function.

D3 also supports interactivity, in particular the selection.on
function allows you to bind event listeners to DOM elements. Recreate the 
moving cross-hair from week 5's assignment by binding an event listener
to the appropriate DOM element. Note that D3 also makes dealing with mouse
coordinates easier, see d3.mouse, and that the D3 scales
have an invert function. Recreate the pop-up of week 5 as well, 
here you can use D3 to manipulate the DOM, but the use of setTimeout
is no different from that of week 5.

Submit your completed files in a folder titled `d3line` containing `d3line.html` , `d3line.js` and
`d3line.css`.


## Problem 3: Interactive network with D3


### Discuss your interactivity choices

At the bottom of d3network.html (the HTML page that contains the map you are making)
briefly explain the design choices you made with
regard to interactivity. What kind of mouseover effects did you enable and why?
What visual queries does your map support and what ones does it not?

Submit your completed files in a folder titled `d3network` containing `d3network.html`,
`d3network.css`, and `d3network.js`. Note that you may not need `d3network.css` here unless you
would like to change additional styling with regard to text, margins, etc.

## Submit instructions

1. Create folder D3 in your master branch and push the following files:
   * 1: `d3questions.pdf`
   * 2: `d3line.html`, `d3line.css`, and `d3line.js`, contained in a folder `d3line`
   * 3: `d3network.html`, `d3network.css`, and `d3network.js`, contained in a folder `d3network`

2. Any libraries used, including d3 if linked to a local copy.
