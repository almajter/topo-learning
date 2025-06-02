# Undergraduate Thesis – Topology of Learning in Neural Networks

This repository contains the source files for my undergraduate thesis titled:

**"Topologija učenja v nevronskih mrežah"**  
*(Topology of Learning in Neural Networks)*

---

## Project Structure

```text
.
├── thesis/          # LaTeX source for the written thesis
│   ├── main.tex
│   ├── metadata.tex
│   ├── literatura.bib
│   ├── poglavja/    # Chapters
│   └── slike/       # Figures and diagrams
│
└── topo-learning/   # Jupyter notebook for experiments
    ├── topo_learning.ipynb
    └── output/      # Plots and other artifacts
```

## GitHub Actions
GitHub Actions workflow (.github/workflows/latex.yml) automatically compiles main.tex and uploads the resulting PDF as an artifact whenever you push to or open a pull request against the main branch.

1. Lint the Workflow YAML
Before pushing changes, you verify that your workflow file is valid YAML and follows style rules:

```bash
yamllint .github/workflows/latex.yml
```
