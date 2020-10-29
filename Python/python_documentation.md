### Conda:
Conda is an open source command-line utility for package management system and environment management system that runs on Windows, macOS and Linux.
### Anaconda:
Anaconda is a free and open-source distribution of the Python and R packages especially for data science, that aims to simplify package management and deployment.

Anaconda is a program to manage (install, upgrade, or uninstall) packages and environments to use with Python. It's simple to install packages with Anaconda and create virtual environments to work on multiple projects conveniently.

### Package Manager: 
Package managers are used to install libraries and other software on your computer. `pip` is the default package manager for Python libraries. Conda is similar to pip except that the available packages
are focused around data science while pip is for general use. However, conda is not Python specific like pip is, it can also install non-Python packages.
It is a package manager for any software stack. Conda installs precompiled packages. For example, the Anaconda distribution comes with Numpy, Scipy and Scikit-learn compiled with the MKL library, speeding up various math operations. 

### Environment:
Along with managing packages, Conda is also a virtual environment manager. It's similar to virtualenv and pyenv, other popular environment managers.
Environments allow you to separate and isolate the packages you are using for different projects.

- A Python environment comprises a particular version of each of the following:

  - Python interpreter,
  - Python-packages, and
  - The utility scripts, such as pip.

### Dependecies:
You can also export the list of packages in an environment to a file, then include that file with your code. This allows other people to easily load all the dependencies for your code.
Pip has similar functionality with `pip freeze > requirements.txt`.

### Packages:
A package is a bunch of modules, where each module consists of a set of classes and function definitions. After installing a particular package, you can `import` and use the functions defined in that package.

#### Conda & Pip: 
The `conda` and `pip` both are the Python package managers. Package managers are used to installing libraries and other software on your computer. pip is the default package manager for Python libraries, whereas conda focuses only on the packages that are available from the Anaconda distribution.

**What to use?**
- The available packages available from the Anaconda distribution in conda focus on data science, whereas pip is for general use. Conda installs precompiled packages. For example, the Anaconda distribution comes with Numpy, Scipy, and Scikit-learn compiled with the MKL library, speeding up various math operations.
- Pip can install both Python and non-Python packages. Pip can install any package listed on the Python Package Index (PyPI).

Some usefull commands are given below -

* `conda upgrade --all` -  running `conda upgrade conda` should not be necessary because --all
includes the conda package itself, but some users have encountered errors without it.
If you are seeing the following "conda command not found" and are using ZShell, you have to do the following:

Add `export PATH="/Users/username/anaconda/bin:$PATH"` to your .zsh_config file.
* `conda install package_name` - To install particular package.
* `conda install numpy scipy pandas` - To install multiple packages at the same time.
* `conda install numpy=1.10` - To install package with specific version.
* `conda remove package_name` - To uninstall package.
* `conda update package_name` - To update package.
* `conda search *search_term*` - To search for a particular package. Example `conda search '*beautifulsoup*'`
#### NOTE:
Conda also automatically installs dependencies for you. For example `scipy` depends on `numpy`, it uses and requires numpy. If you 
install just `scipy` (`conda install scipy`), Conda will also install `numpy` if it isn't already installed.

### Managing Environment:
Conda can be used to create environments to isolate your projects. Usefull comand are given below -
* `conda create -n env_name list of packages` - To create an environment. Here `-n env_name` sets the name of your environment (`-n` for name) and `list of packages` is the list of packages you want installed in the environment. For example, to create an environment named `my_env` and install `numpy` in it, type `conda create -n my_env numpy`.
* `conda create -n py3 python=3` - To create env with specific python version.
* `conda activate my_env` - To enter a created environment.
- `conda list` - To list installed packages under the current environment.
* `conda env export > environment.yaml` - To create a [yaml](https://yaml.org/) file that includes all the packages in the environment, so that one can create same environment using the same packages.
* `conda env create -f environment.yaml` - To create environment from `yaml` file.
* `conda env list` - To list all available environment. There will be an asterisk next to the environment you're currently in. The default environment, the environment used when you aren't in one, is called `base`.
* `conda env remove -n env_name` - To remove an environment.
#### NOTE:
*  To leave the environment, type `conda deactivate` (on OSX/Linux). On Windows, use `deactivate`.
* `conda activate` and `conda deactivate` only work on conda 4.6 and later versions. For conda versions prior to 4.6, run `activate` or `deactivate` (on Windows), `source activate` or `source deactivate` (on OSX/Linux).
* Command would you use to create an environment named data installed with Python 3.6, numpy, and pandas -
`conda create -n data python=3.6 numpy pandas`

### Jupyter(Julia, Python, R) Notebook:
 The notebook is a web application that allows you to combine explanatory text, math equations, code, and visualizations all in one easily sharable document. The central point is the notebook server. You connect to the server through your browser and the notebook is rendered as a web app. Code you write in the web app is sent through the server to the kernel. The kernel runs the code and sends it back to the server, then any output is rendered back in the browser. When you save the notebook, it is written to the server as a JSON file with a `.ipynb` file extension.
 #### Uses:
 Notebooks have quickly become an essential tool when working with data. You'll find them being used for data cleaning and exploration, visualization, machine learning, and big data analysis.
 #### Usefull command:
 * `jupyter nbconvert --to html notebook.ipynb` - To convert from `json` to `html` file.
 * `jupyter nbconvert notebook.ipynb --to slides` - To create slideshow from`json` notebook file.
 * `jupyter nbconvert notebook.ipynb --to slides --post serve` - To create slideshow and see immediately.
 * `jupyter nbconvert presentation.ipynb --to slides --template output-toggle.tpl --post serve` - To convert into slide with the given template.
 #### NOTE:
 * To install Jupyter Notebook use the following command - 
 `conda install jupyter notebook` or `pip install jupyter notebook`.
 * To start notebook enter `jupyter notebook` in terminal or console.
 * By default, the notebook server runs at `http://localhost:8888`. `localhost` means your computer and `8888` is the port the server is communicating on.
 * `conda install nb_conda` - To install Notebook Conda. If then you run the notebook server from a conda environment, you'll also have access to the "Conda" tab shown below. Here you can manage your environments from within Jupyter. You can create new environments, install packages, update packages, export environments and more.
 * Notebooks are also rendered automatically on GitHub. It’s a great feature that lets you easily share your work. [nbviewer](http://nbviewer.jupyter.org/)
 * Notebooks are a form of literate programming proposed by Donald Knuth in 1984. With literate programming, the documentation is written as a narrative alongside the code instead of sitting off by its own.
 * One can setup server on remote machine so that one can access notebooks from anywhere. [set up a server](https://jupyter-notebook.readthedocs.io/en/latest/public_server.html)
