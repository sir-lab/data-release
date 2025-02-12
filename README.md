<h1 align="center" style="margin-bottom:0px; border-bottom:1px; padding-bottom:10px">Huawei Cloud Data Releases</h1>

This is the repository for data released from Huawei Cloud's public and private serverless cloud platforms. The data is analyzed in two papers:
* EuroSys 2025: <a href="https://arxiv.org/abs/2410.06145" download> ***Serverless Cold Starts and Where to Find Them***</a>
    * Links to our paper PDF: [![paper](https://img.shields.io/static/v1?label=arXiv&message=2410.06145&color=B31B1B&logo=arXiv)](https://arxiv.org/abs/2410.06145) [![GitHub](https://img.shields.io/static/v1?label=GitHub&message=PDF&color=181717&logo=github)](https://github.com/sir-lab/data-release/blob/main/papers/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf) [![ACM](https://img.shields.io/static/v1?label=ACM&message=10.1145/3689031.3696073&color=00599C&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiIgdmlld0JveD0iMCAwIDUwIDUwIj48cGF0aCBkPSJNMTIuNSAwTDAgMTIuNSAxMi41IDI1IDAgMzcuNSAxMi41IDUwIDI1IDM3LjUgMzcuNSAxMi41IDI1IDAgMTIuNSAxMi41IDB6IiBmaWxsPSIjMDA1OTlDIi8+PHRleHQgeD0iMjUiIHk9IjMwIiBmb250LXNpemU9IjE1IiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmaWxsPSJ3aGl0ZSIgZm9udC1mYW1pbHk9IlZlcmRhbmEsIHNhbnMtc2VyaWYiPkFDTDwvdGV4dD48L3N2Zz4=)](https://dl.acm.org/doi/10.1145/3689031.3696073)



    
    
    <!-- * Links to our paper PDF: <a href="https://arxiv.org/abs/2410.06145" download> arXiv</a>, <a href="https://github.com/sir-lab/data-release/blob/main/papers/EuroSys_2025_Serverless_Cold_Starts_and_Where_to_Find_Them.pdf" download> GitHub</a> -->

* ACM SoCC 2023: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ***How Does It Function? Characterizing Long-term Trends in Production Serverless Workloads***</a> 
    * Links to our paper PDF: <a href="https://dl.acm.org/doi/10.1145/3620678.3624783" download> ACM Library</a>, <a href="https://arxiv.org/abs/2312.10127" download> arXiv</a>, <a href="https://github.com/sir-lab/data-release/blob/main/papers/SoCC_2023_How_does_it_function.pdf" download> GitHub</a>
  * Conference video presentation: <a href="https://www.youtube.com/watch?v=fNhd7vIJgRc&ab_channel=ArtjomJoosen" download> YouTube</a>, <a href="https://www.bilibili.tv/en/video/4789602907980800?bstar_from=bstar-web.ugc-video-detail.related-recommend.all" download> BiliBili</a>

## How to download the data

The datasets used in our papers can be downloaded at the links below.
* <a href="https://github.com/sir-lab/data-release/blob/main/README_data_release_2025.md"> Huawei Public cold start traces 2025</a> contains time series of 19 metrics per function over 31 days for 5 regions, as well as per-event tables of requests and cold starts.
* <a href="https://github.com/sir-lab/data-release/blob/main/README_data_release_2023.md"> Huawei Public and Public traces 2023</a> contains time series of 8 metrics per function over 235 days at per-minute and per-second granularity for two serverless platforms.

In some cases, you may not need all files in a zip folder. You can use <a href='https://www.7-zip.org/download.html'> 7zip</a> to drag and drop the desired files or directories without extracting the entire archive. 

### Code

To get started using the datasets, look at our notebooks for tips on how to load files and visualize the data.
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_cold_start.ipynb"> Huawei Public cold starts 2025 notebook</a>
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_private.ipynb"> Huawei Private 2023 notebook</a>
* <a href="https://github.com/sir-lab/data-release/blob/main/src/demo_public.ipynb"> Huawei Public 2023 notebook</a>
