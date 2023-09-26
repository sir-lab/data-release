# Huawei Public Cloud and Huawei Private Cloud data release

This repository explains how to use the Huawei Public Cloud and Huawei Private Cloud datasets and where to download the data.

This repository explains:
* Where to download the data
* How to load the data as a Pandas DataFrame in a Jupyter Notebook
* How to make some plots of the data


## How to download the data

The datasets used in our paper can be downloaded here:

### Huawei Private
|Metric         |Minute         | Second     |
|---------------|---------------|------------|
|Requests       |[Requests per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/requests_minute.zip)             |[Requests per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/requests_second.zip)           |
|Function delay |[Function delay per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/function_delay_minute.zip) |[Function delay per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/function_delay_second.zip)     |
|Platform delay |[Platform delay per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/platform_delay_minute.zip) |[Platform delay per second](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/platform_delay_second.zip     )|
|CPU usage      |[CPU usage per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/cpu_usage_minute.zip)           |N/A      |
|Memory usage   |[Memory usage per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/memory_usage_minute.zip)     |N/A   | 
|CPU limit      |[CPU limit per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/cpu_limit_minute.zip)           |N/A      |
|Memory limit   |[Memory limit per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/memory_limit_minute.zip)     |N/A   | 
|Instances      |[Instances per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/private_dataset/instances_minute.zip)           |N/A      |  


### Huawei Public
|Metric         |Minute         |
|---------------|---------------|
|Requests       |[Requests per minute](https://sir-dataset.obs.cn-east-3.myhuaweicloud.com/datasets/public_dataset/public_dataset.zip)|



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
 
 
 
 
 

