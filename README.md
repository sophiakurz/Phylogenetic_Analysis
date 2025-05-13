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
.
├── data/
│   └── sequences.fasta             # Unaligned input sequences
├── results/
│   ├── sequences.aln.fasta         # MAFFT alignment
│   ├── myrun.treefile              # IQ-TREE2 output (Newick with supports)
│   └── myrun_phylogeny_final.png   # Final tree image
├── scripts/
│   ├── align.py                    # MAFFT wrapper script
│   ├── infer_tree.py               # IQ-TREE2 wrapper script
│   └── plot_tree.py                # Tree visualization script
├── environment.yml                 # Conda environment spec
├── LICENSE
└── README.md

