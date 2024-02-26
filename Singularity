Singularity related variables 
$SINGULARITY_CACHEDIR controls where conteiners are downloaded to or expanded
$HOME is mounted into the container, so anything on $PATH that exist in $HOME is available insithe the container
Enviroment variables are carried over 
just like srun/sbatch
Understand: $PATH, $LD_LIBRARY_PATH, $PYTHONPATH, $OMP_NUM__THREADS, '$CUDA_VISIBLE_DEVICES, etc.

Vagrant related variables
$VAGRANT_HOME location of vagrant directory 
machinefolder a property for VirtualBox that determines locations of running virtual machines.

There are two types of specifications you can use:
1)Dockerfile to build an image using Docker or dockerhub and convert to Singularity 
2) A Singularity file to create an image using singularity (needs roots privilegy) on singularity hub.



singularity pull docker://biocontainers/repeatmasker-recon
#open container
 singularity run ../SIF/iqtree_2.2.2.3--h2202e69_2.sif
