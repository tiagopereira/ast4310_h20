# Software and Tools


## Programming environment

This course can be followed using one of two programming languages: Python or Julia. There are two versions for each project: one in Python, one in Julia. In classes, most of the explanations and examples will be given in Python, but it is also possible to replicate them in Julia if there is enough demand. The Python examples are more mature and have undergone more testing; moreover, the Python will normally be more responsive and easier to interact with in a notebook environment because of long Julia compilation times. However, the Julia versions will prove more versatile and faster in the computationally-heavier parts of later projects.

Students can either work from their personal laptops or from the linux machines at the Institute. It is recommended that all install the programming environment in their personal laptops to better participate in the classes; the Institute machines can be used for heavier computations.

**All the required software is already installed** in the Institute's Linux machines, to which you can connect to. See the  [guide](https://www.mn.uio.no/astro/english/services/it/help/programming/using-python.html) on how to use Python at ITA.

To install the programming environment in your laptop, see below.

!!! info
    If you have problems installing the software, you can, as a last resort, run the notebooks from a cloud-based solution via Binder. This has its own issues (e.g. Binder being unavailable, timeouts after 10 minutes of inactivity, etc.), so be sure to save frequently ("Save" and then download to your computer). Here's the binder link: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tiagopereira/ast4310/master?urlpath=lab/tree/notebooks).

## Installing the Python environment

To do the assignments you will need Python 3.8.x with [Astropy](https://www.astropy.org/), plus Jupyter and many other dependencies of these packages.

### Windows (using Docker)

The recommended way to get all the python packages working in Linux is to use [Docker](https://www.docker.com/). Docker runs a virtual Linux container alongside your operative system, in our case one that already has all the necessary packages installed. 

1. Start by [downloading Docker](https://docs.docker.com/get-docker/)
2. Install Docker (administrator priviledges are required)
3. Test your installation by opening a terminal window (Command Prompt or PowerShell) and entering:

```
> docker --version

Docker version 19.03.1
```

If you get a similar output to the above (version may vary), you should be good. Now you will need to download the Docker image "snowgum/astronomy-python":

```
> docker pull snowgum/astronomy-python

Unable to find image 'snowgum/astronomy-python:latest' locally
latest: Pulling from snowgum/astronomy-python
692c352adcf2: Pull complete
97058a342707: Pull complete
2821b8e766f4: Pull complete
(...)
```

This will be several hundreds of MB, so may take a while. You should now have a fully working Linux container with Jupyter lab, and many scientific python packages. You can start it from the terminal. *Be sure to navigate to the directory where you have the AST4310 notebooks*. Then, run:

```
> docker run --rm -p 8888:8888 -e JUPYTER_ENABLE_LAB=yes -v "%cd%":/home/jovyan/work snowgum/astronomy-python

```

!!! tip
    If you use `PowerShell` instead of the Command Prompt, you may have to replace the part `%cd%` with `$pwd`. Likewise if you run macOS or Linux, replace with `$PWD`.


This tells Docker to start running the container `snowgum/astronomy-python` and link the current directory to a directory called `work` inside the container. The output of the command above should show the messages from Jupyter starting. In particular, it should have a few lines such as:

```

    To access the notebook, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/nbserver-7-open.html
    Or copy and paste one of these URLs:
        http://cdd3b0fdf72f:8888/?token=ffa4fd380e9ece6fa12a63ad73b2a74bd5a2c4cbb01c95df
     or http://127.0.0.1:8888/?token=ffa4fd380e9ece6fa12a63ad73b2a74bd5a2c4cbb01c95df
```

Copy paste the second link (host 127.0.0.1) and open in your web browser. Jupyter lab should start.


### Linux or macOS

If you have Linux or macOS, the easiest way to get all the software is to use Docker image (see above). But it is also possible to install your python environment using conda, which will take up less space, be a bit faster, and is probably more useful if you want to keep using some of the packages later. 

To install python yourself, we recommend using [miniconda](https://conda.io/miniconda.html) or [Anaconda](https://www.anaconda.com/download/) Python distributions (*python 3.x versions*). Miniconda is recommended because it is a smaller download, but Anaconda works just as well if you already have it or are more familiar with it.

Once you have conda installed (either a new install or an older version), the recommended way to install the packages is to create a new enviroment (we'll call it `ast4310`) to ensure you have the most recent versions. You can do this by:

``` bash
conda create -n ast4310 -c conda-forge --yes python=3.8 jupyterlab sunpy ipympl bqplot nodejs
```

This will download and install the necessary packages and their ependencies. Next, you need to activate this environment:

``` bash
source activate ast4310
```

!!! warning
    Every time you want to use the newly installed python packages, you must ensure you are running from the `ast4310` environment. Once active, your prompt will start with `(ast4310)`. If you open a new terminal, you will need to activate the environment again.


For Jupyterlab, you will also need to install the extensions:

``` bash
jupyter labextension install @jupyter-widgets/jupyterlab-manager jupyter-matplotlib
jupyter lab build
```

A notebook is a document where you can combine text, images, and source code. If you are unfamiliar with Jupyter, there are [several](https://jupyter-notebook.readthedocs.io/en/stable/) [guides](https://www.youtube.com/watch?v=HW29067qVWk) and [tutorials](https://www.datacamp.com/community/tutorials/tutorial-jupyter-notebook). We recommend you use [Jupyterlab](https://jupyterlab.readthedocs.io/en/latest/), the next-generation version of Jupyter. But you can also use the classical notebook interface.

#### Testing installation

To make sure you have all necessary software ready, start Jupyterlab from the terminal (if using conda, activate the  `ast4310` environment):

```
jupyter lab
```

This will then open up a browser with the Jupyterlab launcher. Choose "Python 3" notebook, and it will start a new notebook. In the first cell enter the following and run:

``` python
from astropy import units
import matplotlib.pyplot as plt
```

!!! success
    If you got no error messages above, your installation is good and you are ready to start!

## Installing the Julia enviroment

To do the assignments you will need Julia 1.5.0 or above, plus Jupyter and a few extra packages. Julia itself is stabilising, but its packages are still changing quickly. It is recommended that you do a fresh install of all packages at the start of the semester, to ensure that all will work consistently with the examples.

### Windows 

!!! warning
    If you have a laptop with Windows, the recommended way to install all the packages is to use the Docker with an image that we will provide. This is not yet ready, but we are working on it and will update this page soon.

### Linux or macOS

If you have Linux or macOS, the easiest way to get all the software is to use Docker image (see above). But it is also possible to install your Julia environment manually. 

[Download Julia](https://julialang.org/downloads/) from the official web page and follow the install instructions for your system. Once that is done, start the Julia REPL and enter the package manager (press `]` key). Once there, install the necessary packages:

```  julia
(@v1.5) pkg> add IJulia Unitful UnitfulRecipes NumericalIntegration Interpolations PhysicalConstants FITSIO Plots LaTeXStrings pluto
```

Note that this will not install Jupyter. To install Jupyter, you will either need to install if via a python installation with conda (strongly recommended, see above). If you have done so, you will need to copy the Julia kernel to the Jupyter kernel directory (in Linux: `~/.local/share/jupyter/kernels`, in macOS: `~/Library/Jupyter/kernels/`). Another option to install Jupyter is from the REPL:

``` julia
using IJulia
notebook()
```

This will prompt you to install Jupyter via Conda.jl. 

## Text editor for sharing

If needed for remote teaching, we will use the text editor [Visual Studio Code](https://code.visualstudio.com/) and its extension [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) for remotely sharing a coding session. It is also recommended that you install the [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) or [Julia](https://github.com/julia-vscode/julia-vscode) extensions for VS Code.