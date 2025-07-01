# 🧬 Genome Annotation Pipeline Using MAKER

This repository provides a modular and reproducible workflow for eukaryotic genome annotation using [MAKER](http://www.yandell-lab.org/software/maker.html). It integrates tools like RepeatModeler, RepeatMasker, SNAP, Augustus, and BUSCO to identify genes and annotate features.

## 📦 Features

- Repeat annotation and masking (de novo and taxon-based)
- Protein and transcript homology support
- ab initio gene prediction with SNAP and Augustus
- AED filtering, BUSCO evaluation
- Optional sample data folder for testing

## 🚀 Quickstart

1. **Clone the repository and set up the environment**:
   ```bash
   git clone https://github.com/yourusername/genome-annotation-maker.git
   cd genome-annotation-maker

   conda create -n maker_env maker=3.01.03 -c bioconda
   conda activate maker_env
   conda install repeatmodeler repeatmasker busco bedtools seqtk seqkit datamash
   ```

2. **Place your input files** into a new `data/` directory:
   ```
   mkdir data
   cp path/to/genome.fasta data/
   cp path/to/proteins.fasta data/
   cp path/to/transcripts.fasta data/
   cp path/to/te_proteins.fasta data/
   ```   

4. **Follow the pipeline steps** in [GENOME_ANNOTATION.md](https://gist.github.com/kmsshafi/def2d1184e15a5b865471a08c44aa8e3)

5. **Expected output structure** (generated after running the pipeline):
   ```
   .
   ├── data/                       # Input genome, proteins, transcripts
   ├── 01_simple/, ..., 05_full/  # RepeatMasker outputs
   ├── round1.maker.output/       # MAKER round 1
   ├── round2.maker.output/       # MAKER round 2
   ├── snap/                      # SNAP training output
   ├── logs/                      # Log files from various steps
   ├── README.md
   └── .gitignore
   ```

## 📜 License & Acknowledgments

This repository wraps third-party bioinformatics tools. Please cite and acknowledge all tools (MAKER, RepeatMasker, Augustus, SNAP, BUSCO, etc.) used in your analyses.
