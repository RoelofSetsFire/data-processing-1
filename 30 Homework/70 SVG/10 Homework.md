# SVG

In this homework you will learn to manipulate maps using Javascript. The maps
for the assignments below are in the Scalable Vector Graphics (SVG) format.
Much like HTML, SVG can be manipulated from Javascript through the Document
Object Model (DOM). For this week's homework you will create 2 static maps
using SVG, CSS and Javascript.

Note: This homework comes with supplementary files which you can download
here: [SVG_Supplementary_Files]. Another file that is very useful is the mapping between
[country codes and country names].

[SVG_Supplementary_Files]: SVG_Supplementary_Files.zip
[country codes and country names]: countries.js

## Resources

* [SVG tutorial] from the *Mozilla Developer Network*
* [SVG Documentation] from the *Mozilla Developer Network*: Documentation on
  SVG elements and what dimensions are needed.
* [W3Schools SVG tutorial]

[SVG Documentation]: https://developer.mozilla.org/en-US/docs/Web/SVG
[SVG tutorial]: https://developer.mozilla.org/en-US/docs/SVG/Tutorial
[W3Schools SVG tutorial]: http://www.w3schools.com/svg/default.asp


## Problem 1: SVG Maps

SVG is a vector-based alternative to the raster-based
Canvas. It is especially useful in cases where you want to interactively modify
your drawn shapes such as areas on a map.

The point of departure for this visualization is the map of Europe. You can find the `europe.svg` among the supplementary files. 
The map is fairly accurate, and each country is well delineated by its own
`<path>` (or several `path`s). Using a DOM inspector (such as Firefox’s Web Developer Toolbar or
Chrome’s Developer Tools (View > Developer > Developer Tools), shown below),
you can examine the SVG’s DOM structure, as well as identify the `<path>`
elements which make up the countries.

[on Wikimedia]: http://en.wikipedia.org/wiki/File:BlankMap-World6.svg

![map example](map-new.png)

In this problem, you will write a JavaScript function to change the fill color
of several countries.


### Continent setup

You have received four starter files with this homework: `svg.html`,
`svg.css`, `main.js` and `europe.svg`.

Begin by working on `svg.html`. Open the `europe.svg` with text editor, copy the svg and paste it into `svg.html`. The countries on the map are already marked with appropriate ids/classes.
In `svg.css`, change the fill color of three countries (eg. by ID) to three different colors of your choice.

### Programmatically change the color of a country

In `main.js`, write a function, `changeColor()`,that does what you did in `svg.css`
via JavaScript instead. Complete the `changeColor()` function here, which will
take as arguments the id of a path (country) and a fill color. This will come
in handy since most visualizations will want to color countries on-the-fly.

Then make sure your changeColor() function works by calling the function on 4
countries (different than those you have changed via CSS) when the page loads. Make sure that these colors are different than
those you have changed via CSS.

### Submit
Submit your completed files in a folder titled SVG1 containing `svg1.html`,
`svg1.css`, and `main1.js`. Don't forget to change the references in
`svg1.html` to reflect the changed stylesheet and js file names!
As usual push everything on GitHub! Don't forget to put your name in all the files!

## Problem 2: Analyze Geographical Data with SVG

In Problem 2, you will extend Problem 1 by preparing a dataset of
geographically indexed data in the JSON format and using this data set to
create a color-encoded map of your continent. Create new files, svg2.html,
svg2.css, and main2.js, based on your problem 2 solution.

### Acquire and prepare your data

Prepare a dataset of geographically indexed data. That is, you
can choose any data set provided that the data set points are indexed by country.
Examples include world population by country, literacy rates by country, etc.
Wikipedia has good examples like [List of Countries by Population] and [List of
Countries and Dependencies by Population].

Your visualisation could consists of Europe only. In that case use the SVG map provided in the assignment. Alternatively you can visualise the whole world. Freely available SVG maps can be found [on Wikimedia].

[List of Countries by Population]: http://en.wikipedia.org/wiki/List_of_countries_by_population
[List of Countries and Dependencies by Population]: http://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population_density

Write a python script to convert the data into JSON format ([JavaScript Object Notation]), and embed the formatted data into the
svg2.html document. This means your data will look something like:

	{
		"points" : [ 
			{ "country": "France" , "data": "3"},
			{ "country": "Germany" , "data" : "5"}, ...
		]
	}

Alternatively, your `points` object can be an array of arrays {"points": [["France", "3"], ["Germany", "5"], ....]}.

[JavaScript Object Notation]: http://www.w3schools.com/json/

### Color code your map

Using JavaScript, iterate over your dataset. 
Check [JSON HowTo] to convert a JSON text into a JavaScript object.

For each country in the dataset, locate the appropriate path with the same ID (you might want to use the mapping between
[country codes and country names]), and adjust its fill style to
reflect the data by color coding. 
That is, you may now get rid of any arbitrary colors applied from the previous
problem using CSS and only color countries by their encoded data.
The color coding is left up to you though you have to justify it. Choose a
spectrum which maps to the range of your data points. For example, a
population's range is from about 10,000 (Tuvalu) through 1,350,000,000 (China).
We strongly advise you to have a look at the [ColorBrewer]. If possible, always choose color scheme for your map with [ColorBrewer].

You do not have to do this for ALL countries. Your iteration loop can simply "skip" over countries whose
corresponding paths are not tagged in the SVG. If the path is present in the SVG but you don't have the data for the corresponding country, you have to treat it as a missing value. Choose one appropariate color for your missing values.

[JSON HowTo]: http://www.w3schools.com/json/json_eval.asp

### Add the details and discuss your implementation

This should look something like the following (again, an example of population
density):

[population density]: http://en.wikipedia.org/wiki/List_of_countries_and_dependencies_by_population_density

![map sample 2](map2.png)

You should also place a title above your graph. Though the example above
includes a proper legend, this is not required. Make sure though that it is understandable what the colors represent.

At the bottom of `svg2.html` ( *visible when the page is viewed in a web browser* 
), explain your choice of colors. Try to invoke some of the principles of color mentioned in the readings/designs
including the type of color series you are using (sequential, diverging, etc,
and also note that the above example may or may not be a good example of color
choice). Also, explain your reasoning behind creating the bounds for each
category in your encoding.

[ColorBrewer]: http://colorbrewer2.org/

### Submit
Submit your completed files in a folder titled SVG2 containing `svg2.html`,
`svg2.css`, and `main2.js`. Note that you may not need `svg2.css` here unless
you would like to change additional styling with regard to text, margins, etc.
Submit also your python script that converts your data to JSON format.
As usual push everything on GitHub! Don't forget to put your name in all the files!


### Checklist 

* Are all the files present and in the correct relative paths?
* Do you have enough comments and are your variable names appropriate?
* Did you push&commit everything on GitHub?
* Does every file contain your name?
