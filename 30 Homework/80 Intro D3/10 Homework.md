# Intro D3

This is an introduction assignment to D3. Please take time to read the tutorials carefuly. 


[D3website]: http://d3js.org/

## Resources

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


## Introduction: Readings on D3 and SVG

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
   appended, and what parts of the graph did these elements correspond to?

## D3 setup
You can find the detailed instructions on how to set up D3 [here][1].

[1]: https://github.com/mbostock/d3/wiki

*  Download the latest version of D3 [here][2]. Or, to link directly to the latest release, copy this snippet into your html file:
    
      <script src="//d3js.org/d3.v3.min.js" charset="utf-8"></script>

* When developing locally, note that your browser may enforce strict permissions for reading files out of the local file system. If you use d3.xhr locally (including d3.json et al.), you must have a local web server. For example, you can run Python's built-in server (in the console):

      python -m SimpleHTTPServer 8888 &

or for Python 3+
      
      python -m http.server 8888 &

You should run the server from within the directory where your html file is located. Once the server is running, go to: http://localhost:8888/.
   
[2]: https://github.com/mbostock/d3/releases   
   
## Load dataset in JSON

The most convenient way to load your data set with D3 is to use JSON format and to
load it using the `d3.json` function. You can also use a CSV file, as long as you load your data from a separate file and use the proper d3 function to load it. Note that these loading functions take callbacks and that the
file loading is done asynchronously, so the data will only be available in
the scope of the callback. As an aside: if you want to load several files
that all need to be available before your program can run look into 
[queue.js].

[queue.js]: https://github.com/mbostock/queue

* Find the dataset that you would like to show in a barchart. You can use for example the [KNMI webpage] again to download the avarage monthly amount of rain in De Bilt in 2015.

* Create a barchart.html file with a title of your data visualisation, include/link to the D3 library and include the barchart.js where you will write the rest of your code.

* Convert the data into JSON format and load it using D3. Using console.log check whether your data is loaded correctly. Don't forget to run the server!


[KNMI webpage]: http://projects.knmi.nl/klimatologie/daggegevens/selectie.cgi

## Submit

* Create folder D3 in your master branch and push the following files:
    * `questions.pdf`
    * `barchart.html`, `barchart.js` ( and `barchart.css`, if necessary) contained in a folder `Barchart`




