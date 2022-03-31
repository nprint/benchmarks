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
* Metric to Optimize: recall, [r-precision](https://doi.org/10.1109/SP40000.2020.00015)

## Special Dataset Notes

The dataset contains more than 100 samples per QUIC and TCP per monitored class, around monitored 100 classes, and 3 samples per QUIC and TCP per unmonitored website.
The original evaluations were run on a subsampled dataset of *exactly* 100 samples per QUIC and TCP monitored class and 100 monitored classes, and *exactly* 3 samples per protocol per unmonitored website. 
See the [code](https://github.com/jpcsmith/wf-in-the-age-of-quic/) from the original paper for dataset cleaning and filtering.

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

| Model         | r-Precision | Recall | Code |
|:-------------:|:---------:|:------:|:----:|
| k-FP Mixed    | 90.4      | 95.0   | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| p-FP(C) Mixed | 75.9      | 67.4   | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| DF Mixed      | 51.0      | 98.4   | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
| Var-CNN Mixed | 95.8      | 93.7   | [WFAoQ](https://github.com/jpcsmith/wf-in-the-age-of-quic/)
