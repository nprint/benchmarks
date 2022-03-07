---
layout: default
title: mobile country of origin
parent: Application Identification
has_children: false
---

# Cross Market Mobile Country of Origin

## Dataset Overview

This dataset is created from a subset of the [Cross Market](https://recon.meddle.mobi/papers/cross-market.pdf) mobile application dataset. The dataset was
originally gathered to examine the privacy of the 100 most popular iOS and Android applications in India, China, and the US. In this dataset, the same applications
network captures are used but with the goal of deteremining the country of origin of the application.

## Task Description

The task is to determine the country of origin of each mobile application in a given application traffic trace (US, China, or India).

## Links and Facts
* Dataset Link: [Google Drive](https://drive.google.com/file/d/1QRRY5gPPrZ9keOdDORmuGStVjFGapuMn/view?usp=sharing)
* Dataset Size (Uncompressed): < 10 GB
* Disallowed Features: None
* Number of Classes: 3
* pcapML Metadata Comment Format: `sampleID,label`
* Protocols: IPv4, TCP, UDP, Payloads
* Metric to Optimize: Balanced Accuracy

## Special Dataset Notes

None.

## Citation(s)

Original Dataset
```
@article{crossmarketdataset,
    title={An International View of Privacy Risks for Mobile Apps},
    author={Ren, Jingjing and Dubois, Daniel J. and Choffnes, David},
    url={https://recon.meddle.mobi/papers/cross-market.pdf},
    year={2019}
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

|           Model           | Balanced Accuracy |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              96.8 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |
