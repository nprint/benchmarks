# Tracking Progress in Network Traffic Analysis

The goal of this repository is to centralize, standardize, and track the progress of techniques in network traffic analysis for a variety of tasks.

# Contributing

## Results  

* Results reported in published papers are preferred; an exception may be made for influential preprints.

### Adding a New Result

If you would like to add a new result, you can just click on the small edit button in the top-right corner of the file for the respective task (see below).

This allows you to edit the file in Markdown. Simply add a row to the corresponding table in the same format. Make sure that the table stays sorted (with the best result on top). After you've made your change, make sure that the table still looks ok by clicking on the "Preview changes" tab at the top of the page. If everything looks good, go to the bottom of the page, where you see the below form.

Fill out the file change information

Add a name for your proposed change, an optional description, indicate that you would like to "Create a new branch for this commit and start a pull request", and click on "Propose file change".

## Datasets

* Must be encoded using [pcapML](https://github.com/nprint/pcapml) for standardization. *Every* packet in each dataset must be associated with a sampleID (more information [here](https://nprint.github.io/pcapml_walk.html))
* Must be accompanied by at least one result to benchmark against
* Must describe any features that cannot be used for classification (e.g. IP addresses directly identify samples)
* Must describe either the number of folds needed to benchmark against, or the training sampleIDs and testing sampleIDs if using a single data fold.
Adding a new dataset or task


### Adding a New Task or Dataset

* If the task is new, create a new file and link to it in the table of contents.
* If not, add your dataset to the respective section of the corresponding file (in alphabetical order).
* Describe the dataset, task, and include download and citation links
* Copy the table below and fill int he first result for the dataset. A single score metric to optimize for is preferred.
* Submit the change as a pull request to the repository

| Model | Score | Paper | Code |
|:-----:|:-----:|-------|------|
|       |       |       |      |