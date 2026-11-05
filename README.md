# Wireless Communication Workshop

This repository contains the code and resources for the Wireless Communication Workshop done for the Digital Communication course of Communication Engineering Master Degree at University of Pisa.

## Workshop Materials

- [Workshop Slides](https://docs.google.com/presentation/d/1DahXnPQVf465QPkwZgq8kIFCXBrltOvENReyAysGAZE/edit?usp=sharing)

The Jupyter notebooks to work with are in `2026_wirelesscomms` folder.
The notebook `raytracer_channel.ipynb` is the complete version while the `raytracer_channel_students.ipynb` is the version to compile, given to the students during the lecture.

## Hardware setup
If working with Windows and CPU, Sionna RT needs one additional hardware-dependent setup step. Its Mitsuba backend supports Windows, but CPU execution requires LLVM installed separately.

So, if you have a Windows PCs and will use the CPU:
- Install LLVM using the official Windows installer linked from [DrJit's releases](https://github.com/llvm/llvm-project/releases/) (more info in [Dr.Jit's instructions](https://drjit.readthedocs.io/en/stable/what.html)).

## Code installation
To properly work, each PC should have installed a Python interpreter. Then a virtual environment with the required packages can be created using the following commands on a PowerShell:
```
cd C:\Users\SI6\Desktop\comm-workshops
 
py -m venv .venv

.\.venv\Scripts\python.exe -m pip install --upgrade pip

.\.venv\Scripts\python.exe -m pip install -r .\requirements.txt
```

Then, JupyterLab notebook can be launched through
```
.\.venv\Scripts\python.exe -m jupyterlab
```
(If the browser does not open automatically, please navigate to the http://localhost printed by the command in your web browser.)
