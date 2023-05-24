for Conda environment
```bash
conda create -n new_env python==3.9
```

to activate new or previous environment
```bash
conda activate new_env
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

