---
layout: default
title: snowflake fingerprintability
parent: Application Identification
has_children: false
---

# Snowflake Fingeprintability

## Dataset Overview

Tor is the most well-known tool for circumventing censorship. Unfortunately, Tor traffic has been shown to be detectable using deep-packet inspection. 
WebRTC is a popular web frame-work that enables browser-to-browser connections. Snowflake is a novel pluggable transport that leverages WebRTC to connect Tor clients to the Tor network. 
In theory, Snowflake was created to be indistinguishable from other WebRTC services. We evaluate the indistinguishability of Snowflake. 
We collect over 6,500 DTLS handshakes from Snowflake, Facebook Messenger, Google Hangouts, and Discord WebRTC connections. The dataset listed here further splits 
these handshakes into the browser that was useed to capture the traffic, either Google Chrome or Firefox, resulting in 7 classes of traffic.

## Task Description

The task is to classify the (browser, application) tuple in each DTLS handshake in the datset.

## Links and Facts
* Dataset Link: [Google Drive](https://drive.google.com/file/d/1QYPXemuoU7obtJZdL3MAmIxgFLraR0S8/view?usp=sharing)
* Dataset Size (Uncompressed): < 1GB 
* Disallowed Features: None
* Number of Classes: 7
* pcapML Metadata Comment Format: `sampleID,label`
* Protocols: IPv4, UDP, DTLS
* Metric to Optimize: Macro F1

## Special Dataset Notes

None

## Citation(s)

Original Release
```
@article{macmillan2020evaluating,
title={Evaluating snowflake as an indistinguishable censorship circumvention tool},
author={MacMillan, Kyle and Holland, Jordan and Mittal, Prateek},
journal={arXiv preprint arXiv:2008.03254},
year={2020}
}
```

Subsequent Dataset Release (Fine-grained Classes)
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

|           Model           | Macro F1 |                                                      Paper                                                     |                    Code                    |
|:-------------------------:|:-----------------:|:--------------------------------------------------------------------------------------------------------------:|:------------------------------------------:|
| nPrint Autogluon (AutoML) |              99.8 | [CCS 2021](https://dl.acm.org/doi/abs/10.1145/3460120.3484758) - [Arxiv](https://arxiv.org/pdf/2008.02695.pdf) | [nPrint](https://github.com/nprint/nprint) |
