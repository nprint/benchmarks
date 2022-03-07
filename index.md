---
layout: default
title: Home
nav_order: 1
description: "A central repository to track progress in network traffic analysis"
permalink: /
---

# Tracking Progress in Network Traffic Analysis

The goal of this repository is to centralize, standardize, and track the progress of techniques in network traffic analysis for a variety of tasks. This repository
was modeled after the incredibly successful [nlpprogress](https://nlpprogress.com/) repository.

# Contributing

## Results  

* Results reported in published papers are preferred; an exception may be made for influential preprints.

### Adding a New Result

If you would like to add a new result, you can just click on the small edit button in the top-right corner of the file for the respective task.

This allows you to edit the file in Markdown. Simply add a row to the corresponding table in the same format. Make sure that the table stays sorted (with the best result on top). After you've made your change, make sure that the table still looks ok by clicking on the "Preview changes" tab at the top of the page. If everything looks good, go to the bottom of the page to commit the change.

Add a name for your proposed change, a description, and indicate that you would like to "Create a new branch for this commit and start a pull request", and click on "Propose file change".

## Datasets

* Must be encoded using [pcapML](https://github.com/nprint/pcapml) for standardization. *Every* packet in each dataset must be associated with a sampleID (more information [here](https://nprint.github.io/pcapml_walk.html))
* Must be accompanied by at least one result to benchmark against
* Must describe any features that cannot be used for classification (e.g. IP addresses directly identify samples)
* Must describe either the number of folds needed to benchmark against, or the training sampleIDs and testing sampleIDs if using a single data fold.
Adding a new dataset or task

### Adding a New Task or Dataset

* If the task is new, create a new task file to create a new task category ([Example here](https://raw.githubusercontent.com/nprint/benchmarks/main/application_identification/index.md))
* If not, add your dataset under the correct task using the [new dataset template](https://raw.githubusercontent.com/nprint/benchmarks/main/dataset_template.md)
* You will need to change the `nav_exclude:` parameter to `false` (or remove the parameter from the page) for the page to be listed.
* Submit the change as a pull request to the repository
