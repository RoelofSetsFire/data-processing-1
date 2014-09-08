## Introduction

In this homework you will get more experience scraping data from the web as
well as answer questions on the readings.

As always if you need help, the first place you should check is Piazza because
likely someone else will have had the same problems as you!

## Problem 1: Web Crawling & HTML Scraping

For this exercise, we will practice scraping from multiple websites using
web-crawling. You will learn how you can acquire data from multiple pages by
following links. You’ll be scraping data from IMDB, the Internet Movie Database!

For this exercise we have provided some scaffolding that handles making HTML
backups of a few selected web pages. It also handles writing Unicode to your 
CSV file. You will provide the code that does the
actual scraping of the top 250 movie index page and the code that scrapes the
individual movie pages on IMDB. Download the scaffolding
[here](imdb-crawler.py). You should submit your version of this script along
with the output CSV file (`top250movies.csv`), and the two backup HTML files
that the script creates (`index.html` and `movie-083.html`). 

The goal of this exercise is to create a CSV file containing for each movie in
the top 250:

* Title of movie
* Runtime
* Genre (separated by semicolons if multiple)
* Director(s) (separated by semicolons if multiple)
* Writer(s) (separated by semicolons if multiple)
* Actors (only the first three actors listed, separated by semicolons)
* Ratings
* Number of Ratings

Make sure that your python script produces clean results that do not need
additional cleanup. For example, the entry "Writer" should only contain
"Stephen King; Frank Darabont"", not "Stephen King (short story "Rita Hayworth
and Shawshank Redemption"); Frank Darabont (screenplay)".

Your output should look like [`sample_HTML.csv`](sample_HTML.csv).

**Remarks**

* Have a look at the `pattern.web.Element` documentation and look for 
  the attribute selectors, they come in handy for this exercise.
* The script will likely be slow, but that is no problem.

## Alternative exercise

*You are allowed to create a script from scratch that crawls another
datasource but it should be of similar complexity to the IMDB data. So
at least 5 attributes per entry and at least 200 entries. Also, to collect
all information you should at least follow links to other web pages (not
just scrape a single web page. If you are in doubt your data source is 
complex enough, please ask in class.*


## Problem 2: Questions about the readings.

1. Ware describes bottom up and top down processing of visual information in
   the brain. Give a concrete and detailed example of how bottom up processing is
   influenced by top down processing, leading to a potentially wrong
   interpretation of "reality" by the viewer. Your example can include a
   screenshot, photo, or web site URL to refer to the scene that is being viewed.

2. Go to the Many Eyes website and browse around the visualizations. Click
   through a few and look at the comments. How successful do you think Many Eyes
   has been in achieving its original design purpose according to the paper? What
   do you think is the biggest issue/flaw with Many Eyes? What improvements might
   you suggest to Many Eyes to address these issues/flaws?

