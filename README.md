# Intro to Machine Learning - Pattern Recognition for Fun & Profit

[![Known Vulnerabilities](http://snyk.io/test/github/mramshaw/Intro-to-ML/badge.svg?style=plastic&targetFile=requirements.txt)](http://snyk.io/test/github/mramshaw/Intro-to-ML?style=plastic&targetFile=requirements.txt)

The table of contents is as follows:

* [Overview](#Overview)
* [Prerequisites](#prerequisites)
* [scikit-learn](#scikit-learn)
* [Libraries](#libraries)
    * [Numpy](#numpy)
    * [Matplotlib / Seaborn](#matplotlib--seaborn)
    * [StatsModels](#statsmodels)
* [requirements.txt](#requirementstxt)
* [TODO](#todo)
* [Credits](#credits)
* [Alternatives](#alternatives)
* [Data Cleaning](#data-cleaning)
* [Quick Hits](#quick-hits)
* [End to End](#end-to-end)
* [Tools](#tools)

## Overview

This is a nice free introduction to Machine Learning with Python.

![xkcd](http://imgs.xkcd.com/comics/machine_learning.png)

Here is how the folks at
[nVidia](http://blogs.nvidia.com/blog/2016/07/29/whats-difference-artificial-intelligence-machine-learning-deep-learning-ai/)
see the relationship between Artifical Intelligence, Machine Learning and Deep Learning:

![AI_versus_ML_versus_Deep_Learning](/images/Deep_Learning_Icons_R5_PNG.jpg.png)

Towards the beginning of my career, I was interested in AI and joined a society founded
by [Donald Michie](http://www.theguardian.com/science/2007/jul/10/uk.obituaries1) - who
was then at the University of Edinburgh. I wonder how much things have progressed since
then?

Machine Learning is hot right now, and of course the cloud providers have noticed.

Here is Google's Cloud offering:

        http://cloud.google.com/products/machine-learning/

For a more sombre view of things, the following article is worth reading:

        http://www.cio.com/article/3223191/artificial-intelligence/a-practical-guide-to-machine-learning-in-business.html

## Prerequisites

[Chris Manning](http://profiles.stanford.edu/chris-manning), Stanford, 3 Apr 2017:

> "Essentially, Python has just become the [lingua franca](http://en.wikipedia.org/wiki/Lingua_franca) of nearly all the
> deep learning toolkits, so that seems the thing to use."

        http://youtu.be/OQQ-W_63UgQ?list=PL3FW7Lu3i5Jsnh1rnUwq_TcylNr7EkRe6&t=2102

For an explanation of why Python (as contrasted with other languages) is a good choice for
[Natural language processing](http://en.wikipedia.org/wiki/Natural_language_processing)
the following link is worth a look:

        http://www.nltk.org/book_1ed/ch00-extras.html

1. Python (Python 2 support has been dropped from a number of projects, so use Python 3)

2. `pip` or possibly `pip3` (if using Python 2 __and__ Python 3)

`pip` (or `pip3`) is the Package manager for Python, much as `npm` is the package manager
for the [Node.js](http://nodejs.org/) platform.

## scikit-learn

The course uses this library, which it refers to as `sklearn`.

The latest version may be found here:

        http://scikit-learn.org/stable/

To install this library in multi-user mode (not recommended) with `pip` (replace with `pip3` if using Python 3):

        pip install -U scikit-learn

To install this library in single-user mode (recommended) with `pip` (replace with `pip3` if using Python 3):

        pip install --user scikit-learn

## Libraries

It's not really possible to do much of anything in Python without additional libraries.

Essential libraries include:

* [NumPy](http://www.numpy.org/)
* [SciPy](http://www.scipy.org/index.html)

Useful optional libraries include:

* [matplotlib](http://matplotlib.org/)
* [nltk](http://www.nltk.org/)
* [pandas](http://pandas.pydata.org/)

Verify library presence and version with `pip` as with `scikit-learn`:

    pip list --format=freeze | grep numpy

[Replace `numpy` above as necessary.]

Or verify library presence and version with Python:

    python -c "import numpy as im; print(im.__version__)"

[Likewise replace `numpy` above as necessary.]

Or use `try_import.py` for multiple libraries as shown:

```bash
$ python try_import.py numpy scipy sklearn keras pytorch
"numpy" was imported
"scipy" was imported
"sklearn" was imported
Using TensorFlow backend.
"keras" was imported
"pytorch" could not be imported - try "pip install --user pytorch"
$
```

Install the library with `pip` (either multi-user or single-user) as with `scikit-learn` above.

#### Numpy

NumPy allows for a nice performance optimization called __single instruction, multiple data__, or
[SIMD](http://en.wikipedia.org/wiki/SIMD).

Basically, this allows for vector or matrix handling (compare 'vectors\ pt1.py' to 'vectors\ pt2.py').

#### Matplotlib / Seaborn

Matplotlib is great for plotting variables, but can be very low-level.

To make these graphs look a little better, check out my [No More Blue](http://github.com/mramshaw/No_More_Blue) repo.

Or - for a higher-level library - check out [Seaborn](http://seaborn.pydata.org).

[Seaborn will greatly simplify a number of difficult `matplotlib` graphing exercises.]

#### StatsModels

Although not used in this course, [StatsModels](http://www.statsmodels.org/stable/index.html) is also worth a look.

It provides classes and functions for the estimation of many different statistical models, as well as for conducting
statistical tests, and statistical data exploration.

Some __Seaborn__ functions will optionally use StatsModels if it is installed.

## requirements.txt

Of course, it's also possible (as with __npm__ or __composer__) to install all dependencies in one fell swoop (probably a _best practice_).

Simply list the dependencies in a file (for example `requirements` or `requirements.txt`) and install from it:

        pip install --user -r requirements.txt

[Note the `--user` option, which may be omitted for a Global install, also the `-r` option to specify an input file.]

## TODO

- [ ] Finish course
- [x] Update Quick Hit links to make them easier to navigate
- [ ] Update everything for the most recent (and secure) version of TensorFlow

## Credits

Based upon:

        http://www.udacity.com/course/intro-to-machine-learning--ud120

You can find an interview with co-author Katie Malone here:

        http://www.se-radio.net/2017/03/se-radio-episode-286-katie-malone-intro-to-machine-learning/

## Alternatives

The following look like interesting options too:

        http://web.stanford.edu/class/cs224n/

        http://openclassroom.stanford.edu/MainFolder/CoursePage.php?course=MachineLearning

## Data Cleaning

A ___lot___ (lets say three quarters) of a data scientist's time is spent massaging data.
Which is a pretty important (lets say _critically_ important) part of a data scientist's
job and not often discussed.

___Garbage in, garbage out.___

[Not to mention the (very expensive) computer time wasted.]

For a quick introduction to data cleaning with `numpy` and `pandas`, have a look at this
great tutorial:

    http://realpython.com/python-data-cleaning-numpy-pandas/

You can see my stab at it [here](http://github.com/mramshaw/Data-Cleaning).

For a more complicated example, check out my [ML with Missing Data](http://github.com/mramshaw/ML_with_Missing_Data) repo.

## Quick Hits

For an easy (and quick) introduction to the various Python tools and ML concepts:

        http://www.youtube.com/playlist?list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal

This series is from mid-2016 so there is a small amount of 'code rot', plus it seems to use
Python 2 rather than Python 3, but even so it's a quick and fun way to get a brief overview
of ML and the tools & techniques involved.

* [Machine Learning Recipes #1 (Hello World)](./Hello_World/)
* [Machine Learning Recipes #2 (Visualizing a Decision Tree)](./Iris/)
* [Machine Learning Recipes #3 (What Makes a Good Feature?)](./Features/)
* [Machine Learning Recipes #4 (Let's Write a Pipeline)](./Pipeline/)
* [Machine Learning Recipes #5 (Writing Our First Classifier)](./Custom_Classifier/)
* [Machine Learning Recipes #6 (Train an Image Classifier with TensorFlow for Poets)](./Image_Classifier/)
* [Machine Learning Recipes #7 (Classifying Handwritten Digits with TF.Learn)](./Handwriting_Classifier/)
* [Machine Learning Recipes #8 (Let's Write a Decision Tree Classifier from Scratch)](./Decision_Tree/)
* [Machine Learning Recipes #9 (Intro to Feature Engineering with TensorFlow)](./Feature_Engineering/)
* [Machine Learning Recipes #10 (Getting Started with Weka)](./WEKA/)

## End to End

For a deeper dive into the Iris dataset, check out my [ML with SciPy](http://github.com/mramshaw/ML_with_SciPy) repo.

This project shows a full end-to-end workflow.

## Tools

There are a number of tools, such as Python, IPython, and Jupyter Notebooks.

One website that gets a lot of mentions is [Anaconda](http://www.anaconda.com/):

    http://www.anaconda.com/download/
