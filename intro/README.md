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

- The `train.py` and `test.py` files are the main scripts for train and test DL models (indipendentely from the actual models).

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


