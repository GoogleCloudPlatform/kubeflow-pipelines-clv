# Predicting Customer Lifetime Value with Kubeflow Pipelines

## Overview

This repository maintains code samples accompanying the **Predicting Customer Lifetime Value with Kubeflow Pipelines** reference guide.

The **Predicting Customer Lifetime Value** reference guide discusses operationalization of Customer Lifetime Value (CLV) modeling techniques described in the [Predicting Customer Lifetime Value with AI Platform](https://cloud.google.com/solutions/machine-learning/clv-prediction-with-offline-training-intro) series of articles.

The primary goal of the guide is to demonstrate how to orchestrate two Machine Learning workflows:
- The training and deployment of the Customer Lifetime Value predictive model.
- Batch inference using the deployed Customer Lifetime Value predictive model.

## Understanding the design of the pipelines

The below diagram depicts the high level architecture:

![KFP Runtime](./images/arch-final.png)

There are two example pipelines 

Refer to [README](./pipelines/README.md)l in the `/pipelines` folder for more information.



## Deploying Kubeflow Pipelines

The example pipelines have been developed and tested on [AI Platform Pipelines](https://cloud.google.com/ai-platform/pipelines/docs). 

Refer to [README](./install/README.md) in the `/install` folder  for the instructions on how to deploy and configure an **AI Platform Pipelines** instance.

## Building and deploying the pipelines

The building and deploying of the solution components has been automated using **Cloud Build**. 

Refer to [README](./deploy/README.md) in the `/deploy` folder  for the detailed deployment instructions.


## Running the pipelines

There are two ways to run the solution's pipelines:
- Using Kubeflow Pipelines UI
- Using KFP SDK

Refer to [README](./run/README.md) in the `/run` folder  for detailed instructions on how to trigger runs.

## Repository structure

`/pipelines`
The source code for example pipelines.

`/components`

The source code for the custom components used in the pipelines.

`/install`

The environment setup instructions

`/deploy`

Cloud Build configuration for automated building and deployment.

`/run`

Sample code demonstrating how to use the `kfp.Client()` programmatic interface to KFP services.



## Acknowledgements

The sample dataset used in the samples is based on the publicly available [Online Retail Data Set](http://archive.ics.uci.edu/ml/datasets/Online+Retail) from the UCI Machine Learning Repository. 

The original dataset was preprocessed to conform to the the schema used by the solution's pipelines and uploaded to a public GCP bucket as `gs://clv-datasets/transactions/`. 



