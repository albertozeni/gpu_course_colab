# CUDA C/C++ on Colab
Repository with useful scripts for CUDA C/C++ on Colab
## Getting started
Go to this link to create a google Colab notebook

https://colab.research.google.com/#create=true

Then after having created the notebook we need to change the runtime from CPU to GPU.

To do so click on the top bar:
```
Runtime-> Change Runtime type-> Hardware accelerator-> GPU.
```
And then save.

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/master/media/pic0.png">
</p>

<p align="center">
  <img width="639" height="223" src="https://github.com/albertozeni/gpu_course_colab/blob/master/media/pic1.png">
</p>

Once saved you will need to upload the script file contained in this folder and execute it.

As a general rule, most commands that have an exclamation point at the start (`!`) will be interpreted as OS commands instead of Python.

Remeber to execute each command after typing it by pressing the start symbol on each code box. For the sake of simplicity I highly advise you to create a new box for each of the commands below.

First clone this repository on the session by typing:
```
!git clone https://github.com/albertozeni/gpu_course_colab.git
```
Then navigate inside the repo by typing:
```
%cd gpu_course_colab
```
Once you reached this point you can run the cuda installer script by typing:
```
!bash install_cuda_colab.sh
```
And finally you can go back a level so that you are outside of this repo directory
```
%cd ..
```
After doing this you will be able to execute most commands on the current instance of Colab.
Remember that you will need to rexecute the script everytime you restart the runtime.
To start programming with cuda you can do the same operations you will perform on a regular command line, just remember to type `!` before every command launched on Colab.