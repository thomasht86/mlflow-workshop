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

1. Clone the workshop repository.
    
    ```git clone https://github.com/thomasht86/mlflow-workshop.git```

2. Create conda environment. 

    Run ```conda env create -f condaenv.yml``` from the project root directory in a Anaconda prompt.
    This will create a conda environment with the necessary packages installed.

3. Activate conda environment. 
    
    Run ```conda activate mlflowenv``` in Anaconda prompt. This will activate the newly created environment.

4. Start jupyter notebook server with the active environment.

    Run ```jupyter notebook``` in Anaconda prompt. The jupyter server is now available at ```localhost:8888``` in your browser. 

5. Start mlflow tracking server with the active environment.

    Run ```mlflow ui``` in Anaconda prompt. The mlflow server is now available at ```localhost:5000``` in your browser. 
