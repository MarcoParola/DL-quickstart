# Introduction

This guide aims to provide a roadmap for setting up your deep learning project environment. Whether you are new to deep learning or looking to streamline your workflow, this document will help you get started quickly and efficiently.

## Programming Language

Use [Python](https://www.python.org/) as the primary programming language for your deep learning project. Open your terminal and check if it is installed:

```sh
python --version
```
If Python is not installed, on Linux you can prompt to install it
```sh
sudo apt install python3
```
On windows, you can download the .exe from the [official web site](https://www.python.org/downloads/) and follow the instruction.


## Project strutcure

The following schema summarize the project structure of the thesis project. Please note, not all these files must be tracked on GitHub.

```
project_root/
│
├── train.py
├── test.py
├── data/
│   ├── (data files go here)
│
├── src/
│   ├── models/
│   │   ├── (model files go here)
│   ├── datasets/
│   │   ├── (dataset files go here)
│   ├── utils.py
│
├── env/
│   ├── (virtual environment files and dependencies)
│
├── .git/
│   ├── (git version control files)
│
├── config/
│   ├── config.yaml
│   ├── (other config files in YAML format)
│
├── doc/
│   ├── README.md (technical documentation)
│   ├── (other doc files in .md format)
│
├── scripts/
│   ├── (non-training related scripts, e.g., for plotting or preprocessing)
│
├── requirements.txt
├── README.md
├── .gitignore
├── (other project files and folders)

```

- The `train.py` and `test.py` files are the main scripts for train and test DL models (indipentely from the actual models).

- The `data/` folder contains all your data files.

- `src/` folder contains subfolders for models and datasets, as well as a utils.py file for utility functions. 

- The `env/` folder is for the virtual environment. It's automatically generated, see the guide for [virtual environment](../virtual-env/README.md)

- `.git/` is for version control automatically generated when you clone the repo

- `config/` holds configuration files containing a config.yaml. 

- `doc/` for technical documentation with a README.md file

- `scripts/` for non-training and stand alone scripts e.g. for plot and pre-proessing

- `requirements.txt` for specifying dependencies

- `README.md` for general project information. 

- The `.gitignore` file is included to specify files or directories that should be ignored by version control.


## Virtual environment

Virtual environments are an important component of Python project. They provide an isolated, self-contained environment in which project-specific libraries can be installed without affecting the system-wide installation of Python. This ensures that different projects can have their own dependencies, versions and configurations, avoiding potential conflicts. Follow the [virtual environment guide](../virtual-env/README.md)


## Pip

pip is the default package installer for Python. It manages Python packages and dependencies from PyPI. PyPI is a repository of software packages developed and maintained by the Python community. pip interacts with PyPI to download and install packages. 

Installing a Package:
```sh
pip install package_name
```

Uninstalling a Package:
```sh
pip uninstall package_name
```

### Freezing
Freezing an environment is an important step in the context of software development, particularly when working collaboratively with others. 
Freezing an environment means recording the specific versions of software libraries and dependencies used in a project. This ensures that the project can be recreated at any time in the future with the exact same configuration, minimizing the risk of compatibility issues.
When multiple developers or teams work on a project, they must have a consistent development environment. Freezing the environment allows everyone to work with the same set of dependencies, reducing the possibility of errors or discrepancies between different configurations.

Freeze the environment at the end of the coding session, in case new dependencies have been installed, and put in requirements.txt:

```sh
pip freeze > requirements.txt
```

If you are using a repo or a project prepared by others, installs packages listed in a requirements file.
```sh
pip install -r requirements.txt
```
