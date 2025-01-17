---
title: In Search For A Cure - Recommendation with Knowledge Graph on CORD-19
description: Generate an academic knowledge graph from CORD-19 dataset and Microsoft Academic Graph (MAG) & perform analytics on it
language: Python
date: 08/24/2020
---

# In Search For A Cure: Recommendation with Knowledge Graph on CORD-19  -- KDD 2020 hands-on tutorial

This page contains the instruction for Module 1 and 2 in the [KDD 2020 hands-on tutorial: cord19recommender](https://kdd2020tutorial.github.io/cord19recommender/). 

Please first follow the [environment setup instruction](https://github.com/microsoft/recommenders/tree/kdd2020_tutorial/scenarios/academic/KDD2020-tutorial) in order to complete the full hands-on tutorial. 

### Notes: 
Above environment setup is required for Module 2 and 3. 

Completion of Module 1 requires either 
* Request [Microsoft Academic Graph (MAG)](https://docs.microsoft.com/en-us/academic-services/graph/get-started-setup-provisioning),  [Project Academic Knowledge (PAK) API]( https://www.microsoft.com/en-us/research/project/academic-knowledge/) or [MAKES API](https://docs.microsoft.com/en-us/academic-services/knowledge-exploration-service/) access, OR,
* direct download processed CORD-19 MAG subgraph data.

## Module 1 - Basics of CORD-19 data set and knowledge graph

### Option 1 - Map CORD-19 and MAG (Access requests are needed.)
1. Get [CORD-19 dataset](https://www.semanticscholar.org/cord19/download) 
1. link CORD-19 to MAG on paper id: Use [Project Academic Knowledge (PAK) API](https://www.microsoft.com/en-us/research/project/academic-knowledge/) or self-hosted [MAKES API](https://docs.microsoft.com/en-us/academic-services/knowledge-exploration-service/) to [map reference string to MAG paper](https://github.com/microsoft/mag-covid19-research-examples/tree/master/src/PAK-Samples/MapReferenceToPaper)
1. Use mapped paper id ([official released CORD-19/MAG paper id mapping](https://github.com/microsoft/mag-covid19-research-examples/blob/master/src/data/releases.md)) to [get CORD-19 MAG Subgraph using PySpark](./Module1-Get-MAG-SubGraph/)

### Option 2 - Direct access to CORD-19 MAG subgraph
1. Please follow the [environment setup instruction](https://github.com/microsoft/recommenders/tree/kdd2020_tutorial/scenarios/academic/KDD2020-tutorial) to download the dataset, if you miss some steps during the hands-on tutorial, you can make it up by copying corresponding files into experiment folders.
 
1. Acceess CORD-19 papers mapped to MAG via [PAK CORD-19 closure API](https://github.com/microsoft/mag-covid19-research-examples/blob/master/src/PAK-Samples/cord-19-closure.md)

## Module 2 - Understanding contents with the aid of knowledge graph

* [CORD-19 MAG Sub-graph Analytics](./Module2-Cord19-SubGraph-Analytics/)
