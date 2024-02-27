Singularity related variables 
$SINGULARITY_CACHEDIR controls where conteiners are downloaded to or expanded
$HOME is mounted into the container, so anything on $PATH that exist in $HOME is available insithe the container
Enviroment variables are carried over 
just like srun/sbatch
Understand: $PATH, $LD_LIBRARY_PATH, $PYTHONPATH, $OMP_NUM__THREADS, '$CUDA_VISIBLE_DEVICES, etc.

There are two types of specifications you can use:
1)Dockerfile to build an image using Docker or dockerhub and convert to Singularity 
2) A Singularity file to create an image using singularity (needs roots privilegy) on singularity hub.

Curso https://sib-swiss.github.io/containers-introduction-training/2023.12/course_material/introduction_containers/
Aula https://sib-swiss.github.io/containers-introduction-training/2023.12/course_material/apptainer/
#####################################################################################################

............ comeca aqui, precisa ser root.........
# Ensure repositories are up-to-date
sudoapt-getupdate
# Install debian packages for dependencies
sudo apt-getinstall-y\
   autoconf\
   automake\
   cryptsetup\
   git\
   libfuse-dev\
   libglib2.0-dev\
   libseccomp-dev\
   libtool\
   pkg-config\
   runc\
   squashfs-tools\
   squashfs-tools-ng\
   uidmap\
   wget\
   zlib1g-dev
....... agora é como usuario /home/admin em uma pasta qualquer............
export VERSION=4.0.0 && # adjust this as necessary \
    wget https://github.com/sylabs/singularity/releases/download/v${VERSION}/singularity-ce-${VERSION}.tar.gz && \
    tar -xzf singularity-ce-${VERSION}.tar.gz && \
    cd singularity-ce-${VERSION}
./mconfig --without-suid --prefix=/home/admin/singularity-ce && \
    make -C ./builddir && \
    make -C ./builddir install
echo "source /home/admin/singularity-ce/share/bash-completion/completions/singularity" >> ~/.bashrc && source ~/.bashrc
### testando o help no  RMATS!!!!!!
/home/admin/singularity-ce/bin/singularity run docker://xinglab/rmats python3 /rmats/rmats.py --help
### repositorio com varios programas
https://depot.galaxyproject.org/singularity/

Pulling an image

Use apptainer pull to convert an image from dockerhub to the ‘apptainer image format’ (.sif)
singularity pull docker://godlovedc/lolcow

biocontainers/phyml
biocontainers/repeatmasker-recon

#open container
 singularity run ../SIF/iqtree_2.2.2.3--h2202e69_2.sif

#You can also use the build command to download pre-built images from an external resource. When using build you must specify a name for your container like so:

 singularity build ubuntu.sif library://ubuntu
 singularity build lolcow.sif docker://godlovedc/lolcow

