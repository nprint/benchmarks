---
layout: default
title: nPrint Streaming Video Services
parent: Application Identification
has_children: false
---

# nPrint Streaming Video Services

## Dataset Overview

This dataset was derived from the video services dataset released by [Bronzino et. al.](https://dl.acm.org/doi/abs/10.1145/3366704)They captured and labeled a large number of video streaming sessions from
a number of vantage points. This dataset is filtered to contain only the first 10 SYN packets (flow creation) for each video session, with the goal being to identify
the streaming service using these packets.

## Task Description

The task is to identify the video service which generated the SYN packets in a given video session.

## Links and Facts
* Dataset Link: [Google Drive](link)
* Dataset Size (Uncompressed): < 2 GB
* Disallowed Features: None
* Number of Classes: 4
* pcapML Metadata Comment Format: `sampleID,label`
* Protocols: IPv4, TCP
* Metric to Optimize: Balanced Accuracy

## Special Dataset Notes

IPs have been cryptopanned for release.

## Citation(s)

Original Dataset
```
@article{10.1145/3366704,
author = {Bronzino, Francesco and Schmitt, Paul and Ayoubi, Sara and Martins, Guilherme and Teixeira, Renata and Feamster, Nick},
title = {Inferring Streaming Video Quality from Encrypted Traffic: Practical Models and Deployment Experience},
year = {2019},
issue_date = {December 2019},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3366704},
doi = {10.1145/3366704},
}
```

nPrint Filtered Dataset
```
@inproceedings{10.1145/3460120.3484758,
author = {Holland, Jordan and Schmitt, Paul and Feamster, Nick and Mittal, Prateek},
title = {New Directions in Automated Traffic Analysis},
year = {2021},
isbn = {9781450384544},
url = {https://doi.org/10.1145/3460120.3484758},
doi = {10.1145/3460120.3484758},
series = {CCS '21}
}
```

# Leaderboard
___

|           Model           | Balanced Accuracy |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              77.9 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |
