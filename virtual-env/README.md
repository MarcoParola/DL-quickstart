# Virtual environment

Virtual environments are useful because they provide isolated environments for Python projects, preventing conflicts between dependencies. They allow for project-specific package installations, enabling clean and reproducible development environments. Additionally, virtual environments facilitate dependency management, making it easier to share projects without worrying about conflicting dependencies.

Create a virtual enviroment:
```sh
python -m venv /path/to/new/virtual/environment
```

Activate virtual environment:
```sh
source <venv>/bin/activate
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

### Official Guide:
[https://docs.python.org/3/library/venv.html](https://docs.python.org/3/library/venv.html)

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
