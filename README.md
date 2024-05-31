# WineQualityPred-InRemoteServer-using-Daxab-mlflow

# Allowing Dagshub to track my repo MLflow
===============================================

# Method 1
=============
  Step 1 =: Installing the dagshub in to our current working repo or directory

```bash
pip install -q dagshub mlflow
```
 Step 2 =: Use the DagsHub client to setup connection information for MLflow

```bash
import dagshub
dagshub.init(repo_owner='Vamsivarma116', repo_name='WineQualityPred-InRemoteServer-using-Daxab-mlflow', mlflow=True)
```
 Step 3 =: Use MLflow to log params and metrics(Which is already done in WineQualityPred.py file line no 74 - 78)

```bash
import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)
```

# Method : 2  
===============
  Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/''''''''''''

export MLFLOW_TRACKING_USERNAME="   " 

export MLFLOW_TRACKING_PASSWORD="   "

```