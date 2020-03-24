# Python and Gurobi: Bakach et al. (2019), A Two-Tier Urban Delivery Network

Modeling the approach of "Bakach et al. (2019), A Two-Tier Urban Delivery Network" in Python using Gurob 9.0.1

## Setting up the working environment
* install Anaconda/Miniconda, Python and Gurobi following https://www.gurobi.com/documentation/quickstart.html (including obtaining and activating a gurobi license)
* open the conda command prompt, navigate to this repository's location and create a new conda environment. You can use the `environment.yml` file so some basic necessary packages (e.g. for the examples) will already be installed with it. (Ensure that the file is UTF-8 encoded, if problems occur)
```bash
conda env create -f environment.yml
```
* activate the the environment by running
```bash
conda activate gurobi
```
* if you have not used the environment.yml file, install the gurobipy package by running the following command in the conda shell
```bash
conda install gurobi
```
* as this repo is based on jupyter notebooks, run
```bash
jupyter notebook
```
to open the jupyter interface

## Examples
* to get familiar with the use of Gurobi and Python, follow the examples at https://www.gurobi.com/documentation/8.1/quickstart_windows/py_simple_python_example.html

* some of the examples can be found in the corresponding notebooks in the examples folder. However, they are not exactly as they are presented in the website guide but merely a few simple test snippets to get used to the gurobi modeling procedure


## Modeling the Two-Tier Urban Delivery Problem
* The models without time windows can be found in the TTUD folder (with TW is still in progress). The decision variables x of the model are based on 4 indices [hub, instance, customer, robot]. The first tier minimizes the number of necessary hubs. The second tier optimizes the necessary time by using only the minimum number of hubs as determined by tier 1
* More details are given in the notebook (markdown cells and comments)

