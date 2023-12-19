# Huawei Public Cloud and Huawei Private Cloud data release

This is the repository for <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ***How Does It Function? Characterizing Long-term Trends in Production Serverless Workloads***</a> published at ACM SoCC 2023. 

The paper analyzes the Huawei Public Cloud and Huawei Private Cloud datasets, which are available for download below. 

We also provide two Jupyter Notebooks that show how to load the data as a Pandas DataFrame and make plots.

### Download/read our paper

* <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ACM Library </a>
* <a href="https://arxiv.org/abs/2312.10127" download> arxiv </a>
* <a href="https://github.com/sir-lab/data-release/blob/main/SoCC_2023_How_does_it_function.pdf" download> GitHub </a>

### Conference video presentation

* <a href="https://www.youtube.com/watch?v=fNhd7vIJgRc&ab_channel=ArtjomJoosen" download> YouTube </a>
* <a href="https://www.bilibili.tv/en/video/4789602907980800?bstar_from=bstar-web.ugc-video-detail.related-recommend.all" download> BiliBili </a>

## How to download the data

The datasets used in our paper can be downloaded here:

### Huawei Private

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


### Huawei Public

This dataset contains 26 days for 5093 functions from one availability zone of our public cloud.

|Metric         |Minute         |Description      |
|---------------|---------------|-----------------|
|Function ID | - |Unique function identifier out of 5093 (0-5092) |
|Timestamp | - | Timestamp in seconds (0-2246340) |
|Requests       |[Requests per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/public_dataset/public_dataset.zip)| Number of function invocations |



After downloading the data, the folder structure should look like this. 
```console
.
├── demo_private.ipynb
├── demo_public.ipynb
└── datasets
    ├── private_dataset
    │   ├── cpu_limit_minute
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
