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

## Virtual environment

Virtual environments are an important component of Python project. They provide an isolated, self-contained environment in which project-specific libraries can be installed without affecting the system-wide installation of Python. This ensures that different projects can have their own dependencies, versions and configurations, avoiding potential conflicts. 

`venv` is a module built into Python 3 that allows you to create lightweight virtual environments effortlessly. To create a virtual environment using venv, navigate to your project directory in the terminal and run the following commands:

```sh
python3 -m venv env
```

This creates a virtual environment named `env` in your project directory. Activate the virtual environment using:

On Windows:
```sh
.\venv\Scripts\activate
```

On macOS/Linux:
```sh
source venv/bin/activate
```

Once activated, the terminal prompt will change, indicating that you are now working within the virtual environment.  To deactivate the virtual environment, simply type deactivate in the terminal. 

```sh
deactivate
```

Alternatively, you can use Conda, an open-source package and environment management system that simplifies the process of installing, managing, and organizing software packages in various programming languages, including Python. It will not be covered in this guide

### Pip

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
