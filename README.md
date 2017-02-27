PySD
====

### Using pysd from source

If you are having trouble with nested functions but you don't want to change your
model, these instructions are for you. The instructions will use a slightly less
stable yet much more current version of pysd that is able to handle those nested
functions, no model changes required.

Requirements: Python 3.5 or 3.6 *Note: I have this version: Python 3.6.0 :: Anaconda 4.3.0 (x86_64)*

Step 1: Uninstall existing pysd

```shell
pip uninstall pysd
```

Step 2: Install yapf

```shell
pip install yapf
```

Step 3: Download pysd source from github. You can do this using a zip file or
by cloning, whichever you are comfortable with. The repository is a forked
version of pysd, with a change in the installation process to make it work.

Below is the link you can use to either download a zip of the source code or
clone directly:

https://github.com/eebart/pysd

As with all activities involving programming, be sure to have no spaces in the
directory path leading to the final location or file names in general. Sometimes
spaces cause weird or annoying problems, and it's just a generally good policy
to avoid spaces in file names :). If you don't know what it means to git clone,
just download the zip.

```shell
cd /your/desired/directory
git clone https://github.com/eebart/pysd
    OR
unzip pysd.zip

python setup.py install
```

Step 4: Continue programming as before! You should hopefully have no more errors
with nested functions (but not necessarily no more errors in general...)!

## Original pysd Documentation

[![Coverage Status](https://coveralls.io/repos/github/JamesPHoughton/pysd/badge.svg?branch=master)](https://coveralls.io/github/JamesPHoughton/pysd?branch=master)
[![Code Health](https://landscape.io/github/JamesPHoughton/pysd/master/landscape.svg?style=flat)](https://landscape.io/github/JamesPHoughton/pysd/master)
[![Build Status](https://travis-ci.org/JamesPHoughton/pysd.svg?branch=master)](https://travis-ci.org/JamesPHoughton/pysd)

Simulating System Dynamics Models in Python

This project is a simple library for running [System Dynamics](http://en.wikipedia.org/wiki/System_dynamics) models in python, with the purpose of improving integration of *Big Data* and *Machine Learning* into the SD workflow.

### Resources
See the [project documentation](http://pysd.readthedocs.org/) for information about:

- [Installation](http://pysd.readthedocs.org/en/latest/installation.html)
- [Basic Usage](http://pysd.readthedocs.org/en/latest/basic_usage.html)
- [Function Reference](http://pysd.readthedocs.org/en/latest/functions.html)

For standard methods for data analysis with SD models, see the  [PySD Cookbook](https://github.com/JamesPHoughton/PySD-Cookbook), containing (for example):

- [Model Fitting](http://nbviewer.ipython.org/github/JamesPHoughton/PySD-Cookbook/blob/master/2_1_Fitting_with_Optimization.ipynb)
- [Surrogating model components with machine learning regressions](http://nbviewer.ipython.org/github/JamesPHoughton/PySD-Cookbook/blob/master/6_1_Surrogating_with_regression.ipynb)
- [Multi-Scale geographic comparison of model predictions](http://nbviewer.ipython.org/github/JamesPHoughton/PySD-Cookbook/blob/master/Exploring%20models%20across%20geographic%20scales.ipynb)

If you use PySD in any published work, consider citing the [PySD Introductory Paper](https://github.com/JamesPHoughton/pysd/blob/master/docs/PySD%20Intro%20Paper%20Preprint.pdf):

>Houghton, James; Siegel, Michael. "Advanced data analytics for system dynamics models using PySD." *Proceedings of the 33rd International Conference of the System Dynamics Society.* 2015.


### Why create a new SD simulation engine?

There are a number of great SD programs out there ([Vensim](http://vensim.com/), [iThink](http://www.iseesystems.com/Softwares/Business/ithinkSoftware.aspx), [AnyLogic](http://www.anylogic.com/system-dynamics), [Insight Maker](http://insightmaker.com/), and [others](http://en.wikipedia.org/wiki/List_of_system_dynamics_software)). In order not to waste our effort, or fall victim to the [Not-Invented-Here](http://en.wikipedia.org/wiki/Not_invented_here) fallacy, we should have a very good reason for starting a new project.

That reason is this: There is a whole world of computational tools being developed in the larger data science community. **System dynamicists should directly use the tools that other people are building, instead of replicating their functionality in SD specific software.** The best way to do this is to bring specific SD functionality to the domain where those other tools are being developed.

This approach allows SD modelers to take advantage of the most recent developments in data science, and focus our efforts on improving the part of the stack that is unique to System Dynamics modeling.

### Cloning this repository

If you'd like to work with this repository directly, you'll need to use a recursive git checkout in order to properly load the test suite (sorry..)

The command should be something like:
```shell
git clone --recursive https://github.com/JamesPHoughton/pysd.git
```
