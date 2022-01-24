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

Please, gain confidence with the basic commands and actions of Colab notebook (e.g., write and execute a Python command, upload a file in the notebook from your computer). Moreover, you should know that:

* As a general rule, adding an exclamation point before any instruction (`!`) will force the notebook to interpret the instruction as OS commands instead of Python (Colab runs a Linux OS).


## Install CUDA libraries
Everytime you open the Colab notebook, you need to install CUDA libraries from scratch (It takes approximately 5 minutes).

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

## Compile and Execute a CUDA program
The commands to compile and execute a CUDA program are the standard ones.

1. Upload in the CUDA file in the notebook as show in the following screenshots
<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic2.png">
</p>

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/main/media/pic3.png">
</p>

2. Compile the program:
```
!nvcc my_cuda_appl.cu -o my_cuda_appl 
```

3. Run the program:
```
!./my_cuda_appl
```

Do note that outputs of printf calls executed in a kernel on the device are not displayed on screen.