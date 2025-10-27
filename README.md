<h1 align="center" style="margin-bottom:0px; border-bottom:1px; padding-bottom:10px">Huawei Cloud Production FaaS Trace Data Releases</h1>

This repository contains public releases of Huawei Cloud production serverless FaaS traces made available to the research and academic community by Huawei's Systems Infrastructure Research (SIR) lab in Edinburgh, UK. 

These public traces are hashed versions of our raw production logs of tens of billions of user requests over multiple data centers and many months. We release them to enable researchers to conduct realistic simulations and train machine learning models to improve scheduling and resource allocation in cloud platforms. 

The data is analyzed in two papers:

* EuroSys 2025: <a href="https://dl.acm.org/doi/10.1145/3689031.3696073" download> ***Serverless Cold Starts and Where to Find Them***</a>
    * Links to our paper PDF: [![paper](https://img.shields.io/static/v1?label=arXiv&message=2410.06145&color=B31B1B&logo=arXiv)](https://arxiv.org/abs/2410.06145) [![ACM](https://img.shields.io/static/v1?label=ACM&message=10.1145/3689031.3696073&color=00599C&logo=acm&logoColor=white)](https://dl.acm.org/doi/10.1145/3689031.3696073) [![GitHub](https://img.shields.io/static/v1?label=GitHub&message=PDF&color=181717&logo=github)](https://github.com/sir-lab/data-release/blob/edits/papers/Serverless_Cold_Starts_and_Where_to_Find_Them_EuroSys_2025.pdf) 

* ACM SoCC 2023: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ***How Does It Function? Characterizing Long-term Trends in Production Serverless Workloads***</a> 
    <!-- * Links to our paper PDF: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ACM Library</a>, <a href="https://arxiv.org/abs/2312.10127" download> arXiv</a>, <a href="https://github.com/sir-lab/data-release/blob/main/papers/SoCC_2023_How_does_it_function.pdf" download> GitHub</a> -->
    * Links to our paper PDF: [![paper](https://img.shields.io/static/v1?label=arXiv&message=2312.10127&color=B31B1B&logo=arXiv)](https://arxiv.org/abs/2312.10127) [![ACM](https://img.shields.io/static/v1?label=ACM&message=10.1145/3620678.3624783&color=00599C&logo=acm&logoColor=white)](https://dl.acm.org/doi/10.1145/3620678.3624783) [![GitHub](https://img.shields.io/static/v1?label=GitHub&message=PDF&color=181717&logo=github)](https://github.com/sir-lab/data-release/blob/main/papers/SoCC_2023_How_does_it_function.pdf) 
    * Conference video presentation: [![YouTube](https://img.shields.io/static/v1?label=YouTube&message=Video&color=FF0000&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=fNhd7vIJgRc) [![BiliBili](https://img.shields.io/static/v1?label=BiliBili&message=Video&color=00A1D6&logo=bilibili&logoColor=white)](https://www.bilibili.tv/en/video/4789602907980800)

## How to download the data

The datasets used in our papers can be downloaded at the links below.
* <a href="https://github.com/sir-lab/data-release/blob/main/README_data_release_2025.md"> Huawei Public cold start traces 2025</a> contains 85 billion raw user requests and 11.9 cold start events in 5 regions. There are 19 metrics per function over 31 days, as well as aggregated time series formats for convenience. 
* <a href="https://github.com/sir-lab/data-release/blob/main/README_data_release_2023.md"> Huawei Public and Public traces 2023</a> contains 1.4 trillion function requests in time series format. There are 8 metrics per function over 235 days at per-minute and per-second granularity for two serverless platforms.

In some cases, you may not need all files in a zip folder. You can use <a href='https://www.7-zip.org/download.html'> 7zip</a> to drag and drop the desired files or directories without extracting the entire archive. 

## Code

To get started using the datasets, look at our notebooks for tips on how to load files and visualize the data.
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_cold_start.ipynb"> Huawei Public cold starts 2025 notebook</a>
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_private.ipynb"> Huawei Private 2023 notebook</a>
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_public.ipynb"> Huawei Public 2023 notebook</a>

To run our notebooks with the required packages installed, you can install our conda environment as follows:

```bash
conda env create -f environment.yml
conda activate trace-analysis
```

## Contact us

We welcome feedback, collaboration, or questions. Feel free to open an [Issue](https://github.com/sir-lab/data-release/issues).

These traces and associated research result from a collaboration between the Systems Infrastructure Research (SIR) lab in Edinburgh (part of Huawei Research UK) and Huawei's YuanRong serverless cloud platform team.

Licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.