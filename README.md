# To use pyemma in CESGA FT3 HPC: 
#"go to https://cesga-docs.gitlab.io/ft3-user-guide/env_modules.html for initial instruction."

#In your login node:apply compute node, the time limit for this job is 8.0 hours:

```
compute -c 64 --mem 150
```
#activate conda
```
export CONDA_ENVS_PATH=$STORE/conda/envs
```
```
export CONDA_PKGS_DIRS=$STORE/conda/pkgs
```
```
module load cesga/2020 miniconda3/4.9.2
```
#activate the pyemma conda environment:
```
 source activate pyemma
```

#Inside of your pyemma env, call on jupyter (don't install yourself)
```
(pyemma) [try-msm]$ start_jupyter
```


##########################

##Installing PyEMMA2.5.7 in CESGA FT3 cluster can be tricky

#activate conda

```
export CONDA_ENVS_PATH=$STORE/conda/envs
```
```
export CONDA_PKGS_DIRS=$STORE/conda/pkgs
```
```
module load cesga/2020 miniconda3/4.9.2
```
```
conda create -n pyemma python=3.7
```

```
 source activate pyemma
```
#First download the archived package for installing pyemma from the anaonda website: https://anaconda.org/conda-forge/pyemma/files?version=2.5.7
```
(pyemma) [try-msm]$ conda install /mnt/netapp1/Store_CSIC/home/csic/tsm/hlu/aa/pyemma-2.5.7-py37hdc94413_6.tar.bz2
```
Then insall a series of depending sub modules of pyemma:

```
python -m pip install pandas==0.25.3
```

```
python -m pip install mdtraj==1.9.5
```

#Other modules like
```
 h5py==3.8.0 tqdm==4.67.1 pyyaml==6.0.1 psutil==7.0.0  pathos==0.3.1 matplotlib==3.5.3
```

#In the end it is advisable to install pyemma for double check
```
python -m ip install pyemma==2.5.7
```
#if it doesn't work, please check the following the version of the following packages:
```
numpy-1.21.6 pandas-0.25.3 python-dateutil-2.9.0.post0 pytz-2025.2 six-1.17.0
```
