# 🧬 Genome Annotation Pipeline Using MAKER

This repository provides a modular and reproducible workflow for eukaryotic genome annotation using [MAKER](http://www.yandell-lab.org/software/maker.html). It integrates tools like RepeatModeler, RepeatMasker, SNAP, Augustus, and BUSCO to identify genes and annotate features.

## 📦 Features

- Repeat annotation and masking (de novo and taxon-based)
- Protein and transcript homology support
- ab initio gene prediction with SNAP and Augustus
- AED filtering, BUSCO evaluation
- Optional sample data folder for testing

## 📁 Folder Structure

```
.
├── GENOME_ANNOTATION.md      # Detailed pipeline instructions
├── sample_data/              # Optional test FASTA/protein files
├── logs/                     # Output logs
├── 01_simple/, ..., 05_full/ # RepeatMasker output stages
├── round1.maker.output/      # MAKER output round 1
└── round2.maker.output/      # MAKER output round 2
```

## 🚀 Quickstart

1. Clone this repository and install dependencies:
```bash
conda create -n maker_env maker=3.01.03 -c bioconda
conda activate maker_env
```

2. Place your genome and evidence files in `data/`.

3. Follow the steps in [GENOME_ANNOTATION.md](https://gist.github.com/kmsshafi/def2d1184e15a5b865471a08c44aa8e3) to run the pipeline.

## 🧪 Sample Data

Sample input files are available in the `sample_data/` directory for testing the pipeline.

## 📜 License & Acknowledgments

This repository wraps third-party bioinformatics tools. Please cite and acknowledge all tools (MAKER, RepeatMasker, Augustus, SNAP, BUSCO, etc.) used in your analyses.
