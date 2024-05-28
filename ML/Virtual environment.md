for Conda environment {change the name new_env}
```bash
conda create -n new_env python==3.9
```

to activate new or previous environment
```bash
conda activate new_env
```
to install python
```shell
conda search --full-name python
conda search  pandas
conda install python=3.8
```

to create a kernel for jupyter notebook

```bash
conda install ipykernel
```

Then deactivate the virtual environment
```bash
conda deactivate
```
To add the Jupyter kernel run this on base environment
```bash
python -m ipykernel install --user --name new_env --display-name "name-change this"
```
To install jupyter in virtual
```bash
conda install jupyter
```
to install any Python package
```bash
conda install <package_name>
```

to find the all environment
```bash

conda info --envs
```

Update python
``` shell
conda update python
```

conda update
``` shell
conda update -n base -c conda-forge conda
```

update pip

```shell
conda update pip
```

```python
! pip install --upgrade pip
```

```shell
pip --version
```