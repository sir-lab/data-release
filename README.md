<h1 align="center" style="margin-bottom:0px; border-bottom:1px; padding-bottom:10px">Huawei Cloud Data Releases</h1>

This is the repository for data released from Huawei Cloud's public and private serverless cloud platforms. The data is analyzed in two papers:
* EuroSys 2025: <a href="https://github.com/sir-lab/data-release/blob/main/papers/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf" download> ***Serverless Cold Starts and Where to Find Them***</a>
    * Links to our paper PDF: <a href="https://github.com/sir-lab/data-release/blob/main/papers/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf" download> GitHub</a>

* ACM SoCC 2023: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ***How Does It Function? Characterizing Long-term Trends in Production Serverless Workloads***</a> 
    * Links to our paper PDF: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ACM Library</a>, <a href="https://arxiv.org/abs/2312.10127" download> arxiv</a>, <a href="https://github.com/sir-lab/data-release/blob/main/papers/SoCC_2023_How_does_it_function.pdf" download> GitHub</a>
  * Conference video presentation: <a href="https://www.youtube.com/watch?v=fNhd7vIJgRc&ab_channel=ArtjomJoosen" download> YouTube</a>, <a href="https://www.bilibili.tv/en/video/4789602907980800?bstar_from=bstar-web.ugc-video-detail.related-recommend.all" download> BiliBili</a>

## How to download the data

The datasets used in our papers can be downloaded at the links below.

In some cases, you may not need all files in a zip folder. In this case, use <a href='https://www.7-zip.org/download.html'> 7zip</a> to open the zipped file and drag out the files or directories you want without extracting everything. 

### Code

To get started using the datasets, look at our notebooks for tips on how to load files and visualize the data.
* Huawei Public cold starts 2025 <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_cold_start.ipynb"> notebook</a>
* Huawei Private 2023 <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_private.ipynb"> notebook</a>
* Huawei Public 2023 <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_public.ipynb"> notebook</a>


### Huawei Public cold starts (2025)

These files contain every cold start analyzed in our 2025 paper. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R1.zip)|Region 1 cold start events|
|[Region 2 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R2.zip)|Region 2 cold start events|
|[Region 3 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R3.zip)|Region 3 cold start events|
|[Region 4 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R4.zip)|Region 4 cold start events|
|[Region 5 cold starts](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/cold_start/R5.zip)|Region 5 cold start events|


### Huawei Public trigger types and runtime languages (2025)

This file contains the runtime languages, trigger types, and CPU request for each function in Region 2. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 2 runtimes and trigger types](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/runtime_triggerType/df_funcID_runtime_triggerType.csv)|Runtime languages and trigger types per function in Region 2|


### Huawei Public quantiles (2025)

These files contain the time series quantiles of different metrics on our platform per function, such as totalCost (function execution time) or cold start time. We also include the number of requests, number of pods, and number of cold starts. 

|Metric/link         |Description          |
|--------------------|---------------------|
|[Region 1 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R1.zip)|Region 1 quantiles|
|[Region 2 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R2.zip)|Region 2 quantiles|
|[Region 3 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R3.zip)|Region 3 quantiles|
|[Region 4 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R4.zip)|Region 4 quantiles|
|[Region 5 quantiles](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/quantiles/R5.zip)|Region 5 quantiles|


### Huawei Public request tables (2025)


|Metric/link         |Description          |
|--------------------|---------------------|
|Region 1 requests| Coming soon |
|Region 2 requests| Coming soon |
|Region 3 requests| Coming soon |
|Region 4 requests | [Region 4 part 1](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R4/R4_00000_00099.zip), [Region 4 part 2](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R4/R4_00100_00199.zip)
|Region 5 requests|[Region 5](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/cold_start_dataset/per_request/R5/R5.zip)|


### Huawei Private (2023)

This dataset contains 141 days (collected over 235 days) for 200 functions from all availability zones combined of our private cloud.

|Metric         |Minute         |Second      |Description    |
|---------------|---------------|------------|---------------|
|Function ID | - | - |Unique function identifier out of 200 (0-199) |
|Timestamp | - | - | Timestamp in seconds (0-20303940) |
|Requests       |[Requests per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/requests_minute.zip)             |[Requests per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/requests_second.zip) | Number of function invocations |
|Function delay |[Function delay per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/function_delay_minute.zip) |[Function delay per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/function_delay_second.zip)     | Function execution time averaged over all pods running that function |
|Platform delay |[Platform delay per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/platform_delay_minute.zip) |[Platform delay per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/platform_delay_second.zip     )| Platform delay is scheduling time and some network overheads; averaged over all pods running that function |
|CPU usage      |[CPU usage per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/cpu_usage_minute.zip)           |N/A      |Percentage of allocated CPU used per function averaged over all pods |
|Memory usage   |[Memory usage per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/memory_usage_minute.zip)     |N/A   | Percentage of allocated memory used per function averaged over all pods |
|CPU limit      |[CPU limit per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/cpu_limit_minute.zip)           |N/A      | Allocated CPU for all pods running that function (normalized)|
|Memory limit   |[Memory limit per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/memory_limit_minute.zip)     |N/A   | Allocated memory for all pods running that function (MB)
|Instances      |[Instances per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/instances_minute.zip)           |N/A      | Number of pods allocated to that function |

Note: For Huawei Private, requests, function delay, and platform delay are originally expressed per second. We provide aggregated per-minute versions of these metrics for convenience. Requests per minute are obtained by summing requests per second every 60 seconds. Function and platform delay per minute are obtained by taking the mean every 60 seconds. 


### Huawei Public (2023)

This dataset contains 26 days for 5093 functions from one availability zone of our public cloud.

|Metric         |Minute         |Description      |
|---------------|---------------|-----------------|
|Function ID | - |Unique function identifier out of 5093 (0-5092) |
|Timestamp | - | Timestamp in seconds (0-2246340) |
|Requests       |[Requests per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/public_dataset/public_dataset.zip)| Number of function invocations |


<!---
After downloading the data, the folder structure should look like this. 
```console
.
├── demo_private.ipynb
├── demo_public.ipynb
└── datasets
    ├── private_dataset
    │   ├── cpu_limit_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ... 
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── cpu_usage_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── function_delay_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── function_delay_second
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── instances_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── memory_limit_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── memory_usage_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── platform_delay_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── platform_delay_second
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   ├── requests_minute
    │   │   ├── day_000.csv
    │   │   ├── day_001.csv
    │   │   ├── ...
    │   │   ├── day_233.csv
    │   │   └── day_234.csv
    │   └── requests_second
    │       ├── day_000.csv
    │       ├── day_001.csv
    │       ├── ...
    │       ├── day_233.csv
    │       └── day_234.csv
    └── public_dataset
        └── requests_minute
            ├── day_00.csv
            ├── day_01.csv
            ├── ...
            ├── day_24.csv
            └── day_25.csv
``` 
-->

