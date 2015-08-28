# Scraping

In this assignment you will learn to use the Document Object Model (DOM) using
Python via the Pattern library, in a few weeks you will also access the DOM
from Javascript. For the programming excercises in this homework, we provide
both some scaffolding and automated tests that are also used when grading the
homework.

* The Python module that you will need to complete for the first programming
  exercise: [exercise.py]
* Test script that should work with your code: [test-exercise.py]
* The IMDB highest ranking TV-series exercise: [tvscraper.py]
* The test script for this exercise [test-tvscraper.py]

[exercise.py]: exercise.py
[test-exercise.py]: test-exercise.py
[tvscraper.py]: tvscraper.py
[test-tvscraper.py]: test-tvscraper.py

## Python Exercise

Welcome to Python! At this point, we hope you have Python up and running. If
you're having a lot of trouble, please come see us at Office Hours. Reinstalling Python can fix certain strange issues you might
come across.

1. Open up `exercise.py`
2. Follow the instructions in the comments or below and complete the exercise!
3. You are allowed to import other libraries but no using the split() function
4. To run python, simple type in commands ''python exercise.py''
5. To test the functions you implemented after running your script type the command ''python test-exercise.py''

### Building `exercise.py`

This is your first exercise in Python! Use it as a warmup exercise. The
built­in `aString.split()` in Python only uses white­ space to split the string.
This is annoying because if you had a sentence with punctuation marks, the
procedure won't be able to recognize it.

In this exercise you will implement a string splitting function that can split
on several separators. As inputs it takes a string (the one you want to split)
and a string of separator characters. The output of this function should be a
list of strings that result from splitting the first string on each of the 
separator characters.

We have provided a Python module [exercise.py] with an incomplete
implementation of this more general string splitting function, it is up to you
to complete it. Open the python module and look for the function
`split_string(source, separators)` and implement it.

Whenever possible we strive to provide you with a file to test your code as
well. For this exercise the Python script [test-exercise.py] that will check
whether your implementation of `split_string(source, separators)` is correct.
This script will also be used in grading your implementation.

Unlike some other programming languages (such as C), blocks in Python are
defined by indenting. If you make mistakes with the indenting your script,
it will not work. For this class we stick to the most common (and 
recommended) way of indenting Python, i.e. using 4 spaces. More
recommendations on proper Python style can be found in [PEP8]. It is no
problem if you cannot understand everything in PEP8 yet.

[PEP8]: http://www.python.org/dev/peps/pep-0008/

Note: DO NOT USE `split()`, but you can import other libraries (i.e. regular
expressions) There are many solutions so as long as it works!

## DOM scraping and traversal

To scrape data, we will be using Pattern, a Python web mining module. Its
description is as follows:

> Pattern is a web mining module for the Python programming language. It bundles
> tools for data mining (Google + Twitter + Wikipedia API, web spider, HTML DOM
> parser), natural language processing (tagger/chunker, n­gram search, sentiment
> analysis, WordNet), machine learning (vector space model, k­means clustering,
> Naive Bayes + k­NN + SVM classifiers) and network analysis (graph centrality
> and visualization). It is well documented and bundled with 30+ examples and
> 350+ unit tests.

Instructions:

1. We assume Python and pattern are installed (see [preparations] if this is not
the case).

2. We will be looking at IMDB TV Series and getting data off this website. To
get started, you should look at the `examples` folder within `patterns­2.5`
Under `01-web` folder, look at example `07-dom.py`. If you have `pattern2.6`
the example is in directory `01-web` in the file `12-dom.py`.

The documentation on the website is also useful.

3. To get you started we have provided you with a script [tvscraper.py] that 
loads the correct IMDB address, makes a local backup of it (`tvseries.html`)
and outputs a CSV file (`tvseries.csv`) that will contain only a header until
you complete the implementation of the functions `extract_tvseries(dom)` and
`save_csv(f, tvseries)`.

4. To help you validate your script we provide both an example output CSV
file [output.csv] and a test script [test-tvscraper.py]. To use the latter you
must first run the `tvscraper.py` script (with the command 
`python tvscraper.py`). This will copy the IMDB webpage to the local directory
and save a CSV file. After you get these files run `test-tvscraper.py` from 
the same directory. If your implementation of the missing functions is
correct, you will see no ERROR of FAIL messages.

5. When you hand this exercise in be sure to submit: your `tvscraper.py`, 
`tvseries.html` and `tvseries.csv`. This will allow us to verify that your
output CSV file is correct and that the script actually works given the HTML
from IMDB.

6. It could be that there are missing data (for instance the runtime), insert
   an appropriate value when something is missing.

[output.csv]: output.csv
[test-tvscraper.py]: test-tvscraper.py
[preparations]: http://data3.mprog.nl/homework/preparations

### Building `scraper.py`

This is the introductory exercise to Pattern. We will try to guide you along as
much as possible, but you should read up on documentation and get used to doing
that. It's a really useful skill and a big part of programming is 
self-­learning!

This is also just a skeleton so you actually don't have to use this at all. As
long as your code runs at the end of the day and produces the write results in
a CSV file, we're happy.

Print is probably going to be your best friend for debugging so print often
especially if something goes wrong.

This is taken from the documentation, which you should learn to read!

	The DOM object is a tree of Element and Text objects. All objects inherit
	from Node, DOM also inherits from Element.
	
	Node.type => NODE, TEXT, COMMENT, ELEMENT, DOM
	Node.parent => Parent Node object
	Node.children => List of child Node objects
	Node.next => Next Node in Node.parent.children
	Node.previous => Previous Node in Node.parent.children
	
	DOM.head => Element with tag name "head"
	DOM.body => Element with tag name "body"
	
	Element.tag => Element tag name, e.g. "body"
	Element.attributes => Dictionary of tag attribute, e.g. {"class": "header"}
	Element.content => Element HTML content as a string.
	Element.source => Element tag + content
	
	Element.get_element_by_id(value)
	Element.get_elements_by_tagname(value)
	Element.get_elements_by_classname(value)
	Element.get_elements_by_attribute(name=value)
	
	You can also use short aliases: by_id(), by_tag(), by_class(), by_attribute()
	The tag name passed to Element.by_tag()
	can include a class ("div.message") or an id ("div#header").

## Submitting

Add a folder Scraping to your DataProcessing/Homework repository containing the following files:

1. `exercise.py`
2. `tvscraper.py`
3. `tvseries.html`
4. `tvseries.csv`
