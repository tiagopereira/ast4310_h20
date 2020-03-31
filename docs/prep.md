# Preparation


## Software

To do the assignments you will need Python 3.x with [Astropy](https://www.astropy.org/), plus Jupyter and many other dependencies of these packages.

**All the required software is already installed** in the Institute's Linux machines, to which you can connect to. See the  [guide](https://www.mn.uio.no/astro/english/services/it/help/programming/using-python.html) on how to use Python at ITA.

!!! info
    If you have problems installing the software, you can, as a last resort, run the notebooks from a cloud-based solution via Binder. This has its own issues (e.g. Binder being unavailable, timeouts after 10 minutes of inactivity, etc.), so be sure to save frequently ("Save" and then download to your computer). Here's the binder link: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ita-solar/ast4310/master?urlpath=lab/tree/notebooks).

### Installing in your own laptop

You can also install the software in your laptop, which may be a more convenient option. The easiest way to do this is using the [miniconda](https://conda.io/miniconda.html) or [Anaconda](https://www.anaconda.com/download/) Python distributions (*python 3.x versions*). Miniconda is recommended because it is a smaller download, but Anaconda works just as well if you already have it or are more familiar with it.

Once you have conda installed (either a new install or an older version), the recommended way to install the packages is to create a new enviroment (we'll call it `ast4310`) to ensure you have the most recent versions. You can do this by:

``` bash
conda create -n ast4310 -c conda-forge --yes python=3.7 jupyterlab sunpy ipympl bqplot nodejs
```

This will download about 140 MB and install all the needed dependencies. Next, you need to activate this environment:

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

### Testing installation

To make sure you have all necessary software ready, start Jupyterlab from the terminal (after activating the `ast4310` environment):

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

## Repository for materials

The assignment and tutorial materials are available on a [Github repository](https://github.com/ita-solar/ast4310). Please clone the repository into a directory of your choice:

```bash
git clone https://github.com/ITA-Solar/ast4310.git
```

This will create a directory `ast4310`. In the terminal, go to that directory and then start jupyter lab.
