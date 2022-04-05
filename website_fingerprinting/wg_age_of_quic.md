---
layout: default
title: joint quic-tcp website fingerprinting
parent: Website Fingerprinting
has_children: false
nav_exclude: false
---

# Joint QUIC-TCP Website Fingerprinting

## Dataset Overview

This dataset was gathered by downloading the index pages of around 16,000 websites from the [Alexa Top 1M](https://www.alexa.com/topsites), [Cisco Umbrella](http://s3-us-west-1.amazonaws.com/umbrella-static/index.html), and [Majestic Million](https://majestic.com/reports/majestic-million) lists,
using the Chromium web-browser, and over encrypted wireguard tunnels with gateways in New York, U.S.A.; Frankfurt, Germany; and Bengaluru, India.
The traces, which were collected at the client, contain encrypted wireguard packets. 

## Task Description

The task is to identify the visited website given traces which may have been collected using HTTP/QUIC or using HTTP/TCP.

## Links and Facts
* Dataset Link: Due to size, available upon request.
* Dataset Size (Uncompressed): 69 GB
* Disallowed Features: None
* Number of Classes: 101
* pcapML Metadata Comment Format: `sampleID,final URL;original URL;tcp or quic;VPN location`
* Protocols: Ethernet, IP, UDP, Wireguard
* Metric to Optimize: F<sub>1,r</sub>-score (see notes below)

## Special Dataset Notes

The dataset contains more than 100 samples per QUIC and TCP per monitored class, around monitored 100 classes, and 3 samples per QUIC and TCP per unmonitored website.
The original evaluations were run on a subsampled dataset of *exactly* 100 samples per QUIC and TCP monitored class and 100 monitored classes, and *exactly* 3 samples per protocol per unmonitored website. 
See the [code](https://github.com/jpcsmith/wf-in-the-age-of-quic/) from the original paper for dataset cleaning and filtering.

The F<sub>1,r</sub>-score is the F<sub>1</sub>-score calculated using the r-precision score of [Wang et al. (2020)](https://doi.org/10.1109/SP40000.2020.00015). It is calculated as

<img src="https://render.githubusercontent.com/render/math?math=F_{1,r}=\frac{2}{\text{recall}^{-1}%2B\text{r-precision}^{-1}}">

The F<sub>1,r</sub>-scores below were calculated with an r-value of 20.

## Citation(s)

```
@InProceedings{smith2021website,
    author = {Jean-Pierre Smith and Prateek Mittal and Adrian Perrig},
    title = {Website fingerprinting in the age of {QUIC}},
    booktitle = {Proceedings on Privacy Enhancing Technologies (PoPETs)},
    year = 2021,
    month = jul,
    doi = {10.2478/popets-2021-0017},
    keywords = {privacy},
}
```

# Leaderboard
___

| Model         | F<sub>1,r</sub>-score | Paper |  Code |
|:-------------:|:----:|:----:|:------:|
| k-FP Mixed    | 92.6 | [PoPETs 2021](https://doi.org/10.2478/popets-2021-0017) | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| p-FP(C) Mixed | 71.4 | [PoPETs 2021](https://doi.org/10.2478/popets-2021-0017) | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| DF Mixed      | 67.2 | [PoPETs 2021](https://doi.org/10.2478/popets-2021-0017) | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| Var-CNN Mixed | 94.7 | [PoPETs 2021](https://doi.org/10.2478/popets-2021-0017) | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
