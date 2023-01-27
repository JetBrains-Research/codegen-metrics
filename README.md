# Evaluation of metrics for code generation
This is a replication package for [our work](https://arxiv.org/abs/2208.03133v1) on evaluation of code generation metris.

## Setup

We use poetry to manage the environment and library versions. 
1. You can find the installation manual [here](https://python-poetry.org/docs/).
2. Run `poetry install` to setup the environment.

To run grading scripts you will also need to install `tkinter`. 
- For linux users: `sudo apt-get install python3-tk`. 
- For Mac users: `brew install python-tk@3.9`

To run metric computations, you will also need [tree-sitter](https://github.com/tree-sitter/tree-sitter). 
- To use it, run `git clone https://github.com/tree-sitter/tree-sitter-python.git build/tree-sitter-python`.

## Repository structure
- `metrics_evaluation/grading` contains Python scripts that run simple GUI for grading HS and Conala datasets
- `metrics_evaluation/metrics` contains code to run all the metrics studied in our work. For usage examples refer to `02-compute-metrics.ipynb`
- `metrics_evaluation/metrics` contains code for bootstrapping and analysis. It is further used in `03-bootstrap.ipynb`
- `data` directory contains all the data: intentions, generations from all models, human grades, etc.