### Conda:
Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux.
### Anaconda:
Anaconda is a free and open-source distribution of the Python and R programming languages for scientific computing, that aims to simplify package management and deployment.
### Package Manager: 
Package managers are used to install libraries and other software on your computer. `pip` is the default package manager for Python libraries. Conda is similar to pip except that the available packages
are focused around data science while pip is for general use. However, conda is not Python specific like pip is, it can also install non-Python packages.
It is a package manager for any software stack. Conda installs precompiled packages. For example, the Anaconda distribution comes with Numpy, Scipy and Scikit-learn compiled with the MKL library,
speeding up various math operations. 
### Environment:
Along with managing packages, Conda is also a virtual environment manager. It's similar to virtualenv and pyenv, other popular environment managers.
Environments allow you to separate and isolate the packages you are using for different projects.
### Dependecies:
You can also export the list of packages in an environment to a file, then include that file with your code. This allows other people to easily load all the dependencies for your code.
Pip has similar functionality with `pip freeze > requirements.txt`.
### Packages:
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
#### NOTE:
*  To leave the environment, type `conda deactivate` (on OSX/Linux). On Windows, use `deactivate`.
* `conda activate` and `conda deactivate` only work on conda 4.6 and later versions. For conda versions prior to 4.6, run `activate` or `deactivate` (on Windows), `source activate` or `source deactivate` (on OSX/Linux).
* Command would you use to create an environment named data installed with Python 3.6, numpy, and pandas -
`conda create -n data python=3.6 numpy pandas`

