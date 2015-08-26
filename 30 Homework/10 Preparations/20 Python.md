# Installing Python and the pattern library

About the version numbers of Python. There are currently two flavors of the
Python language, Python 2 and Python 3. For this class (and currently in most
science and business) Python 3 is not used. We require that you install version
2.7.? of Python. (Note that there are real incompatibilities between Python 2
and python 3, so installing the wrong one will break the most Python exercises
in this course.)

If you are a Windows user and have no pre-existing Python installation,
we recommend that you install 
[Python(x, y)](http://code.google.com/p/pythonxy/). This distribution includes
Python 2.7 (the version we use of Python comes with all common scientific
libraries (and hence saves you a lot of trouble in case you need Numpy, Scipy
or Matplotlib later).

For users of OS X, you already have Python so you need to check which version.
You do this by opening a Terminal (included in every Mac) and typing `python`
followed by pressing return. This will start Python, and if your version of Mac
OS X is recent enough you will have Python 2.7 already. If you don't have
Python 2.7, you should install it (i.e. download it from the
[Python](http://www.python.org) and install it).

If you are using a version of Linux, Python is probably already installed and
if it is not you can install it through the package manager of your Linux
distribution.

Once you successfully installed python you will be able to run python from your
command line. On Windows you can get a command line by starting the "Command
Prompt" and on a Mac by starting the "Terminal". For Linux you should also look
for the terminal (emulator) program.

Starting python should look something like this:

	~$ python
	Python 2.7.3 (default, Sep 26 2012, 21:51:14)
	[GCC 4.7.2] on linux2
	Type "help", "copyright", "credits" or "license" for more information.
	>>>

## Installing the Pattern Library

The Pattern library is a library that supports web­scraping and interfaces to
many streaming APIs. To install pattern go to their website and follow the
instructions. There you can download the library in a zip file. Simply extract
this zip, open a terminal in the directory where the unpacked files are and
execute the command ( *from the command line, not from inside Python or IDLE* )

	~$ python setup.py install

This will run the script stored in "setup.py" which installs the library.

Make sure that you run this with administrator privileges (add `sudo` at the
front on Mac and Linux and use and Administrator command prompt on Windows)!
For details see the pattern website.

## Executing Python Code

Being an interpreted language, Python requires an interpreter to execute a
script. You’ve already executed a script for the pattern installation! The
interpreter is called by typing python at the command line. If a file is passed
as the first argument (e.g., `python myfile.py`), the interpreter will execute
the specified script. If no parameters are given, the interpreter will launch
in interactive mode where you can type individual commands one at a time.
Interactive mode is similar to using the prompt in Matlab in the sense that
variables can be created, functions can be called, etc. In general, most things
that can be done via script can be done in interactive mode. However, in
practice, scripts are more common.

Therefore the process is you edit a file, e.g., `hello_world.py` in the editor
of your choice (emacs, notepad++, or a comple IDE like PyDev) You run python
and give your script as a parameter. Here is a simple example.

	import math
	
	a=math.ceil(math.pow(3,2)*19)
	print "Hello World, and welcome to CS ", int(a), "!"

To get your feet wet with python go through this and this page of the python
tutorial and play around with strings, lists, control flow, functions, etc.

## Try if Pattern is correctly installed

Copy the following code to a script and run it with python:

	from pattern.web import Twitter, plaintext
	
	for tweet in Twitter().search('"more important than"', cached=False):
		print plaintext(tweet.description)

If you get output similar to this, everything is fine:

	$ python twitter_test.py
	RT @BillSimmons: I love when coaches decide that their gimmick "system" is
	more important than figuring out to put their best players in the best
	situation.
	RT @ri_zugg: Finally realizing that God is more important than everything
	else. #nowtoputittoplay

Note that the content you see will be different, as you are getting real tweets
through the twitter API!

If this happens:

	$ python twitter_test.py Traceback (most recent call last):
	File "twitter_test.py", line 1, in <module>
		from pattern.web import Twitter, plaintext
	File "/home/cs171/twitter_test.py", line 1, in <module>
		from pattern.web import Twitter, plaintext
	ImportError: No module named web

then python can't find you pattern modules. There are several fixes described
on the pattern start site. The easiest one is to grab the "pattern" folder from
the zip and put it in the same directory as your python script. If you’re still
having trouble getting things working just ask for help.
