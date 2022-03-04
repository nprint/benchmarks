---
layout: default
title: Nmap Network and IoT Device Fingerprinting
parent: Remote Device Fingerprinting
has_children: false
---

# Network and IoT Device Fingerprinting

## Dataset Overview
This dataset was gathered by actively probing remote network devices across the internet using [Nmap](https://nmap.org/). Labels were gathered through a combination of SSH and Telnet banner grabs (for routers) and [Shodan](https://www.shodan.io/) (for IoT devices) 

## Task Description
The task is to use the raw packet responses from Nmap's probes to accurately classify the 15 classes of devices.

## Links and Facts
* Dataset Link: [Google Drive](https://drive.google.com/file/d/1vd38hHMB77Qk7V7Q3mXy4ucvMq0KC7Pu/view?usp=sharing)
* Dataset Size (Uncompressed): < 1GB
* Disallowed features: None
* Number of classes: 15
* pcapML metadata comment format: `sampleID,label,probe_name`
* protocols: IPv4, TCP, ICMP
* Optimization metric: balanced accuracy

## Special Dataset Notes

Device fingerprinting represents a unique task in that each packet in the dataset is a response to a specific probe. As such, each response packet in the dataset 
is named according to the probe that it was responding to. This extra information is helpful when extracting features from the dataset, and is encoded in
the pcapML metadata comment.

## Citation(s)

Routers:
```
@article{holland2020classifying,
  title={Classifying Network Vendors at Internet Scale},
  author={Holland, Jordan and Teixeira, Ross and Schmitt, Paul and Borgolte, Kevin and Rexford, Jennifer and Feamster, Nick and Mayer, Jonathan},
  journal={arXiv preprint arXiv:2006.13086},
  year={2020}
}
```

IoT:
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

|       Model      | Balanced Accuracy |                                                     Paper                                                     |                    Code                   |
|:----------------:|:--------:|:-------------------------------------------------------------------------------------------------------------:|:-----------------------------------------:|
| nPrint Autogluon |     95.4 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |
