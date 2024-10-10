<h1 align="center" style="margin-bottom:0px; border-bottom:1px; padding-bottom:10px">Huawei Public Cloud Trace 2025</h1>


This is the description of the Huawei Public Cloud Trace 2025. The data is described in our paper, <a href="https://arxiv.org/abs/2410.06145" download> ***Serverless Cold Starts and Where to Find Them***</a> (EuroSys 2025). 

We provide a schema of the dataset as well as several notebooks and scripts to show how to load the data and make plots. We also provide the links to download the dataset. 

# Table of Contents
- [Table of Contents](#table-of-contents)
- [How to download the data](#how-to-download-the-data)
  - [Code](#code)
  - [Huawei Public cold starts](#huawei-public-cold-starts)
    - [Schema](#schema)
  - [Huawei Public request tables](#huawei-public-request-tables)
    - [Schema](#schema-1)
  - [Huawei Public trigger types and runtime languages (2025)](#huawei-public-trigger-types-and-runtime-languages-2025)
    - [Schema](#schema-2)
  - [Huawei Public time series (2025)](#huawei-public-time-series-2025)
    - [Schema](#schema-3)

# How to download the data

The datasets used in our paper can be downloaded at the links below. 

In some cases, you may not need all files in a zip folder. In this case, use <a href='https://www.7-zip.org/download.html'> 7zip</a> to open the zipped file and drag out the files or directories you want without extracting everything. 

## Code

To get started using the datasets, look at our notebook for tips on how to load files and visualize the data.
* Huawei Public cold starts 2025 <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_cold_start.ipynb"> notebook</a>

## Huawei Public cold starts

These files contain every cold start analyzed in our 2025 paper. 

**Length:** 31 days

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R1.zip)|Region 1 cold start events|
|[Region 2 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R2.zip)|Region 2 cold start events|
|[Region 3 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R3.zip)|Region 3 cold start events|
|[Region 4 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R4.zip)|Region 4 cold start events|
|[Region 5 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R5.zip)|Region 5 cold start events|

### Schema
This table contains individual cold start events. There are different steps of a cold start, including pod allocation, time to deploy code, time to deploy dependencies, and scheduling and other overheads. 

| Name  | Log | Description | Unit    | Example   |
|-------|-----|-------------|---------|----------|
| day  | cold start | day   | date    | 0-30      |
| time  | cold start | cold start timestamp | seconds | 51937.425 |
| clusterName | cold start | cluster processing | int | can be 1, 2, 3, 4 |
| funcName| cold start | function name | int     | 10  |
| userID  | cold start | user ID   | int     | 134   |
| requestID    | cold start | unique request identifier of the request that triggered the scaling decision. Note that one request may trigger multiple cold start events.         | -       | 82f1aa192e8ce27...|
| totalCost_cold_start   | cold start | total time spent on cold start. This should be used as the `cold start time` | seconds | 2.239314 |
| podAllocationCost      | cold start | the time taken to start a pod if no free pods exist or to select a pod from the existing pool to be used by the newly started function | seconds | 0.027161815 |
| deployCodeCost         | cold start | time to download, extract, and deploy function code | seconds | 0.045 |
| deployDependencyCost   | cold start | time to fetch and load dependencies   | seconds | 0.454 |
| schedulingCost         | cold start | time for networking, routing, and scheduling overheads | seconds | 1.713152185 |
| podID | cold start | pod ID, contains the pool name (pool24-600-512) which contains pods with CPU limit 600 millicores and memory limit 512MB.  | -       | pool24-600-512-0000577863        |

## Huawei Public request tables

This table contains event-level logs of individual requests for day 30 of our dataset. 

**Length:** 1 day

|Metric         |Download link          |
|--------------------|---------------------|
|Region 1 requests| Coming soon |
|Region 2 requests| [Region 2 part 1](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00000_00019.zip), [Region 2 part 2](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00020_00039.zip), [Region 2 part 3](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00040_00059.zip), [Region 2 part 4](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00060_00079.zip), [Region 2 part 5](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00080_00099.zip), [Region 2 part 6](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00100_00119.zip), [Region 2 part 7](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00120_00139.zip), [Region 2 part 8](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00140_00159.zip), [Region 2 part 9](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00160_00179.zip), [Region 2 part 10](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R2/R2_00180_00199.zip)
|Region 3 requests| Coming soon |
|Region 4 requests| [Region 4 part 1](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R4/R4_00000_00099.zip), [Region 4 part 2](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R4/R4_00100_00199.zip)
|Region 5 requests|[Region 5](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R5/R5.zip)|


### Schema 

Huawei's serverless platform produces logs in several different components. This dataset includes data from three main types of logs: frontend, worker, and cold start. 

This section briefly describes the architecture of our system, shown in the diagram below. When a user sends a request, it arrives at the frontend. The frontend sends the requests to a VM, which receives it using the busProxy. The request is then handled by a function worker pod. The function worker pod contains a runtime for the function to run, and a worker component to monitor and interface with the runtime. 

![System architecture](https://github.com/sir-lab/data-release/blob/main/architecture.png)

The timestamps have been normalized to start at 0 on day 0, so 2600186.994 means 2600186 seconds and 994 milliseconds after the start of the dataset. 

**Resource usage** The CPU usage of a request is the CPU usage of the entire pod, averaged over the execution time of that request. Similarly, the memory usage of a request is the memory usage of the entire pod, averaged over the execution time of that request.


| Name              | Log      | Description            | Unit   | Example                |
|-------------------|----------|------------------------|--------|------------------------|
| time_worker       | worker   | worker timestamp       | seconds| 2600186.994            |
| time_frontend     | frontend | frontend timestamp     | seconds| 2600186.995            |
| requestID         | worker   | unique request identifier | hash   | 763ff09a...            |
| clusterName       | worker   | cluster starting pod   | int    | can be 1, 2, 3, 4      |
| funcName          | worker   | function name          | int    | 296                    |
| podID             | worker   | pod ID, contains the pool name (pool22-300-128) which contains pods with CPU limit 300 millicores and memory limit 128MB. | -      | pool22-300-128-0000618412 |
| userID            | worker   | unique user ID         | int    | 224                    |
| totalCost_worker  | worker   | total time spent in function worker pod   | seconds| 0.023749               |
| workerCost        | worker   | time spent in worker   | seconds| 0.000112               |
| runtimeCost       | worker   | time spent in runtime  | seconds| 0.023637               |
| totalCost_frontend| frontend | end-to-end time as measured by frontend   | seconds| 0.026421               |
| frontendCost      | frontend | time spent monitoring and forwarding in frontend  | seconds| 0.000364               |
| busCost           | frontend | time spent in busProxy component | seconds| 0.001994               |
| readBodyCost      | frontend | time spent reading request body  | seconds| 0.000016               |
| writeRspCost      | frontend | time spent writing response      | seconds| 0.000006               |
| cpu_usage         | worker   | CPU usage              | cores  | 0.291506               |
| memory_usage      | worker   | memory usage           | MB     | 32.308594              |
| requestBodySize   | frontend | size of the request body  | Bytes  | 1018                   |


## Huawei Public trigger types and runtime languages (2025)

This file contains the runtime languages, trigger types, and CPU request for each function in Region 2. 

**Length:** static (valid for 31 days)


|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 2 runtimes and trigger types](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/runtime_triggerType/df_funcID_runtime_triggerType.csv)|Runtime languages and trigger types per function in Region 2|

### Schema 

This table contains the cpu_request, runtime language, and triggerType-invocationType of each function in Region 2. A unique function is identified by funcID, which is a combination of funcName, userID, and poolName.

**CPU request and CPU limit** In our system, the user can specify a CPU limit, e.g. 300 millicores. This is the maximum amount of CPU that pods for this function can use. However, the amount of CPU initially requested tends to be lower, which we call cpu\_request. The exact value of cpu_request for different resource configurations may vary, and we provide common values from one region, but they can be used for other regions as well. 

| Name | Log | Description | Unit | Example |
|------|-----|-------------|------|---------|
| funcID | -   | funcName---userID---poolName | - | 400---418---pool22-300-128 |
| cpu_request | - | Amount of CPU requested  | millicores  | 100 |
| runtime  | -   | Runtime language | - | Python3 |
| triggerType-invocationType    | -   | List of trigger types of function, as well as the invocation type (synchronous/asynchronous). Refer to the paper for more details. | - | workflow-S  |



## Huawei Public time series (2025)

These files contain the time series of different metrics on our platform per function, including quantiles of totalCost (function execution time) or cold start time. We also include the number of requests, number of pods, and number of cold starts. 

**Length:** 31 days

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R1.zip)|Region 1 quantiles|
|[Region 2 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R2.zip)|Region 2 quantiles|
|[Region 3 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R3.zip)|Region 3 quantiles|
|[Region 4 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R4.zip)|Region 4 quantiles|
|[Region 5 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R5.zip)|Region 5 quantiles|

### Schema

In addition to the event-based tables above, we provide files that aggregate different metrics per minute as a time series per funcID. The funcID uniquely identifies a function, which is a combination of funcName, userID, and poolName, e.g. 400---418---pool22-300-128 (funcName=400, userID=418, poolName=pool22-300-128). Refer to the example notebooks for more information about how to use these files.

We provide the following summary statistics per function per minute: avg, std, and 0, 0.25, 0.50, 0.75, 0.90, 0.95, 0.99 1.00 quantiles. 

These statistics are computed for most of the metrics seen in the event-based tables, as shown in the table below.

| Name                  | Log        | Description                                         |
|-----------------------|------------|-----------------------------------------------------|
| busCost               | frontend   | See request table schema.                       |
| cpu_usage             | worker     | See request table schema.                       |
| deployCodeCost        | cold start | See cold start table schema.                    |
| deployDependencyCost  | cold start | See cold start table schema.                    |
| frontendCost          | frontend   | See request table schema.                       |
| memory_usage          | worker     | See request table schema.                       |
| num_cold_starts       | cold start | Number of cold starts per function. See cold start table schema. |
| num_pods              | worker     | Number of running pods per function. See request table schema.    |
| podAllocationCost     | cold start | See cold start table schema.                    |
| readBodyCost          | frontend   | See request table schema.                       |
| requestBodySize       | frontend   | See request table schema.                       |
| requests              | worker     | Number of requests per function. See request table schema.         |
| runtimeCost           | worker     | See request table schema.                       |
| schedulingCost        | cold start | See cold start table schema.                    |
| totalCost             | worker     | See totalCost_worker in request table schema.   |
| totalCost_cold_start  | cold start | See cold start table schema.                    |
| totalCost_frontend    | frontend   | See request table schema.                       |
| workerCost            | worker     | See request table schema.                       |
| writeRspCost          | frontend   | See request table schema.                       |
