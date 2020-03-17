# Colab Usage Tips

## Introduction

Colaboratory is a free Jupyter notebook environment that requires no setup and runs entirely in the cloud.

It supports free GPU running with python in clouds and contains really fast GPU clusters with K80 and T4 (Faster than V100)!

With Colaboratory you can write and execute code, save and share your analyses, and access powerful computing resources, all for free from your browser.

The usage of Colab is well described in the following tutorial page down below. Some useful tips will be described in the following sections.

Reference: [https://colab.research.google.com/notebooks/welcome.ipynb](https://colab.research.google.com/notebooks/welcome.ipynb)

<img src="../../images/image1.png" width="500">

## Usage of Colab

1. (**Important!**) Link Google drive to upload images or documents.

1.1 Login google drive

1.2 Mount google drive to your Google GPU server.

~~~~
from google.colab import drive
drive.mount('/content/gdrive')
~~~~

1.3 Change directory to your default notebook root path.

~~~~
import os
os.chdir("/content/gdrive/My Drive/Colab Notebooks/{YOUR_DIR}")
~~~~

2.Open a New notebook and write scripts similar to the Jupyter Notebook by using IPython programming.

e.g. check whether GPU is available:

~~~~
import torch
print(torch.cuda.is_available())
~~~~

Usually, if it is not available, please do the following step to enable the GPU.

3.(**Important!**) Make sure the GPU is on in the Edit -> Notebook Settings -> Hardware Accelerator (GPU)!

<img src="../../images/image2.png" width="300">
<img src="../../images/image3.png" width="500">


Then, the program can be easily run with GPU by clicking the triangle run button at the top.

4.(**Optional**) The .py program can also be easily run by typing:

~~~~
! python example.py
~~~~

inline in the notebook by adding a '!' before the shell commands.

After uploading all the training data, just do

~~~~
! pwd
~~~~

to see and change the working directory to run.


## Good Colab Example: 

**CVAE with MNIST dataset**: [https://colab.research.google.com/github/tensorflow/docs/blob/master/site/en/tutorials/generative/cvae.ipynb](https://colab.research.google.com/github/tensorflow/docs/blob/master/site/en/tutorials/generative/cvae.ipynb])

