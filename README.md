# reproducibility-tutorial
# i did it

## Cloning repository on githubreproducibility tutorial for FOSS
    1  cd /scratch
    2  df -h
    3  pwd
    4  git clone https://github.com/mmsprinkle/reproducibility-tutorial.git
    5  ls
    6  clear

## Computer Setup

	# download the Miniconda installer
	 wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

	# install miniconda silently (-b) in path (-p) /opt/conda
	bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda

	# make sure all conda packages will be in path by symbolic links to /bin    
	ln -s /opt/conda/pkgs/*/bin/* /bin
	ln -s /opt/conda/bin/* /bin
 	ln -s /opt/conda/pkgs/*/lib/* /usr/lib

	# Intall Jupyter lab version 1.2.3
	/opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
	/opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   
13  /opt/conda/bin/pip install bash_kernel
   14  /opt/conda/bin/pip install ipykernel
   15  /opt/conda/bin/python3 -m bash_kernel.install
   16  clear
   17  /opt/conda/bin/conda search htseq
   18  /opt/conda/bin/conda search -c bioconda htseq
   19  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   20  /opt/conda/bin/conda search -c bioconda snakemake
   21  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   22  ln -s /opt/conda/bin/* /bin
   23  ln -s /opt/conda/lib/* /usr/lib
   24  snakemake --version
   25  sudo apt-get update
   26  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   27  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   28  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   29  sudo apt-get update
   30  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   31  docker run hello-world
   32  cd /scratch/reproducibility-tutorial/
   33  history >>README.md
