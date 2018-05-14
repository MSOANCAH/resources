# Resources for the AI4Good Summer School #

Installation Guide
===================

## Requirements ##
Linux distributions, Windows 10 with Bash (Anniversary update) or recent Mac OS

There are two options for the tutorials:
- 1. Do all them tutorials in Colab! (recommended)
- 2. Install everything on your computer. While this is not necessary for the notebooks, it will be for your project.

## Using Colab ##
The quickest and easiest way to go through these notebooks is with Colab.
[Colab](https://colab.research.google.com/) is an open research project from Google allowing you to work with a cloud interface that is very similar to Jupyter, using Google's free computing resources.
No installation required! Simply clone this repo and upload the notebooks to [Colab](https://colab.research.google.com/).

### Linux instructions ###

1. If Conda is already installed, you can update it with

    `conda update conda`

* Otherwise, download Miniconda for Linux with python 3.6

  `wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh`

* Install Conda from the console bash:

  `bash Miniconda3-latest-Linux-x86_64.sh`


2. Create conda environment

    `conda create -n py36 python=3 jupyter matplotlib pandas`
    py36 is the environment name

3. Activate the virtual environment with

    `source activate py36`

    The last command must be run every time you open a new console to activate the Conda environment.

4. Install Pytorch:
  The following command lines installs the CPU version of Pytorch.

    - Linux:  `conda install pytorch-cpu torchvision -c pytorch`
    - Mac OS: `conda install pytorch torchvision -c pytorch`

    To install the GPU version of Pytorch run the following commands

    - Linux:  `conda install pytorch torchvision -c pytorch`
    - Mac OS: `conda install pytorch torchvision -c pytorch`
      MacOS Binaries dont support CUDA, install from source if CUDA is needed

    If you have any other requirement, please follow the instructions from the Pytorch official page [here](https://pytorch.org/)


5. Access a given directory and start jupyter
    `cd name; jupyter notebook`


6. A window should open in your browser. If not,  you can copy the URL that appears in the terminal into your browser to access the jupyter environment.

### Instructions for Windows ###

1. If Conda is already installed, you can update it with
    `conda update conda`

    Otherwise, download and install [Miniconda for Windows](https://conda.io/miniconda.html) with python 3.6  (exe installer)

2. Follow the aforementioned [Linux instructions](https://github.com/ai4socialgood/resources/blob/master/README.md#linux-instructions) from point 2


### Instructions for Mac OS ###

1. If Conda is already installed, you can update it with
  `conda update conda`

    Otherwise, download and install  [Miniconda for Mac OS](https://conda.io/miniconda.html) with python 3.6
    `wget https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh`

    Install Conda from the console bash:
    `bash Miniconda3-latest-MacOSX-x86_64.sh`

2. Follow the aforementioned [Linux instructions](https://github.com/ai4socialgood/resources/blob/master/README.md#linux-instructions) from point 2


Tutorials
===================
Tutorial on [Scientific computing with Numpy](http://cs231n.github.io/python-numpy-tutorial/)



Additional Resources
===================
- [Documentation on Conda](https://conda.io/docs/index.html)
- [PyTorch](https://pytorch.org/)
- [Documentation for Pytorch](https://pytorch.org/docs/stable/index.html)


FAQ
===================

* Q. The command `jupyter notebook` opens a browser, but displays an connexion error to the  Jupyter server.

  A. It is possible that the default port 8888 is unavailable. You can change the port manually with `jupyter notebook --port 8080 --no-browser`


* Q. Once conda installed, the Bash console does not find the conda environment

  A. For the Conda installation, you must accept the automatic modification of the .bashrc file that contains the paths. If not done, you need to add `export PATH="~/Miniconda3/bin :$PATH"` in the file called ~/.bashrc.

