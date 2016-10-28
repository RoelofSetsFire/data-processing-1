# D3: Prepare dataset for an interactive multiseries line graph with D3

In the assignment next week you will create a line graph based on your own dataset (you can use again the KNMI dataset).
In this assignment you will prepare your own dataset. 
Your dataset should contain the following variables:

1. time variable (eg.: data per month)

2. at least three different variables for 1 time stamp (eg.: maximum temperature, minimum temperature, average temperature per month)

3. this dataset should be dependent on one extra variable, which should have at least two values (eg.: two different years, two different cities)

Make sure that you put your data in JSON format correctly (the JSON format is compulsory).
Optionally, you can use multiple data files. If you want to load several data files
that all need to be available before your program can run look into 
[queue.js]. This D3 example uses queue to load two json files: [D3: Queue.js].

As usual, create a new HTML file (d3line.html) that loads the D3 script (make sure that you have this file saved locally).
Create separate JavaScript file for drawing the lines (d3line.js). Load the dataset that you created and create data structures that will contain your data (which you will use to access the data to draw the line).


[these D3 examples]: https://github.com/mbostock/d3/wiki/Gallery

[queue.js]: https://github.com/mbostock/queue
[D3: Queue.js]: http://bl.ocks.org/mapsam/6090056


## Submit 
Push the created files into a folder titled `d3line`. It should contain your JSON dataset, `d3line.html` , `d3line.js` and `d3line.css`, if needed.


