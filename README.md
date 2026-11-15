# OpenBioHackathon – Track 01

**Question:** Do early-onset and late-onset preeclampsia tell different biological stories?

## Data
- Placenta bulk RNA-seq counts + metadata (`track01_counts_vt.csv`, `track01_metadata_vt.csv`)
- Single-cell pseudobulk by donor, from Admati, Skarbianskis et al. ([figshare](https://figshare.com/articles/dataset/Placenta_PE_single_cell_RNAseq_dataset_Admati_Skarbianskis_et_al_/23264102), CC BY 4.0)
- Data files come from [openbio-datathon-2026](https://github.com/Harvard-Undergraduate-OpenBio/openbio-datathon-2026) (`track-01/data`); not included here.

## Run
Open `track01_workflow.ipynb` in Google Colab (setup is automatic) or place it in `track-01/notebooks/` of the datathon repo. Run top to bottom.

Requires: `pydeseq2`, `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `matplotlib-venn`

## Analyses
| Comparison | Data | Covariates |
|---|---|---|
| PE vs no PE | Bulk | gestational age, maternal age |
| Early vs late PE | Pseudobulk (donor) | maternal age |
| Late PE vs control | Pseudobulk (donor) | maternal age |
| Early PE vs control | Pseudobulk (donor) | maternal age |

Cutoffs: padj < 0.05, |log2FC| ≥ 0.5. Each donor counts once; early-onset comparisons are exploratory (small groups).

## Key results
- **PE vs no PE:** 836 genes passed (512 up, 324 down). Top: SERPINA3, ENG, HTRA4 (all up in PE).
- **Marker overlap:** KLRD1 ↓, KIT ↑ (decidual NK); CLDN5 ↑ (endothelial); PDGFRB ↑ (perivascular); CGA ↑ (syncytiotrophoblast).
- **Early vs late PE:** SGOL2 and UHRF1 up in early-onset, with BUB1B, NEK2, AURKA, suggesting more proliferating cells.

## Outputs (`results/`)
DE tables, passing-gene lists, up/down gene lists for DAVID, volcano plots, Venn diagrams of overlapping genes.
