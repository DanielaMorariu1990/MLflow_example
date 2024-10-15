# MLflow example in Jupyter Notebook 


This Jupyter notebook offers the possibility to try out the MLflow model locally. You can then explore the MLflow UI and play with various experiments.

## Data
I use the wine data set from sklearn. It's a small inbuilt data set, perferct to try out new models or frameworks. 

## Data exploration
The purpose of the notebook was not to explore data, but I did include some basic EDA plots, just to mimic the data science process. In reality about 80% of the time spent on a use case goes into data cleaning, processing and exploration.

## Data preprocessing

I did some basic preprocessing on the data. 

## ML workflow

I train both a Random Forest Classifier from the standrad framework sklearn, as well as an Explanable Boosting Machine algorithm from the package interpret.
This way you can explote how various framework are used in conjuction with MLflow. 
I log parameters, metrics and artifacts for both models. I then load the model via the MLflow framwrok and predict using both models. I also breifly explore how one would serve a model to an endpoint (this time a local endopoint on your machine). 
At this point you can explore and intercat with the MLflow UI. 
After you explore the UI, feel free to also try out various ways to intercat with the experiments via the MLflow tracking APIs. I give a brief example how to select multiple runs from a particular experiment using a metrics, as a criterion.

## How to start

Start by creating a new conda environment. All the mentioned steps are to be executed inside a terminal. 
```
conda create --name mlflow_env python=3.8 pip

```
Install the requirements.txt with pip:

```
pip install -r requirements.txt

```

Create a Jupyter notebook Kernel. 

```
conda install ipykernel
python -m ipykernel install --user --name mflow_kernel

```

Then select the created kernel and execute the Jupyter notebook. (If you slect an existing kernel and run the command !pip install -r requirements.txt in your notebook, then the requirements will be installed in that  existing environment. However you will not have a completely new and clean environment for experimentation, which is not the best practice.)

You can explore the mlflow UI via the command, sued in teh terminal. 
```
mflow ui 

```