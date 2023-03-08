# Intro
This is a Jupyter installation on Open OnDemand with some customization.

## Prerequisites

This Batch Connect app requires the following software be installed on the
**compute nodes** that the batch job is intended to run on (**NOT** the
OnDemand node):

- [Jupyter](http://jupyter.readthedocs.io/en/latest/)

  This setup was installed using 

  `conda create --prefix $HPC_SOFTWARE/jupyter/3.6.1 -c conda-forge jupyterlab=3.6.1 python=3.9`
  
- [OpenSSL](https://www.openssl.org/) 1.0.1+ (used to hash the Jupyter server password)

**Optional** software:

- [Lmod](https://www.tacc.utexas.edu/research-development/tacc-projects/lmod)
  6.0.1+ or any other `module purge` and `module load <modules>` based CLI
  used to load appropriate environments within the batch job before launching
  the Jupyter Notebook server.