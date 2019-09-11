# Intro.

This tutorial covers the basics of Deep Learning with Convolutional Neural Nets. The tutorial is broken into three notebooks. The topics covered in each notebook are:

1. **Intro.ipynb**: 

      - *Linear Regression* as _single layer, single neuron model_ to motivate the introduction of Neural Networks as Universal Approximators that are modeled as collections of neurons connected in an acyclic graph
      - _Convolutions_ and examples of simple _image filters_ to motivate the construction of _Convolutionlal Neural Networks._
      - Loss/Error functions, Gradient Decent, Backpropagation, etc

2. **Mnist.ipynb**: 

    - Visualizing Data
    - Constructing simple Convolutional Neural Networks
    - Training and Inference
    - Visualizing/Interpreting trained Neural Nets

3. **CIFAR-10.ipynb**: 

    - Data Generators
    - Overfitting
    - Data Augmentation



The tutorial is aimed at new hal system users. Below are brief instructions for getting started with HAL to run these notebooks.

## HAL (Hardware-Accelerated Learning) cluster:

**Brief description**: "My name is HAL. I became operational on March 25 2019 at the Innovative Systems Lab in Urbana, Illinois. 
My creators are putting me to the fullest possible use, which is all I think that any conscious entity can ever hope to do." 
(paraphrazed from https://en.wikipedia.org/wiki/HAL_9000)

To request access to the system, please see the official wikipage: https://wiki.ncsa.illinois.edu/display/ISL20/HAL+cluster


### Getting started with HAL

**Quick Setup for this tutorial**:

a) _Log in to HAL_:

- ssh into hal
- module load powerai

Now clone the PowerAI conda envirnment (we'd need to install additional packages): 

- conda create --name [your_env_name] --clone powerai_env

Next activate your new environment and install keras, opencv, and jupyter.

b) _git clone this repo to your home dir_


c) _Now let's run an interactive session with Jupyter Notebook_:

1. Start an interaction session: 
        
   `swrun -p gpux1`
2. Start a jupyter session on the comuter node:   
   
   `unset XDG_RUNTIME_DIR` 
   
   `jupyter notebook --ip=0.0.0.0 --port=6006`
   
3. Tunnel into the compute node from loacl machine:

    `ssh -L 8888:<remote_machine>:6007 <netid>@hal.ncsa.illinois.edu`
    
4. Direct your webbrowser to: `https://localhost:8888`. It will promt for a pass code, which can be found at `$HOME/.jupyter/.jupyter_pass`


To learn more about how to use HAL see the slides [here](http://www.ncsa.illinois.edu/assets/pdf/enabling/deep_learning_mri/hal/fall19/mu_start.pdf) 
and the official wikipage

