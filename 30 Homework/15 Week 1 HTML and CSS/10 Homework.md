In this homework, you will practice sketching and begin working with HTML/CSS.
As always, if you need help, the first place you should check is Piazza because
someone else may have already posted about the same problems or questions as
you!

Note: This homework comes with supplementary files which you can download
[here](hw5files.zip).

## Problem 1: Sketching (25%)

Have a look at this [movie from the Open University] UK that demonstrates well
what we mean by sketching.

[movie from the Open University]: http://www.open.edu/openlearn/science-maths-technology/engineering-and-technology/design-and-designing?track=109fd90ba3

Perform the following exercises on letter-sized white paper using a Sharpie or
a similar pen.

* 1 page of straight lines
* 1 page of arcs
* 1 page of circles
* 1 page of ellipses
* 1 page of textures/patterns

The goal of drawing textures is to practice various methods to fill in spaces,
to show a differentiation between spaces. It is encouraged for people to
experiment in styles. For instructions, have a look at the video about [Tone]
from the Open University.

[Tone]: http://www.open.edu/openlearn/science-maths-technology/engineering-and-technology/design-and-designing?track=3894637be0

* 1 page of icons -- draw things from around the house/cafe/etc and turn them
  into simple icons.

* 3 pages of graphic layouts

The goal of graphic layouts is to practice using the previous techniques
(lines, arcs, circles, textures, etc) in an applied manner. It is recommended
to start out by looking at a layout that already exists (ie website, magazine,
newspaper, etc) and copy it in a basic layout representation. From there,
experiment with various ways to change it. Try one page of copied layouts and
variations, and two pages of original layouts and variations.

Provide digital images (scans or photos) of your sketching practice. Please
take care to avoid shadows, bad color balance, etc. Include these in your
homework submission. Put the file(s) in a folder titled sketches, to be
included in your submission.

## Problem 2: HTML/CSS (25%)

Read Lessons 1--3 from "A Beginner's Guide to HTML & CSS" by Shay Howe:

* [Lesson 1: Terminology and syntax](http://learn.shayhowe.com/html-css/terminology-syntax-intro)
* [Lesson 2: Elements and semantics](http://learn.shayhowe.com/html-css/elements-semantics)
* [Lesson 3: Box model and positioning](http://learn.shayhowe.com/html-css/box-model)

Briefly answer the following questions in `hw5htmlcss.pdf`. A sentence or two
for each question will suffice.

1. At a high level, what is the purpose of HTML and CSS? How do the two differ?

2. What is the purpose of assigning a "class" to an HTML element? What is the
   difference between a "class" and an "id"? How would one select a division (div)
   element with class "box" using CSS?

3. List 5 different HTML elements and provide a short description of the
   function of each.

4. What is the difference between margin and padding?

5. Consider the Gmail Inbox interface. How is the site functionally divided?
   Create a nested list representing this functional division. Don't worry about
   extremely fine details; this should help you start:

        page
          top bar
            links to various Google sites
		  header bar
            left side
			  Google logo
			  search bar
			  search button

## Problem 3: Implementing a Layout (50%)

It's time to start working with HTML and CSS! Your task for this problem is to
choose a website and reimplement a basic, non-functional version of its user
interface (i.e., its aesthetic appearance). You are welcome to choose Gmail, or
you may choose another website that is of similar visual complexity (e.g., a
Wikipedia article, Piazza). Your implementation need not be functional in any
way (buttons must not be clickable, search bars must not work, there must not
be dynamically loaded data, etc.), and you do not need to worry about images.
The intention of the task is simply to familiarize yourself with HTML and CSS,
particularly with respect to positioning elements on the page.

In terms of detail, don't worry about implementing every last visual element
and replicating the site exactly - just be sure to implement all major details
(e.g. approximate placement, colors, etc.) and show that you understand how to
position and format elements as necessary. For data that is normally dynamic
(e.g., the list of emails in the Gmail Inbox), just include a few static
examples by hard-coding them into your HTML.

You should submit two files for this problem in a folder called website:
index.html and style.css (make sure your HTML file correctly links to your CSS
file!). We have included two sample files - sample_index.html and
sample_style.css - which you may use as templates if you wish. Make sure to
validate your HTML with <http://validator.w3.org/> and your CSS with
<http://jigsaw.w3.org/css-validator>.

Many external resources are also available to help you. Especially if you
haven't worked with HTML and CSS before, you are encouraged to skim through the
other Lessons of "A Beginner's Guide to HTML & CSS" (see Problem 2) for
sections that may be of use. w3schools.com also provides extensive
documentation of HTML elements, CSS properties, etc.

# Submitting

Your submission should be in `hw5.zip` and include the
following items:

1. Folder titled sketches containing your sketch scans or photos.
2. Answers to questions in `hw5htmlcss.pdf`.
3. Folder titled `website` containing `index.html` and `style.css`.
