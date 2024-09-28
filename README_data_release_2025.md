# Huawei Public Cloud Trace 2025

This is the description of the Huawei Public Cloud Trace 2025. The data is described in our paper, <a href="https://github.com/sir-lab/data-release/blob/main/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf" download> ***Serverless Cold Starts and Where to Find Them***</a> (EuroSys 2025). 

We provide a schema of the dataset as well as several notebooks and scripts to show how to load the data and make plots.

We also provide the links to download the dataset. 


### Download/read our paper

* <a href="https://github.com/sir-lab/data-release/blob/main/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf" download> GitHub </a>

## How to download the data

The datasets used in our paper can be downloaded here:

## Cold starts

These files contain every cold start analyzed in our paper. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R1.zip)|Region 1 cold start events|
|[Region 2 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R2.zip)|Region 2 cold start events|
|[Region 3 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R3.zip)|Region 3 cold start events|
|[Region 4 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R4.zip)|Region 4 cold start events|
|[Region 5 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R5.zip)|Region 5 cold start events|


## Trigger types and runtime languages

This file contains the runtime languages, trigger types, and CPU request for each function in Region 2. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 2 runtimes and trigger types](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/runtime_triggerType/df_funcID_runtime_triggerType.csv)|Runtime languages and trigger types per function in Region 2|


## Quantiles

These files contain the quantiles of different metrics on our platform per function, such as totalCost (function execution time) or cold start time. We also include the number of requests, number of pods, and number of cold starts. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R1.zip)|Region 1 quantiles|
|[Region 2 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R2.zip)|Region 2 quantiles|
|[Region 3 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R3.zip)|Region 3 quantiles|
|[Region 4 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R4.zip)|Region 4 quantiles|
|[Region 5 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R5.zip)|Region 5 quantiles|




## Request tables

* Coming soon




