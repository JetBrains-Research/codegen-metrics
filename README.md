# Evaluation of metrics for code generation
This is a replication package for our work on evaluation of code generation metris.
* Library for computation of code generation metrics is [available on PyPi](https://pypi.org/project/codegen-metrics/)
  * `pip install codegen-metrics`
* Pre-print is available on [arXiv](https://arxiv.org/abs/2208.03133v1)
* The article is [to be published soon in Journal of Systems and Software](https://www.sciencedirect.com/science/article/abs/pii/S016412122300136X)

## Setup

We use poetry to manage the environment and library versions. 
1. You can find the installation manual [here](https://python-poetry.org/docs/).
2. Run `poetry install` to setup the environment.

To run grading scripts you will also need to install `tkinter`. 
- For linux users: `sudo apt-get install python3-tk`. 
- For Mac users: `brew install python-tk@3.9`

To run metric computations, you will also need [tree-sitter](https://github.com/tree-sitter/tree-sitter). 
- To use it, run `git clone https://github.com/tree-sitter/tree-sitter-python.git build/tree-sitter-python`.
  - To make sure that you use the right version of tree, checkout the specific version:
  - `cd build/tree-sitter-python && git checkout 9e53981` 

## Repository structure

We expect all scripts to be run from the root directory of this repository.

- `metrics_evaluation/grading` contains Python scripts that run simple GUI for grading HS and Conala datasets
- `metrics_evaluation/metrics` contains code to run all the metrics studied in our work. For usage examples refer to `02-compute-metrics.ipynb`
- `metrics_evaluation/metrics` contains code for bootstrapping and analysis. It is further used in `03-bootstrap.ipynb`
- `data` directory contains all the data: intentions, generations from all models, human grades, etc.

## Cite as
```
@article{evtikhiev2023metrics,
title = {Out of the BLEU: How should we assess quality of the Code Generation models?},
journal = {Journal of Systems and Software},
pages = {111741},
year = {2023},
issn = {0164-1212},
doi = {https://doi.org/10.1016/j.jss.2023.111741},
url = {https://www.sciencedirect.com/science/article/pii/S016412122300136X},
author = {Mikhail Evtikhiev and Egor Bogomolov and Yaroslav Sokolov and Timofey Bryksin},
keywords = {Code generation, Metrics, Neural networks, Code similarity},
}
```
