---
layout: page
title: MPI install with conda (mpi4py)
permalink: posts/mpi_install/
---
1. install **openmpi** instead of mpich, Open MPI 4.0.3/4.0.4 works for me - I always got "mpi4py libmpi.so.12: cannot open shared object file: no such file or directory" error message when using mpich. Check your mpi use `mpirun --version` for ubuntu.
2. Create a clean environmemt, python version 3.9.16 and 3.11.4 work for me
3. `conda install -c conda-forge mpi4py`
4. Test your MPI and mpi4py use script:

  import mpi4py
  from mpi4py import MPI

  comm = MPI.COMM_WORLD
  rank = comm.Get_rank()
  print('My rank is ',rank)

In command line use `mpirun -n 4 python name_of_your_script.py`
