#**Project 1 - Finding Lane Lines on the Road** 

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />
This project was written during the course of UDACity's Self Driving Car NanoDegree Program.


Overview
--- Python 3.6

The purpose of this project is to take in an image or video append red markings on the areas to denote Lane Lines a car will have to apprecaite in the near future.

The main source code (python 3.6) can be found in the file P1.ipynb. Please note that this is a Jupiter Notebook file, that includes inline annotations. The Python code can be extracted from this file, and run in a standalone file just fine. If you would like advice on how to set up jupiter notebook, please contact me at John.Moody@Ieee.org.

The program takes in images from test_images and outputs to test_images_output (go figure?)
The program takes in Named Videos from test_videos and outputs to test_videos_output. Note, the values for the videos in test_video are hard coded, if you would like to adapt it to perform lane detection on any video in the test_videos file, please adapt it to do so in a similar form to how test_images are read.
Note* - You may run into a memory error when performing the processing on the second and third video. This happened to me as well, however only when running on my native machine. The code hit no memory errors when run in Jupyter notebook. More info can be found on jupyter notebook at the bottom of this README, or through contacting me if you wish.

The orriginal Github for this project can be found here [code](https://github.com/udacity/CarND-LaneLines-P1/blob/master/P1.ipynb)
The rubric for this project can be found here [project rubric](https://review.udacity.com/#!/rubrics/322/view)


Included Files
---
P1.ipynb - Source code in Jupyter Notebook form
Writeup - Relfections on this project
Writeup Template - Pre-reflection writeup
examples - ideal example outputs
test_images - images to test program on
test_images_output - output directory for test images post annotation
test_videos - videos to test program on
test_videos_output - output directory for test videos post annotation.







Extra Info for Jupyter Notebook and perfomring initial set up of environment.
---
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

## If you have already installed the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) you should be good to go!   If not, you should install the starter kit to get started on this project. ##

**Step 1:** Set up the [CarND Term1 Starter Kit](https://classroom.udacity.com/nanodegrees/nd013/parts/fbf77062-5703-404e-b60c-95b78b2f3f9e/modules/83ec35ee-1e02-48a5-bdb7-d244bd47c2dc/lessons/8c82408b-a217-4d09-b81d-1bda4c6380ef/concepts/4f1870e0-3849-43e4-b670-12e6f2d4b7a7) if you haven't already.

**Step 2:** Open the code in a Jupyter Notebook

You will complete the project code in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out <A HREF="https://www.packtpub.com/books/content/basics-jupyter-notebook-and-python" target="_blank">Cyrille Rossant's Basics of Jupyter Notebook and Python</A> to get started.

Jupyter is an Ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, use terminal to navigate to your project directory and then run the following command at the terminal prompt (be sure you've activated your Python 3 carnd-term1 environment as described in the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) installation instructions!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  


