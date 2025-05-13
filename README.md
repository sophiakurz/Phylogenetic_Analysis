# Phylogenetic Analysis Pipeline

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## Overview

This repository implements an end-to-end maximum-likelihood phylogenetic analysis pipeline in Python. It takes a FASTA file of unaligned sequences, performs multiple-sequence alignment with MAFFT, infers a phylogenetic tree using IQ-TREE2 (GTR+Γ model with ultrafast bootstrap and SH‐aLRT support), and produces a publication-quality tree figure.

## Features

- **Data parsing** with Biopython
- **Alignment** via MAFFT (four threads)
- **Tree inference** with IQ-TREE2 (`-m GTR+G`, `-bb 1000`, `-alrt 1000`)
- **Visualization** using Biopython’s `Phylo` and matplotlib
- Configurable parameters via command-line flags
- Automated figure export in high resolution

## Repository Structure

```text
├── data/
│   └── sequences.fasta
├── results/
│   ├── sequences.aln.fasta
│   ├── myrun.treefile
│   └── myrun_phylogeny_final.png
├── Phylogenetic_Analysis.ipynb
├── environment.yml
├── LICENSE
└── README.md
