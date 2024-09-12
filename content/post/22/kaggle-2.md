---
title: 【Kaggle】Concepts
date: 2022-08-08 00:00:00+0000
categories: 
    - nutrition
tags:
    - AI
---

Kaggle is a cloud computational environment that enables reproducible and collaborative analysis

## Types of Noteboooks

### Script

Scripts are files that execute everything as code sequentially. To start a script, click on “Create Notebook” and select “Script”. This will open the Scripts editing interface.

### Notebooks

The last type is Jupyter notebooks (usually just “notebooks”). Jupyter notebooks consist of a sequence of cells, where each cell is formatted in either Markdown (for writing text) or in a programming language of your choice (for writing code). To start a notebook, click on “Create Notebook”, and select “Notebook”. This will open the Notebooks editing interface.

## Datasets and Competitions

Data on Kaggle is available through either Datasets or our Competitions. 

There are two ways of loading a Dataset in a Notebook. The first is to navigate to a chosen dataset’s landing page, then click on the [“New Notebook” button](https://www.kaggle.com/notebooks?modal=true). This will launch a new Notebook session with the dataset in question spun up and ready to go.

Alternatively, you may wish to add datasets after creating your Notebook. To do that, navigate to the “Data” pane in a Notebook editor and click the “Add Data” button. This will open a modal that lets you select Datasets to add to your Notebook.

You will notice that there is a third option in the “Add Data” modal: Notebook Output Files.

Up to 20 GBs of output from a Notebook may be saved to disk in /kaggle/working. This data is saved automatically and you can then reuse that data in any future Notebook: just navigate to the “Data” pane in a Notebook editor, click on “Add Data”, click on the "Notebook Output Files" tab, find a Notebook of interest, and then click to add it to your current Notebook.

By chaining Notebooks as data sources in this way, it’s possible to build **pipelines** and generate more and better content than you could in a single notebook alone.

## Editor

Kaggle Notebooks may be created and edited via the Notebook editor. On larger screens, the Notebook editor consists of three parts:

- An editing window
- A console
- A settings window

## Collaboration

From your Notebook editor or viewer, public or private, you may navigate to the 'Share' or 'Sharing' button in the Notebook’s menu to expose, among other settings, the Collaborators options. There, use the search box to find and add other users as Notebook collaborators.

If your Notebook is private, you may choose between giving Collaborators either viewing privileges (“Can view”) or editing privileges (“Can edit”). If your Notebook is public, Collaborators can only be added with editing privileges (“Can edit”), as anyone can view it already.

When you add a collaborator, they will receive a notification via email.

Your Notebook collaborators won’t automatically have the same access to any private Datasets as you unless they are explicitly invited to collaborate on the Dataset. Anyone has access to Datasets shared publicly.

## Environment

Notebooks is more than just a code editor. It’s a versioned computational environment designed to make it easy to reproduce data science work. In the Notebooks IDE, you have access to an interactive session running in a Docker container with pre-installed packages, the ability to mount versioned data sources, customizable compute resources like GPUs, and more.

### Modifying a Notebook-specific Environment

It is also possible to modify the Docker container associated with the current Notebook image.

#### Using a standard package installer

In the Notebook Editor, **make sure "Internet" is enabled** in the Settings pane (it will be by default if it's a new notebook).

For Python, you can **run** **arbitrary shell commands** **by prepending ! to a code cell**. For instance, to install a new package using pip, run `!pip install my-new-package`. You can also upgrade or downgrade an existing package by running `!pip install my-existing-package==X.Y.Z`.

