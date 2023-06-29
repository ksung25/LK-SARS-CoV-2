# Elevated binding and functional antibody responses to SARS-CoV-2 in infants versus mothers

Caitlin I. Stoddard<sup>1</sup>, Kevin Sung<sup>2</sup>, Zak A. Yaffe<sup>1,3</sup>, Haidyn Weight<sup>1</sup>, Guillaume Beaudoin-Bussières<sup>4,5</sup>,
Jared Galloway<sup>2</sup>, Soren Gantt<sup>5,6</sup>, Judith Adhiambo<sup>7</sup>, Emily R. Begnel<sup>8</sup>, Ednah Ojee<sup>7</sup>, Jennifer Slyker<sup>8</sup>,
Dalton Wamalwa<sup>7</sup>, John Kinuthia<sup>8,9</sup>, Andrés Finzi<sup>4,5</sup>, Frederick A. Matsen IV<sup>2,10</sup>, Dara A. Lehman<sup>1,8*</sup>,
Julie Overbaugh<sup>1,2,11*</sup>

<sup>1</sup>Human Biology Division, Fred Hutchinson Cancer Center</br>
<sup>2</sup>Public Health Sciences Division, Fred Hutchinson Cancer Center</br>
<sup>3</sup>Medical Scientist Training Program, University of Washington</br>
<sup>4</sup>Centre de Recherche du CHUM, Université de Montréal</br>
<sup>5</sup>Département de Microbiologie, Infectiologie et Immunologie, Université de Montréal</br>
<sup>6</sup>Centre de Recherche du CHU Sainte-Justine, Université de Montréal</br>
<sup>7</sup>Department of Pediatrics and Child Health, University of Nairobi</br>
<sup>8</sup>Department of Global Health, University of Washington</br>
<sup>9</sup>Department of Research and Programs, Kenyatta National Hospital</br>
<sup>10</sup>Howard Hughes Medical Institute</br>
<sup>11</sup>Lead contact</br>
<sup>*</sup>Correspondence</br>

## Abstract

Infant antibody responses to viral infection can differ from those in adults. However, data on the specificity and function of severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2) antibodies
in infants, and direct comparisons between infants and adults are limited. We characterized antibody binding and functionality in convalescent plasma from postpartum women and their infants infected with
SARS-CoV-2 from a vaccine-naïve prospective cohort in Nairobi, Kenya. Antibody titers against SARS-CoV-2 Spike, receptor binding domain and N-terminal domain, and Spike-expressing cell-surface staining levels were significantly higher in infants than in mothers. Plasma antibodies from mothers and infants bound to similar regions of the Spike S2 subunit, including the fusion peptide (FP) and stem helix-heptad repeat 2. However, infants displayed higher antibody levels and more consistent antibody escape pathways in the FP region compared to mothers. Finally, infants had significantly higher levels of antibody-dependent cellular cytotoxicity (ADCC), though, surprisingly, neutralization titers between infants and mothers were similar. These results suggest infants develop distinct SARS-CoV-2 binding and functional antibody activities and reveal age-related differences in humoral immunity to SARS-CoV-2 infection that could be relevant to protection and COVID-19 disease outcomes.

## Overview
The Phage-DMS data after alignment pipeline processing, replicate selection, and calculation of enrichments and scaled differential selection, is provided in `LK_DMS_1rep_layered.phip`. The code for downstream analyses and generation of plots for some figures in the manuscript is provided here. Outputs from the Jupyter notebooks are saved to the `results/` directory.


## Environment Setup
Currently, the environment is set up with [Conda](https://docs.conda.io/en/latest/) and `pip`. Clone this repository and create the `lk-sars2-env` environment as follows:
```sh
git clone https://github.com/matsengrp/LK-SARS-CoV-2
cd LK-SARS-CoV-2
conda env create -f environment.yml
conda activate lk-sars2-env
pip install logomaker
git clone https://github.com/matsengrp/phippery
cd phippery
git checkout 3c680c3
pip install .
cd -
```

### Figure 2
The wildtype enrichments heatmap of Fig. 2A, and the summed enrichment data for Fig. 2B and Fig. 2C are generated with `PhIP_wt_analysis.ipynb`.

### Figures 3, 4, S4, S5
The logo plots and and box plots of scaled differential selection in Figs. 3A, 3B, 4A, 4B, S4, and S5 are generated with `DMS_logo_diff_sel.ipynb`. The average similarity data in Figs. 3C and 4C are generated with `DMS_avg_sim_profile.ipynb`. The pairwise similarity data in Figs. 3D and 4D are generated with `DMS_escape_compare_sims.ipynb`.

### Figure S3
The eigenassay plots from principal component analysis is generated with `PhIP_pca.ipynb`.

## Alignment Pipeline
The raw sequencing data was processed using [phip-flow](https://github.com/matsengrp/phip-flow) and [phippery](https://github.com/matsengrp/phippery) software tools. See [here](https://matsengrp.github.io/phippery/) for detailed documentation. For questions related to processing the Phage-DMS data for this manuscript, please contact Kevin Sung: ksung2 (at) fredhutch (dot) org.
