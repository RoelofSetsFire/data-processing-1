# Interactive barchart with D3

This week you will implement an interactive barchart using D3. Note that you are not allow to use any other libraries then D3.

##Part 1: Intro D3
This is an introduction assignment to D3. Please take time to read the tutorials carefully. 
Please note that for all the assignment in this course we will be using version 3 of D3!


[D3website]: http://d3js.org/

### Resources

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


### Introduction: Readings on D3 and SVG

Please read this [blog post about D3], [Three Little Circles], [A Bar Chart
Part 1] and answer the following questions (save your answers in questions.pdf).
For further reference a short list
of D3 and SVG resources is included below. Please take a look, as these may be
helpful for your homeworks or future projects!

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
   appended, and what parts of the graph did these elements correspond to?

### D3 setup
You can find the detailed instructions on how to set up D3 [here][1].

[1]: https://github.com/mbostock/d3/wiki

*  Download the version 3 of D3 [here][2]. Or, to link directly to the release 3, copy this snippet into your html file:

      `<script src="//d3js.org/d3.v3.min.js" charset="utf-8"></script>`

* When developing locally, note that your browser may enforce strict permissions for reading files out of the local file system. If you use d3.xhr locally (including d3.json et al.), you must have a local web server. For example, you can run Python's built-in server (in the console):

      python -m SimpleHTTPServer 8888 &

* or for Python 3+:

      python -m http.server 8888 &

You should run the server from within the directory where your html file is located. Once the server is running, go to:

      http://localhost:8888/.


### Load dataset in JSON

The most convenient way to load your data set with D3 is to use [JSON format] and to
load it using the `d3.json` function. 
Note that this loading function takes callbacks ([ex 1] and [ex 2]) and that the
file loading is done asynchronously, so the data will only be available in
the scope of the callback. As an aside: if you want to load several files
that all need to be available before your program can run look into 
[queue.js].

* Create a barchart.html file with a title of your data visualization, include/link to the D3 library and include the barchart.js where you will write the rest of your code.

* Load your JSON dataset (from Intro) using D3. Print the data to the console using console.log(). This will allow you to check whether your data is loaded correctly. 

[JSON format]: http://www.w3schools.com/json/
[ex 1]:http://recurial.com/programming/understanding-callback-functions-in-javascript/
[ex 2]:http://javascriptissexy.com/understand-javascript-callback-functions-and-use-them/
[2]: https://github.com/mbostock/d3/releases   
[queue.js]: https://github.com/mbostock/queue
[KNMI webpage]: http://projects.knmi.nl/klimatologie/daggegevens/selectie.cgi

##Part 2: Interactive barchart

Read [Part 3] of the barchart tutorial (you might want to read [Part 2] of this tutorial as well, if you haven't done so yet) and reproduce the barchart using your own data that you prepared this week (Intro).
As for interaction, your bars should change color while hovering over them (just like in the example in [Part 3]).
Additionally you should display the data value for the chosen bar above it (on mouse hover). You can either just print the text or use a d3-tip. 

[Part 3]: https://bost.ocks.org/mike/bar/3/
[Part 2]: https://bost.ocks.org/mike/bar/2/

Update your completed files in a folder `Barchart`: `barchart.html` , `barchart.js` and
`barchart.css`.  Note that you may not need `barchart.css` here unless you
would like to change additional styling with regard to text, margins, etc.


## Submit instructions

1. Push the following into your D3 folder on GitHub:
   * 1: `questions.pdf`
   * 2: `barchart.html`, `barchart.css`, and `barchart.js`, contained in a folder `Barchart`
   * 3: D3 library, if linked to a local copy.
