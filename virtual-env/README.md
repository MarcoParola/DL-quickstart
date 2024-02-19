# Virtual environment



Virtual environments are an important component of Python project. They provide an isolated, self-contained environment in which project-specific libraries can be installed without affecting the system-wide installation of Python. This ensures that different projects can have their own dependencies, versions and configurations, avoiding potential conflicts. 

## venv

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

A requirements.txt file is a common convention in Python projects used to specify the dependencies required for the project to run. It contains a list of Python packages along with their version numbers. This file is used by package management tools (pip) to install the necessary dependencies for the project.

requirements.txt
```sh
numpy==1.21.3
pandas==1.3.4
matplotlib==3.4.3
```

Once activated the virtual environment:
```sh
pip install -r requirements.txt
```

Deactivate virtual environment:
```sh
deactivate
```

Remove virtual environment:
```sh
rm -rf venv/
```

The official guide can be found [here](https://docs.python.org/3/library/venv.html)

## Conda

An alternative to create a virtual enviroment is to use conda that allows you to choose and use a python version instead of exploiting the current installed one

### Installation of miniconda

1. Create a directory to install minicaonda in
```sh
mkdir -p ~/miniconda3
```

2. Download latest miniconda version
```sh
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
```

3. Run the install script
```sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
```

4. Delete the intall script
```sh
rm -rf ~/miniconda3/miniconda.sh
```

5. Add a conda initialize to your bash and  zsh
```sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

6. Verify the installaton
```sh
conda list
```

Create a conda virtual enviroment:
```sh
conda create -n envname python=x.x anaconda
```

Activate and initialize a conda virtual enviroment:
```sh
conda activate envname
pip install -r requirements.txt
```

Deactivate virtual environment:
```sh
conda deactivate
```
Remove virtual environment:
```sh
conda remove --name envname --all
```


The official guide can be found [here](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
