---
layout: default
title: netml vpn-nonvpn
parent: Application Identification
has_children: false
---

# netML VPN-nonVPN Application Identification

## Dataset Overview

This dataset focuses on detecting applications in traffic flows. The dataset was created using a subset of the [VPN-nonVPN dataset](https://www.unb.ca/cic/datasets/vpn.html). While the original dataset was released as features for the
[netML challenge](https://arxiv.org/pdf/2004.13006.pdf), the dataset below represents a faithful recreation of the netML malware dataset at the raw
network packet level. Although the dataset doesn't perfectly match the original netML challenge, it is used in the nPrint paper and to generate the nPrint results 
in the leaderboard.

## Task Description

The task is to identify the application of each traffic flow sample in the dataset.

## Links and Facts
* Dataset Link: [Google Drive](https://drive.google.com/file/d/1uEbrL9fl1kd5hDCziSjTEnzbtXUZYIdM/view?usp=sharing)
* Dataset Size (Uncompressed): < 1 GB
* Disallowed Features: None
* Number of Classes: 7 (easy) 18 (medium), 31 (hard)
* pcapML Metadata Comment Format: `sampleID,easylabel_mediumlabel_hardlabel`
* Protocols: IPv4, TCP, UDP
* Metric to Optimize: Balanced Accuracy

## Special Dataset Notes

None.

## Citation(s)

original netML release
```
@article{barut2020netml,
  title={Netml: A challenge for network traffic analytics},
  author={Barut, Onur and Luo, Yan and Zhang, Tong and Li, Weigang and Li, Peilong},
  journal={arXiv preprint arXiv:2004.13006},
  year={2020}
}
```

nPrint release

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

## Easy

|           Model           | Balanced Accuracy |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              81.9 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |

## Medium

|           Model           | Balanced Accuracy |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              66.2 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |

## Hard

|           Model           | Balanced Accuracy |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              60.9 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |
