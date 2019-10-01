# git_practice
## Create an Image for DL with FastAI project
Start with a Ubuntu 18.04 LTS image

###Install Anaconda3
- follow instruction found at
  https://docs.anaconda.com/anaconda/install/linux/
  
  Download the file (found at 
  $ wget https://repo.anaconda.com/archive/Anaconda3-2019.07-Linux-x86_64.sh 


### Install the file 
  * Install the downloaded file
  
  $ bash Anaconda3-2019.07-Linux-x86_64.sh
  
  * Add the path to the bashrc file 
  
  $ export PATH=~/anaconda3/bin:$PATH
  
  * Check that now conda is in the PATH
  
  $ conda --version 

### Create an Environment 
  * follow instructions at https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/
  * Update Conda
  
  $ conda update conda
  
  $ conda create -n v3 python=3.7 anaconda
  * => results in an update of the packages.
  
  $ source activate v3 ("conda activate v3" didn't work)


### Clone FastAI course V3 github project 
  * create a www folder
  $ mkdir www
  $ cd www
  $ git clone https://github.com/fastai/course-v3.git
  $ cd course-v3/
  $ tools/run-after-git-clone

### Install dependencies

  $ conda install jupyter nb_conda nb_conda_kernels ipykernel
  
  $ conda install -c fastai fastai
  
