# Simple Celebrity Classifier

### Summary
This project shows a simple image classification example based on a convolutional neural network.
It is alomst identical to the image classification example provided here 

      https://colab.research.google.com/github/pytorch/tutorials/blob/gh-pages/_downloads/4e865243430a47a00d551ca0579a6f6c/cifar10_tutorial.ipynb

as well as here:

      https://github.com/pytorch/tutorials/blob/main/beginner_source/blitz/cifar10_tutorial.py
      
      Copyright (c) 2017-2022, Pytorch contributors
      All rights reserved.
The images hereby, however, stem from a folder structure containing solely jpg files and do not originate from a specifically designed internal object.
Therefore, the images can be simply replaced by other ones.

### Motivation
There is of course a plethora of image classification examples. 
The idea of this project is to use a very simple and explanatory neural network framework for image classification of the CIFAR10 image data set and modify it in a way to use own image data sets.
For this purpose we chose a celebrity human face data set. The classifier developed here is far from perfect but allows for simple adjustments.


### Data sources 
The face image data source is provided by Simarpreet Singh and is located here:
https://www.kaggle.com/datasets/cybersimar08/face-recognition-dataset
licensed under CC0.

For simplicity images have been resized with a powershell script provided in the "Dataset" folder which is based 
on an image rescaling function provided in https://gist.github.com/someshinyobject/617bf00556bc43af87cd


### Install/run instructions:
1. Install python >= 3.11 and the packages denoted in requirements_working_configuration.txt preferably in a virtual environment as exemplarily shown for the windows command prompt:
```
      projectfolder:> python -m venv .venv
      projectfolder:> cd .venv\Scripts
      projectfolder\.venv\Scripts> .\activate.bat
      projectfolder\.venv\Scripts> cd ..\..
      projectfolder:> python -m pip install -r requirements_working_configuration.txt
```
      Within your project folder "projectfolder" use the "python" command as long as the virtual environment is activated
      (if not working with/on the project, the virtual environment should be deactivated by executing projectfolder\.venv\Scripts\deactivate.bat).

      Important note: If you are using requirements.txt (no package versions provided) instead of requirements_working_configuration.txt, make sure to install ipykernel before (python -m pip install ipykernel). The order seems important.

2. In the programming IDE select .venv\Scripts\python.exe as Kernel.

1. Run all code blocks in "simple_celebrity_classifier.ipynb"

### Files in the repository
```
.gitignore
Dataset
|-Facesmodified   # all images of celebrities are stored in separate subfolders
|-create_Facesmodified_folder.ps1      # powershell script for creating an image folder from a source and transforming images into smaller ones (here 32x32 pixels); each subfolder with images represents one class
README.md
requirements.txt                       # list of required packages
requirements_working_configuration.txt # list of packages covering a working configuration
simple_celebrity_classifier.ipynb      # main jupyter file
```
