# CUDA C/C++ on Colab
This repository contains a tutorial and a script to get started with CUDA C/C++ in Google Colab.

If you don't know what's Google Colaboratory, please visit the welcome page: https://colab.research.google.com 

## Create and configure a notebook
The first step is to create a new Colab notebook. You need to execute the following instructions only the first time, or everytime you want to create a new notebook.

1. Go to this link to create a Google Colab notebook:

https://colab.research.google.com/#create=true

2. Then, change the runtime from CPU to GPU. To do so, click on the top bar:
```
Runtime-> Change Runtime type-> Hardware accelerator-> GPU.
```
And, then, save.

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic0.png">
</p>

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic1.png">
</p>

Please, gain confidence with the basic commands and actions of Colab notebook (e.g., write and execute a Python command, upload a file in the notebook from your computer).

## Compile and Execute a CUDA program
The commands to compile and execute a CUDA program are the standard ones.

1. Install xterm, as shown here:

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic4.png">
</p>

* This will open up an interactive terminal, which you can use to compile, execute and handle your files normally (you basically have an Ubuntu machine available through this terminal). 

2. Either clone a repository in the xterm terminal, or upload a CUDA file in the notebook as shown in the following screenshots:

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic2.png">
</p>

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic3.png">
</p>

3. Compile the program:
```
nvcc my_cuda_appl.cu -o my_cuda_appl 
```

4. Run the program:
```
./my_cuda_appl
```

## Install CUDA libraries - If compiling/running executables does not work

Edit: The following stuff is required **only** if something does not work on your instance and you are unable to compile or execute source files for some reason.
You can, and should, skip this step if everything works for you, as removing and reinstalling the cuda environment takes approximately 5 minutes.

To remove and reinstall the CUDA libraries follow these steps:

1.  First, clone this repository in the session:
```
!git clone https://github.com/albertozeni/gpu_course_colab.git
```
2. Then, move in the downloaded folder:
```
cd gpu_course_colab
```
3. Run the CUDA installer script:
```
!bash install_cuda_colab.sh
```
4. And, finally, move in the main directory:
```
cd ..
```