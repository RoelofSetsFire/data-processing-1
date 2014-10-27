## Introduction

For this week's homework you will work with the [D3 library][D3website] to
create a number of graphs and implement an interactive map.

[D3website]: http://d3js.org/

## Resources

### The D3 library

* [D3 for Mere Mortals] by *Luke Francl*: A single, relatively short tutorial
  which covers fundamental concepts for D3 and how to approach creating a
  visualization
* [D3 Wiki Tutorials] by *Mike Bostock*: Tutorials straight from the source,
  starting off with simple, straightforward tutorials like the ones above.
* [D3 Tutorials] by *Scott Murray*: A series of tutorials that are in the
  O’Reilly book Interactive Data Visualization.

[D3 for Mere Mortals]: http://www.recursion.org/d3-for-mere-mortals/
[D3 Wiki Tutorials]: https://github.com/mbostock/d3/wiki/Tutorials
[D3 Tutorials]: http://alignedleft.com/tutorials/d3/


## Introduction

In this homework, you will work with JavaScript, SVG and D3. As always, if you
need help, the first place you should check is Piazza because someone else may
have already posted about the same problems or questions as you!

Note: This homework comes with supplementary files which you can download
[here](HW_8_Supplementary_Files.zip).

## Problem 1: Readings on D3 and SVG

Please read this [blog post about D3], [Three Little Circles], [A Bar Chart
Part 1] and answer the following questions. For further reference a short list
of D3 and SVG resources is included below. Please take a look, as these may be
helpful for this homework or future projects!

[blog post about D3]: http://www.jeromecukier.net/blog/2013/03/05/d3-tutorial-at-strata-redux/
[Three Little Circles]: http://mbostock.github.io/d3/tutorial/circle.html
[A Bar Chart Part 1]: http://mbostock.github.io/d3/tutorial/bar-1.html

1. How can D3 access and change the DOM? What do `select` and `selectAll` do?

2. What are the `d` and `i` in `function(d){}` and `function(d, i){}`?

3. Write sample lines of JavaScript to add a `div` element with class
   "barChart1" and to add an svg element with class "barChart2" with square
   dimensions.

4. Describe `append`, `update`, `enter`, and `exit` at a high level. What does
   "selectAll + data + enter + append" refer to?

5. What are the main differences between drawing a bar chart with HTML and SVG?

6. In drawing the simple bar chart with D3 and SVG, what elements were
   appended, and to what parts of the graph did these element correspond?


## Problem 2: Implement a Line Graph with D3

For this assignment you will create a line graph that is not interactive. The
data you use for this assignment is up to you (as long as the data points have
at least two variables that can use an positional encoding).

Before you get started, take a look at [these D3 examples] for a simple line
graph and a multiseries line graph. Note for the simple line graph, the
JavaScript is < 60 lines with whitespace. You are supposed to create a plot
from scratch, not just copy from the examples.

[these D3 examples]: https://github.com/mbostock/d3/wiki/Gallery

The most convenient way to load your data set is to put in JSON format and to
then load it using the `d3.json` function. 


### Instructions

Start by reading the relevant example and use it as a guide to building your
graph.


### Set up the scales and axes

This is about the first 30 lines in the script from the example. You may need
to change the x scaling and format a bit more depending on if your date is in a
different format or your x values are not dates. For more about time formatting
in D3 see the time formatting documentation.

### Use your JSON data

You will need to work with your JSON data as Arrays. If your points were
formatted similar to the example in HW5, you should have something like
`{...,“points”:[[x0,y0],[x1, y1],...],...}`. Otherwise, you may need to do a
little extra processing such as with `d3.entries()`. You will need to isolate
your array of points, make sure the points are in the right order, and do any
manipulation to the types. For example, the time formatting mentioned above.
Here is the documentation on D3 Arrays. Some helpful functions are
`array.forEach` and `array.reverse`.

### Create the graph

This will follow the rest of the example. When modifying these lines, keep in
mind that each of your points is an Array of two (or more, if there is a
comment) elements. Try to go through the different lines and understand what is
being done. For example, `d3.extent(data)` returns an array with the minimum
and maximum element from its argument. Consider what each attr does.

Submit your completed files in a folder titled `d3line` containing `d3line.html` and
`d3line.css`.


## Problem 3: D3 scatter plot

For this problem you will create a scatter plot using D3. The data you use
can be same data as you used for the line graph, or it can be some new
data set. Look up an example of a scatter plot in the D3 examples, and use
it as a guide to constructing a scatter plot. If your data points have a 
third value (beyond the X and Y values), you could encode that for instance
as the size of your marks. While you can choose what marks to use for each
of the data points it is suggested you use circles.


## Problem 4: Interactive map with D3

In this problem you will be analyzing your geographical data with D3, the idea
is to find a data set that has data for each country (or most countries) in the
world and use that data to make a choropleth. Data you could use are the number
of inhabitants, the GDP, or the population density.

D3 contains an add­on called datamaps which you can get at
<http://datamaps.github.com>. Datamaps will replace your svg map for this
problem. Check out its various examples of usage, including
<http://bl.ocks.org/markmarkoh/4127667>. Adapt Problem 3 so as to visualize the
same data, but this time using D3 and datamaps. Specifically, you will need to
adapt your JSON format to be compatible with that expected by datamaps. For
example, if you were to modify the example at 
<http://bl.ocks.org/markmarkoh/4127667>, you will need to figure out the 
three-letter country codes:

	fills: {
		_your_class_name_: '...', // your color here
		// fill more classes
		defaultFill: '#00446A' // Rest of world
	},
	
	// Fill in countries, key is three letter country name.
	// data contains fillKey and tooltip (name)
	data: {
		'MEX':{ // e.g.mexico
			fillKey: '..', // refer to class name, above
			name: 'for tool tip'
		},
		...
		// add more countries here
	}
	...

### Interactivity

By using datamaps, you should now be able to add interactivity to your map. In
the example above country names appear upon mouseover. You should also make
country names as well as the raw values of your data appear on mouse over. You
can choose how to show this information, either as a tool tip or a label inside
or aside the country. In addition you should also implement some sort of
highlighting mechanism, e.g., changing the fill (color or opacity) or stroke of
the country that is being moused­over.

### Discuss your interactivity choices

At the bottom of d3map.html (the HTML page that contains the map you are making)
briefly explain the design choices you made with
regard to interactivity. What kind of mouseover effects did you enable and why?
What visual queries does your map support and what ones does it not?

Submit your completed files in a folder titled 5 containing d3map.html,
d3map.css, and d3map.js. Note that you may not need d3map.css here unless you
would like to change additional styling with regard to text, margins, etc.

## Problem 5: Questions about the readings of [reading 6][]

1. According to Bostock et. al., what are the primary advantages of D3? Based
on your reading of the article, please provide an example of a type of
visualization that would be easier and better implemented in D3 as opposed to
HTML5, JSON, and Javascript. Please list the pros and cons of choosing D3 over
pure HTML5, JSON and Javascript.

2. Of the visualization figures presented in Heer et. al., which do you find
the most difficult to comprehend? Does the complexity of the figure interfere
with the goal of visualization as described in the article? Include a
screenshot of the figure you have chosen in your response and use principles
that you have learned so far (i.e., from design, perception, and cognition) to
justify your choice.

3. Play around with the interactive graphs included in the Heer article. You
need to open this page in a browser that runs Java. Focus on Figure 1A. To what
extent do interactivity and transitions, elements that D3 optimizes, add to the
clarity and message of the visualization? With the element of interactivity in
mind, redesign and sketch the contents of figure 1A with one of the other
visualization types described in the Heer article. Include a picture of a
sketch of your idea, and describe how it supports comprehension and data
exploration.

[reading 6]: /readings/reading-6

## Submitting

Your submission should be in `hw8.zip` and include the
following items:


1. Your map from each stage of the process, contained in a folder:
   * 1: d3questions.pdf
   * 2: d3line.html, d3line.css, and d3line.js
   * 3: d3scatter.html and d3scatter.css
   * 4: d3map.html, d3map.css, and d3map.js

2. Any libraries used, including d3 if linked to a local copy.
