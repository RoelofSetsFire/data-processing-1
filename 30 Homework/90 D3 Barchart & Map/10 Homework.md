# D3

## Problem 2: Implement a barchart with D3



Submit your completed files in a folder titled `d3bar` containing `d3bar.html` , `d3bar.js` and
`d3bar.css`.


## Problem 3: Interactive map with D3

In this problem you will be analyzing your geographical data with D3, the idea
is to find a data set that has data for each country (or most countries) in the
world and use that data to make a choropleth map. Data you could use are the number
of inhabitants, the GDP, or the population density.

D3 contains an add-on called datamaps which you can get at
<http://datamaps.github.com>. Datamaps will replace your svg map for this
problem. Check out its various examples of usage, including
<http://bl.ocks.org/markmarkoh/4127667>. You could use  the same data as for the previous assignment, but this time using D3 and datamaps. Specifically, you will need to
adapt your data format to be compatible with that expected by datamaps. For
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
the country that is being moused-over.

### Discuss your interactivity choices

At the bottom of d3map.html (the HTML page that contains the map you are making)
briefly explain the design choices you made with
regard to interactivity. What kind of mouseover effects did you enable and why?
What visual queries does your map support and what ones does it not?

Submit your completed files in a folder titled `d3map` containing `d3map.html`,
`d3map.css`, and `d3map.js`. Note that you may not need `d3map.css` here unless you
would like to change additional styling with regard to text, margins, etc.

## Submit instructions

1. Create folder D3 in your master branch and push the following files:
   * 1: `d3questions.pdf`
   * 2: `d3line.html`, `d3line.css`, and `d3line.js`, contained in a folder `d3line`
   * 3: `d3map.html`, `d3map.css`, and `d3map.js`, contained in a folder `d3map`

2. Any libraries used, including d3 if linked to a local copy.
