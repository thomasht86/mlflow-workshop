# Workshop EDC2019 - Machine learning - from experiments to production with MLFlow
This repo contains instructions and code to follow the workshop presented 17-09-2019.

The tutorial will demonstrate the lifecycle of a text classifier through the following phases:
1. Experimenting and EDA in jupyter notebook.
2. Running structured experiments locally.
3. Running experiments remotely on a Databricks-cluster in Azure.
3. Evaluating results of experiments and choosing a model to deploy.
4. Deploy the selected model to production in Azure. 
5. Making requests to the model.

The goal of the workshop is to expose participants to the capabilities of MLFlow, and provide a kickstart for those considering to use the platform for their own projects. 

## Set up environment
This is a guide to help you set up your development environment if you want follow the demo on your own computer. (And use MLFlow for your own projects afterwards). 

1. Install Windows Subsystem for Linux (WSL).

    Follow [this](https://docs.microsoft.com/en-us/windows/wsl/install-win10) tutorial to install WSL on Windows 10.

2. Clone the workshop repository.
    
    ```git clone https://github.com/thomasht86/mlflow-workshop.git```

3. Create conda environment. 

    Run ```conda env create -f condaenv.yml``` from the project root directory in a WSL terminal.
    This will create a conda environment with the necessary packages installed.

4. Activate conda environment. 
    
    Run ```conda activate mlflowenv``` in WSL terminal. This will activate the newly created environment.

5. Start jupyter notebook server with the active environment.

    Run ```jupyter notebook``` in WSL terminal. The jupter server is now available at ```localhost:8888``` in your browser. 

