# Build End-to-End Machine Learning (ML) Workflows with Amazon SageMaker, Spark pre-processing and Step Functions orchestration

This repository contains the assets for the Amazon Sagemaker and Apache Airflow integration sample described in an upcoming AWS blogpost.

## Overview

This repository shows a sample example to build, manage and orchestrate large-data, Spark-based ML workflows using Amazon Sagemaker and Amazon Step Functions. We use a publicly-available Abalone dataset to demonstrate the flow, but the same flow would work for any large dataset as well. More details on this dataset can be found at [UCI data repository](https://archive.ics.uci.edu/ml/datasets/abalone). The ML pipeline shows how to do data ETL pre-processing with PySpark code on SageMaker Processing, train an XGBoost model on this data, implement an inference pipeline container (Spark ETL + XGBoost), and use it for both real-time inference as well as batch inference.

## Solution architecture and workflow

The following architecture shows both the development and deployment components for production using the different types of SageMaker jobs, from the preprocessing of the dataset, for which we will use the public Abalone dataset, the training using an XGBoost model, the optimization of hyperparameters, inference pipeline and results writing (output). This solution is available in a CloudFormation so it can be reproduced in your own AWS account.

<a href="https://ibb.co/FzS9fYp"><img src="https://i.ibb.co/Pg7RbWk/Arquitectura-spark-workflow.png" alt="Arquitectura-spark-workflow" border="0"></a>

## Steps

1. Deploy on your internal account the CloudFormation stack included on this repo:

https://github.com/andresmaopal/sagemaker-spark-stepfunctions/blob/master/cfn/step-functions-sagemaker.yaml

2. Create a SageMaker Notebook instance (ml.m5.xlarge) and upload the step by step demo Notebook included on this repo (this Notebook references a Dev environment where first all steps are assembled):

https://github.com/andresmaopal/sagemaker-spark-stepfunctions/blob/master/cfn/step-functions-sagemaker.yaml

3. Go to Step Functions on the AWS Console and notice the XXXXXXX-workflow-spark-ml states machine, an execute it.


<a href="https://ibb.co/fxjc3Bk"><img src="https://i.ibb.co/jrnpCBy/Screen-Shot-2020-09-03-at-4-35-42-PM.png" alt="Screen-Shot-2020-09-03-at-4-35-42-PM" border="0"></a>







