# Topology of Learning in Artificial Neural Networks (Adaptation)

This repository is an adapted and extended version of the original code from the paper: [Topology of Learning in Artificial Neural Networks](https://arxiv.org/abs/1902.08160)

## Goal

The goal is to analyze the **evolution of neural network weights during training** using techniques from **topological data analysis (TDA)** — primarily the **Mapper algorithm** and **persistent homology**.

## Content

- Trained a fully connected neural network on a **filtered version of MNIST**, containing only digits **3** and **5** (binary classification).
- Extracted weight vectors across all layers and across training steps.
- Constructed **Mapper graphs** from these weights to study their topological organization over time.
- Used several **lens functions (projections)** to generate Mapper graphs:
  - `l2norm`
  - `PCA`
  - `t-SNE`
- Analyzed each layer **independently**, to trace how structure emerges in deeper layers.
- Computed **persistent homology** (H₀, H₁, H₂) of the weight vectors using `giotto-tda` to quantify topological complexity.
- Visualized **persistence diagrams** for deeper interpretation.


## Initialize project 
- `uv init --bare`
- `uv venv`

## Local Setup
Dependencies are declared in `pyproject.toml`.

### Prerequisites

- [Install pyenv](https://github.com/pyenv/pyenv#installation)
- [Install uv](https://astral.sh/uv)

### Setup Instructions

1. Install and activate the Python version:
   - `pyenv install 3.10`
   - `pyenv local 3.10`

2. Create and activate a virtual environment:
   - `uv venv`
   - `source .venv/bin/activate`

3. Install dependencies from `pyproject.toml`:
   - `uv pip install -e .`

4. Run your script:
   - `uv run jupyter notebook topo_learning.py`

### Managing Dependencies

- Add a new package: `uv add <package-name>`

### Clean Up

- Remove the environment: `rm -rf .venv`