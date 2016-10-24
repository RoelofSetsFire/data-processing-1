# Prepare JSON data for barchart in D3

The most convenient way to load your data set with D3 is to use [JSON format].

* Find the dataset that you would like to show in a barchart. The preferable format is a csv file, but it can be any other format as long as it's not JSON. You can use for example the [KNMI webpage] again to download the average monthly amount of rain in De Bilt in 2015.

* Convert the data into JSON format using python. Try to make your script as general as possible so that you can re-use it to format other datasets (will become useful in other assignments in this course, in the programming project and probably in other courses, where you need to manipulate data).


[JSON format]: http://www.w3schools.com/json/
[KNMI webpage]: http://projects.knmi.nl/klimatologie/daggegevens/selectie.cgi

## Submit

Create folder D3 in your master branch and push the following files:

* `convertCSV2JSON.py`
* both datasets (.csv and .json)
