# Local Install and Tutorial

## Python
For the main required Python packages (numpy, scipy, etc.) we recommend using
[Anaconda for Python 3.8](https://www.continuum.io/downloads)


## Installing package and dependencies for NOVAS3D locally

1. Clone repository

        git clone https://github.com/mrozak4/novas3d.git novas3d

        (or install zip file and uncompress)

        cd novas3d

    If you want to create a virtual environment with anaconda where NOVAS3D can be run,

        conda create -n novas3d python=3.8
        source activate novas3d
    
    To end the session, deactivate the environment
    
        source deactivate
    
    To delete the environment,
    
        conda env remove --name novas3d

    Alternative: Use virtualenv to make a virtual enviornment
        
        virtualenv -p python3.8 ENV
        source ENV/bin/activate

2. Install dependencies
    
        pip install novas3d
        pip install git+https://github.com/Image-Py/sknw.git@18f18ab94794964a6dd7a76dd8a2c5c00dab6fd1

3. Download example data
     
     Ensure [git-lfs](https://git-lfs.com/) is installed and enabled or else pickle files present in the example data and model files will not download properly.

        git clone https://huggingface.co/datasets/mrozak/novas3d_example_data

4. Download the model

        git clone https://huggingface.co/mrozak/NOVAS3D_Vessel_and_Neuron_Segmentation


5. Test the installation by running the tutorial in jupyter 

        jupyter notebook Tutorial.ipynb

## Updating NOVAS3D
To update NOVAS3D, navigate to the directory where NOVAS3D was cloned and run

    git pull
    pip install novas3d
                                                                                                