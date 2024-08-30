# Proteomics Project: Diplonema papillatum

## Introduction

This project focuses on validating unusual protein sequences, such as extensions and insertions, in the proteome of *Diplonema papillatum*, a marine eukaryotic organism with a compact yet gene-rich genome. By integrating bioinformatics and mass spectrometry approaches, this study aims to confirm the expression of these unusual regions and explore their potential functional roles. High-confidence peptide detections from mass spectrometry analyses, processed using MSFragger and Philosopher tools, provided evidence for the presence of these unique sequences.

## Objectives

1. Validate the presence of unusual protein sequences (extensions and insertions) in the proteome of *D. papillatum* using mass spectrometry and bioinformatics approaches.
2. Determine the potential functional implications of these unusual regions using protein structure and function prediction models.
3. Compare predictive regions with experimentally detected peptides to confirm their biological validity and explore their ecological roles.

## Data Sources

- **Protein Sequences from *Diplonema papillatum***: Extracted from the UniProt database and specific unpublished sources. The main file, `dp-proteome.faa`, contains 37,346 protein sequences.
- **Protein Sequences from Other Diplonemids**: `11-diplonemids.faa` contains protein sequences derived from the transcriptomes of 11 other Diplonemid species.
- **Protein Sequences from Other Eukaryotes**: `euk-nuc1.faa` includes protein sequences from selected species in the NCBI RefSeq.
- **Mass Spectrometry Data (MS)**: Collected from multiple experiments on *D. papillatum*, analyzed using MSFragger and Philosopher tools.

## Methodology

### Bioinformatics Tools and Methods

1. **DIAMOND**: Fast alignment tool for protein sequences against large databases such as UniProt. Used to identify conserved regions and potential discrepancies indicating unusual regions.
2. **MMseqs2**: Used for sequence clustering and similarity search to identify groups of similar sequences and reduce redundancy.
3. **HMMER**: Employed for Hidden Markov Model (HMM)-based sequence analysis to detect conserved motifs and subtle structural variations.
4. **MUSCLE**: Used for multiple sequence alignments to visualize conserved regions and unusual modifications, such as extensions, in homologous sequences.
5. **MSFragger and Philosopher**: Mass spectrometry tools for peptide identification and statistical validation, confirming the presence of unusual regions detected bioinformatically.

### Scripts and Software Developed

Several custom Python scripts were developed to facilitate data processing and analysis:

- **`filter_conserved.py`**: Filters conserved proteins from DIAMOND alignment results.
- **`detect_unusual_regions.py`**: Analyzes sequence alignments to identify potential insertions and extensions using MUSCLE and HMMER results.
- **`analyze_mass_spectrometry.py`**: Processes mass spectrometry data from MSFragger and Philosopher, filters peptides with high detection probability, and compares them to predictive sequences.
- **`predict_peptides.py`**: Predicts peptides localized in unusual regions of protein sequences through in-silico enzymatic digestion.
- **`compare_ms_digest.py`**: Compares predicted results from MS-Digest with detected peptides in MS-Set1 and MS-Set datasets.

## Results

The analysis confirmed the presence of several unusual protein regions in *D. papillatum*. The study detected 35 significant extensions and 28 insertions, validated through high-confidence peptide detections in mass spectrometry data. The majority of these peptides matched predicted sequences, supporting the hypothesis that these regions play a functional role in the organism's ecological adaptation.

## Challenges and Future Directions

Several challenges were encountered, including low protein abundance and suboptimal enzymatic cleavage, affecting peptide detection in mass spectrometry. Future work will focus on experimental validation of the functional roles of these unusual regions and extend proteomic analysis to different environmental conditions and related species.

## How to Use This Repository

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/EtienneNtumba/Proteomics-Project.git
   cd Proteomics-Project
