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

In some cases, you may not need all files in a zip folder. In this case, use <a href='https://www.7-zip.org/download.html'> 7zip</a> to drag and drop the desired files or directories without extracting the entire archive. 

## Code

Use the <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_cold_start.ipynb"> Huawei Public cold starts 2025 notebook</a> to get started analyzing the data.

## Huawei Public cold starts

These files contain every cold start analyzed in our 2025 paper. 

**Duration:** 31 days

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 cold starts](https://drive.google.com/file/d/1mMQtfZNtg-EPmGmGYuOzC5KPbZoXRd8e/view?usp=drive_link)|Region 1 cold start events|
|[Region 2 cold starts](https://drive.google.com/file/d/1qjnBBH_yEOnxAG5vFPQwx6xyITZrrP8L/view?usp=drive_link)|Region 2 cold start events|
|[Region 3 cold starts](https://drive.google.com/file/d/1WlUk-tQLao6mU0FoMx9YO2-HIMevEDjX/view?usp=drive_link)|Region 3 cold start events|
|[Region 4 cold starts](https://drive.google.com/file/d/1YywoClXTZ1Q0jKfB2Y3Hgu0xh0lrDoBZ/view?usp=drive_link)|Region 4 cold start events|
|[Region 5 cold starts](https://drive.google.com/file/d/1ah7nj5fyedMpOeaFgNVA7oMx3815D8BZ/view?usp=drive_link)|Region 5 cold start events|

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
| totalCost_cold_start   | cold start | total time spent on cold start. This should be used as the cold start time | seconds | 2.239314 |
| podAllocationCost      | cold start | the time taken to start a pod if no free pods exist or to select a pod from the existing pool to be used by the newly started function | seconds | 0.027161815 |
| deployCodeCost         | cold start | time to download, extract, and deploy function code | seconds | 0.045 |
| deployDependencyCost   | cold start | time to fetch and load dependencies   | seconds | 0.454 |
| schedulingCost         | cold start | time for networking, routing, and scheduling overheads | seconds | 1.713152185 |
| podID | cold start | pod ID, contains the pool name (pool24-600-512) which contains pods with CPU limit 600 millicores and memory limit 512MB.  | -       | pool24-600-512-0000577863        |

## Huawei Public request tables

This table contains event-level logs of individual requests for day 30 of our dataset. Note that for Region 1, we release the top 100 pods per function. For Region 3, we also release a subsample of the data analyzed in the paper.

**Duration:** 1 day

|Metric         |Download link(s)          |
|--------------------|---------------------|
|Region 1 requests| [Region 1 part 1](https://drive.google.com/file/d/1o0xBCshTLnposeLmEzyoWn4xiqRERsmS/view?usp=drive_link), [Region 1 part 2](https://drive.google.com/file/d/101CKU4xeJWlmzxWc96RHs4llstnGnKSm/view?usp=drive_link), [Region 1 part 3](https://drive.google.com/file/d/16fNuon4FMD2QNq5S0egYWKxjkzp5lgGb/view?usp=drive_link), [Region 1 part 4](https://drive.google.com/file/d/1h-e9P2pEf9NUjv99YZLxN3ZWtwQ1rjuP/view?usp=drive_link), [Region 1 part 5](https://drive.google.com/file/d/1n4xMD5Z1EmL0ALU6D9JNZz3XGaHqtNCT/view?usp=drive_link), [Region 1 part 6](https://drive.google.com/file/d/1zn7aHFOppEltS76jHDNWWcol5zKwjDrc/view?usp=drive_link), [Region 1 part 7](https://drive.google.com/file/d/16_usg9vZpoQjzUa92RZqdZkQD05YKD5E/view?usp=drive_link), [Region 1 part 8](https://drive.google.com/file/d/1Ujo--ZO-jaF6lY9kMTmW8SPoOHh-8_NN/view?usp=drive_link), [Region 1 part 9](https://drive.google.com/file/d/1oSN7QEopQZVUNbf0wSI19Gofz-FijfQ1/view?usp=drive_link), [Region 1 part 10](https://drive.google.com/file/d/1_kAOnjD4X4ZXPAtfe3k6MOT71a4Vv953/view?usp=drive_link), [Region 1 part 11](https://drive.google.com/file/d/16DN7Kfw901_7BsT1SGf_schmDDXKCGBl/view?usp=drive_link), [Region 1 part 12](https://drive.google.com/file/d/1tlyXZ8YrzN3hFnZ3sZm3IxFsIlnyRFNI/view?usp=drive_link), [Region 1 part 13](https://drive.google.com/file/d/1eNdNmlI8764bNlMbo4_2ImlbJO52DWHg/view?usp=drive_link), [Region 1 part 14](https://drive.google.com/file/d/1zAQSWkd69GzGkxaG6Z4go0d72oeUKZZz/view?usp=drive_link), [Region 1 part 15](https://drive.google.com/file/d/1UhOBGYkntbPcLlEB3SPfLrn3aCkuqrrr/view?usp=drive_link), [Region 1 part 16](https://drive.google.com/file/d/1n0gNdAuFgJHQWtR30uSEU28Ccl_TYBP8/view?usp=drive_link), [Region 1 part 17](https://drive.google.com/file/d/1mJHff0ZaErn4qK0q9aHrfme9QhzU9352/view?usp=drive_link), [Region 1 part 18](https://drive.google.com/file/d/135Sn5elbnDZxtxplKSlobolDUO7aOhK1/view?usp=drive_link), [Region 1 part 19](https://drive.google.com/file/d/17BVGWjJaZvrZkMpqiRRgMLmPxfR_UQVH/view?usp=drive_link), [Region 1 part 20](https://drive.google.com/file/d/1GPC8s9TvhLEFbm09pPnJacxqN2vhSEeC/view?usp=drive_link) |
|Region 2 requests| [Region 2 part 1](https://drive.google.com/file/d/1clZwg5z6vAIF38K3NSkAxuzASsa5GN4B/view?usp=drive_link), [Region 2 part 2](https://drive.google.com/file/d/1S-MpmXdRSxiADKMXKlDnVdHM5Hlw2cKv/view?usp=drive_link), [Region 2 part 3](https://drive.google.com/file/d/1o4_KES_thVoC-P98uneeVbGrQH1G3VqM/view?usp=drive_link), [Region 2 part 4](https://drive.google.com/file/d/1jcFk5XBhmkwiz9EH8c69WW0BGDJ1UFeQ/view?usp=drive_link), [Region 2 part 5](https://drive.google.com/file/d/1PqeJp9DrpkD3UHHbvizPOCfNGptpRgBI/view?usp=drive_link), [Region 2 part 6](https://drive.google.com/file/d/1eT9n9yQZUeKFAyIblS0ks1XqQ_g2OJZl/view?usp=drive_link), [Region 2 part 7](https://drive.google.com/file/d/1SG7tHcuflIE-EE8AoAp99aMVqEF0vJL8/view?usp=drive_link), [Region 2 part 8](https://drive.google.com/file/d/1mCFakKPn8crcNrzFjmBttIJY7-TW3c3r/view?usp=drive_link), [Region 2 part 9](https://drive.google.com/file/d/1lW4N3SrN_z5BgjkHjU2QtDolROs8YhP5/view?usp=drive_link), [Region 2 part 10](https://drive.google.com/file/d/1TBD_1GysKZyGUaFll0qUz5FPR1gVjX0B/view?usp=drive_link)
|Region 3 requests| [Region 3 part 1](https://drive.google.com/file/d/1MxtVaHCpIdKIVk9Rz-0ySBoscXrziuP2/view?usp=drive_link), [Region 3 part 2](https://drive.google.com/file/d/1w4Zrwp_8L60TgqreBi6p0pr_sp2QmBJ2/view?usp=drive_link), [Region 3 part 3](https://drive.google.com/file/d/1KoHz5IGQuLkjtUKUlm_xAOk-wmVot6vV/view?usp=drive_link), [Region 3 part 4](https://drive.google.com/file/d/1ll08z7HqaHNuyjiwbeVcS3pqKOg_0naD/view?usp=drive_link), [Region 3 part 5](https://drive.google.com/file/d/1dgMkKTLOEDigx7-HAHdOuIF5P9d2FZon/view?usp=drive_link) |
|Region 4 requests| [Region 4 part 1](https://drive.google.com/file/d/195kYupynaq2wAz2LIDFBYLX11QXx-Yuw/view?usp=drive_link), [Region 4 part 2](https://drive.google.com/file/d/1uGoaXPEvOoCehVgHt-3cIX_QMc5qKBJ6/view?usp=drive_link)
|Region 5 requests|[Region 5](https://drive.google.com/file/d/102AFIHkEQHuvG8-hZeWHVFqXeeI-a8xS/view?usp=drive_link)|


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

**Duration:** static (valid for 31 days)


|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 2 runtimes and trigger types](https://drive.google.com/file/d/1dUg_yxeLR5OyldivPZGW5djYF31166EG/view?usp=drive_link)|Runtime languages and trigger types per function in Region 2|

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

**Duration:** 31 days

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 quantiles](https://drive.google.com/file/d/1XMSCDTRSEhJRSHA2gLuRM_WEYuuXVyWJ/view?usp=drive_link)|Region 1 quantiles|
|[Region 2 quantiles](https://drive.google.com/file/d/1iZk-n_5IT7j3M_pHpRzhwSPTuJ2vxvlR/view?usp=drive_link)|Region 2 quantiles|
|[Region 3 quantiles](https://drive.google.com/file/d/1xDPmacasZqVB_lM5UwJSiRKRNjg-ImvD/view?usp=drive_link)|Region 3 quantiles|
|[Region 4 quantiles](https://drive.google.com/file/d/1KNDZ1rHEvcfdp92xklmJFlLUPxFbQ75N/view?usp=drive_link)|Region 4 quantiles|
|[Region 5 quantiles](https://drive.google.com/file/d/1BxLz8ETUHZXbxr8PkDRFDwnBjLtCfidR/view?usp=drive_link)|Region 5 quantiles|

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
