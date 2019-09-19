# Workshop EDC2019 - Machine learning - from experiments to production with MLFlow
This repo contains instructions and code to follow the workshop presented 19-09-2019.

The tutorial will demonstrate the lifecycle of a text classifier through the following phases:
1. Experimenting and EDA in jupyter notebook.
2. Running structured experiments locally.
3. Running experiments remotely on a Databricks-cluster in Azure.
4. Evaluating results of experiments and choosing a model to deploy.
5. Deploy the selected model to production in Azure. 
6. Making requests to the model.

The goal of the workshop is to expose participants to the capabilities of MLFlow, and provide a kickstart for those considering to use the platform for their own projects. 

## Set up environment
This is a guide to help you set up your development environment if you want follow the demo on your own computer. (And use MLFlow for your own projects afterwards). 

If you don't have Anaconda installed, you should do that prior to the workshop. [Here](https://www.anaconda.com/distribution/) is the link to download Anaconda.

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


## Cheatsheet for structure of workshop

* Welcome. Short introduction. Experience. GreenTeam DP. (10min)
* Talk about agenda. Phases in readme.
* What is MLFlow? Tracking, Scaling, Serving
* Check prior experience of participants. MLFlow? Databricks? Machine Learning?
* Check if trouble with prerequisites.
* Get everyone up with environment.
* Create conda env. 
* ------10 min break--------
* Go through the jupyter notebook step-by-step.
* Go through train.py file. Focus on mlflow components and how to create a model class. 
* Run training locally.
* Run training with different parameters from notebook.
* Go through comparison in MLFLow UI.
* ------10 min break--------
* Configure databricks CLI. NB: NOT instance id.
* Set tracking URI:
    
    Switch tracking:

    ```export MLFLOW_TRACKING_URI="databricks"```

    Switch back: 

    ```export MLFLOW_TRACKING_URI="file:///c/Users/thotho/Documents/Repos/mlflow-workshop/mlruns"```
* Create experiment in databricks with same name as in code. Get Experiment ID from databricks UI.
* Show how to get databricks cluster configuration from UI.
* Run training in cloud on databricks: <br> 
```mlflow run https://github.com/thomasht86/mlflow-workshop.git -b databricks --backend-config db-clusterconfig.json --experiment-id 1774975914207469```
* Go through deployment-notebook
* Show Azure ML workspace in portal.
* Get predictions from model. 