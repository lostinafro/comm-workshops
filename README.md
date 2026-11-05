# Wireless Communication Workshop

This repository contains the code and resources for the Wireless Communication Workshop.

## Workshop Materials

- [Workshop Slides](https://example.com/slides)

The Jupyter notebook to compile is in `2026_wirelesscomms` folder.

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


### For me to check what is going on
Sionna RT needs one additional hardware-dependent setup step. Its Mitsuba backend supports Windows, but CPU execution requires LLVM installed separately; a requirements file alone does not install that system dependency. A supported NVIDIA GPU and driver provide another execution option. Sionna 2.2.0

For PCs that will use the CPU:
- Install LLVM using the official Windows installer linked from [Dr.Jit’s instructions](https://drjit.readthedocs.io/en/stable/what.html?utm_source=chatgpt.com).
- Ensure LLVM’s bin directory is on PATH, then restart the terminal.
- If Dr.Jit cannot locate it, set the DLL path before launching Jupyter:
```
$env:DRJIT_LIBLLVM_PATH = "C:\Program Files\LLVM\bin\LLVM-C.dll"
.\.venv\Scripts\python.exe -m jupyterlab
```
Adjust that path to the actual installation.

I need to test to one Windows PC first, then distribute the same Python version, dependency versions, and LLVM setup to the others.