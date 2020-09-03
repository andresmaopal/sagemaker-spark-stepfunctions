# Build End-to-End Machine Learning (ML) Workflows with Amazon SageMaker, Spark pre-processing and Step Functions orchestration

This repository contains the assets for the Amazon Sagemaker and Apache Airflow integration sample described in an upcoming AWS blogpost.

## Overview

This repository shows a sample example to build, manage and orchestrate large-data, Spark-based ML workflows using Amazon Sagemaker and Amazon Step Functions. We use a publicly-available Abalone dataset to demonstrate the flow, but the same flow would work for any large dataset as well. More details on this dataset can be found at [UCI data repository](https://archive.ics.uci.edu/ml/datasets/abalone). The ML pipeline shows how to do data ETL pre-processing with PySpark code on SageMaker Processing, train an XGBoost model on this data, implement an inference pipeline container (Spark ETL + XGBoost), and use it for both real-time inference as well as batch inference.

## Solution architecture and workflow

<a href="https://ibb.co/FzS9fYp"><img src="https://i.ibb.co/Pg7RbWk/Arquitectura-spark-workflow.png" alt="Arquitectura-spark-workflow" border="0"></a>
