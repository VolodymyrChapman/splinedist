
# SplineDist: Automated Cell Segmentation with Spline Curves 

This repository contains the implementation of SplineDist, a machine learning framework for automated cell segmentation with spline curves.  The [manuscript](https://www.biorxiv.org/content/10.1101/2020.10.27.357640v1) is accepted at [ISBI 2021](https://biomedicalimaging.org/2021/). The code in its current state allows reproducing the paper experiments but is still in development. We are currently working to package it in a cleaned and optimized form. In the meantime, we encourage interested end-users to contact us for more information and assistance.


## Overview
SplineDist has been designed for performing instance segmentation in bioimages. Our method has been built by extending the popular [StarDist](https://arxiv.org/abs/1806.03535) framework. Our repository relies on the high-quality [StarDist](https://github.com/mpicbg-csbd/stardist) repository.  We encourage the user to explore StarDist repository for further details on the StarDist method.

While StarDist models objects with star-convex polygonal representation, SplineDist models objects as parametric spline curves. As our representation is more general, it allows to model non-star-convex objects as well, with the possibility of conducting further statistical shape analysis.


## Requirements 

1. Tensorflow

2. [StarDist 0.6.2](https://github.com/mpicbg-csbd/stardist) (can be installed with `pip` : `pip install stardist==0.6.2`)

## Example installation instructions
### Tested on Ubuntu 20.04. System compiler libraries required (installation of aptitude build-essential and gcc_linux-64 libraries may resolve compilation issues).
1. Initiate an environment titled splinedist containing python 3.6, tensorflow 2.4.0 and compilers required for build

        conda create -n splinedist -c conda-forge python=3.6 tensorflow=2.4.0 gcc_linux-64 gxx_linux-64 opencv -y
       
   Additionally, for use of Jupyter notebooks:
     
        conda install ipykernel

2. Activate the new environment and install splinedist (from GitHub)
    
        conda activate splinedist
        git clone https://github.com/uhlmanngroup/splinedist.git
        cd splinedist
        pip install .   
        

## Walkthrough

Three walkthrough notebooks have been included in this repository for data-exploration, training, and inference tasks.


## Datasets

The synthetic dataset used in the SplineDist manuscript can be found [here](https://osf.io/z89pq/).This dataset contains synthetic images with mostly star-convex and some non-star convex cell-like objects. 
