<h1 align="center" style="margin-bottom:0px; border-bottom:1px; padding-bottom:10px">Huawei Public Cloud and Huawei Private Cloud data release 2023</h1>

This is the repository for <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ***How Does It Function? Characterizing Long-term Trends in Production Serverless Workloads***</a> published at ACM SoCC 2023. 

The paper analyzes the Huawei Public Cloud and Huawei Private Cloud datasets, which are available for download below. 

We also provide two Jupyter Notebooks that show how to load the data as a Pandas DataFrame and make plots.

### Download/read our paper

* <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ACM Library </a>
* <a href="https://arxiv.org/abs/2312.10127" download> arXiv </a>
* <a href="https://github.com/sir-lab/data-release/blob/main/papers/SoCC_2023_How_does_it_function.pdf" download> GitHub </a>

### Conference video presentation

* <a href="https://www.youtube.com/watch?v=fNhd7vIJgRc&ab_channel=ArtjomJoosen" download> YouTube </a>
* <a href="https://www.bilibili.tv/en/video/4789602907980800?bstar_from=bstar-web.ugc-video-detail.related-recommend.all" download> BiliBili </a>
  
## Code

To get started using the datasets, look at our notebooks for tips on how to load files and visualize the data.
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_private.ipynb"> Huawei Private 2023 notebook</a>
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_public.ipynb"> Huawei Public 2023 notebook</a>
  

## How to download the data

The datasets used in our paper can be downloaded here:

### Huawei Private

This dataset contains 141 days (collected over 235 days) for 200 functions from all availability zones combined of our private cloud.

|Metric         |Minute         |Second      |Description    |
|---------------|---------------|------------|---------------|
|Function ID | - | - |Unique function identifier out of 200 (0-199) |
|Timestamp | - | - | Timestamp in seconds (0-20303940) |
|Requests       |[Requests per minute](https://drive.google.com/file/d/1W9dQvqRGylfUeHJcYqWwJrpYHIsYCVq_/view?usp=drive_link)             |[Requests per second](https://drive.google.com/file/d/11XC-gLyg1hYr39qT-oKDwzkpvseRdDIv/view?usp=drive_link) | Number of function invocations |
|Function delay |[Function delay per minute](https://drive.google.com/file/d/1Ooentp5nUeC2qKig8QSvJAaRgk3Kix_v/view?usp=drive_link) |[Function delay per second](https://drive.google.com/file/d/1T_G_CRrqzYE2sGSkcnZgntygoZrxaUC0/view?usp=drive_link)     | Function execution time averaged over all pods running that function |
|Platform delay |[Platform delay per minute](https://drive.google.com/file/d/1PEHdfOdmMfzWz-MSnj5q5Zy_9kKeDRqD/view?usp=drive_link) |[Platform delay per second](https://drive.google.com/file/d/1h24PsYMXSDl7QZ7CgI1UQWfjaNe-sJRc/view?usp=drive_link)| Platform delay is scheduling time and some network overheads; averaged over all pods running that function |
|CPU usage      |[CPU usage per minute](https://drive.google.com/file/d/1K0zaP6rGi-eaH2yJvPAhEo6zNBOC-TwK/view?usp=drive_link)           |N/A      |Percentage of allocated CPU used per function averaged over all pods |
|Memory usage   |[Memory usage per minute](https://drive.google.com/file/d/1S7TnHspI4FnR5ed1eIEJWl6nlqyNw73b/view?usp=drive_link)     |N/A   | Percentage of allocated memory used per function averaged over all pods |
|CPU limit      |[CPU limit per minute](https://drive.google.com/file/d/1OX2zfHJ79ACfwrzUgBoX78r4zv7uoVmN/view?usp=drive_link)           |N/A      | Allocated CPU for all pods running that function (normalized)|
|Memory limit   |[Memory limit per minute](https://drive.google.com/file/d/1COvoR8VwQnwxstOHuJj_YjlSaMv_jDLT/view?usp=drive_link)     |N/A   | Allocated memory for all pods running that function (MB)
|Instances      |[Instances per minute](https://drive.google.com/file/d/15_YwzY7lcUnfytof9D6mY7TAJAdhOfDH/view?usp=drive_link)           |N/A      | Number of pods allocated to that function |

Note: For Huawei Private, requests, function delay, and platform delay are originally expressed per second. We provide aggregated per-minute versions of these metrics for convenience. Requests per minute are obtained by summing requests per second every 60 seconds. Function and platform delay per minute are obtained by taking the mean every 60 seconds. 


### Huawei Public

This dataset contains 26 days for 5093 functions from one availability zone of our public cloud.

|Metric         |Minute         |Description      |
|---------------|---------------|-----------------|
|Function ID | - |Unique function identifier out of 5093 (0-5092) |
|Timestamp | - | Timestamp in seconds (0-2246340) |
|Requests       |[Requests per minute](https://drive.google.com/file/d/1RfkSxt9TddpOHiybEJFwUXfWqpsJyqSK/view?usp=drive_link)| Number of function invocations |



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
