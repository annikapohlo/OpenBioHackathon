Marker genes of proliferating cells in the preeclamptic placenta
---
By: Christine Le, Annika Pohlo, Jessica Li
---
| gene | baseMean | log2FC | lfcSE | stat | pvalue | padj |
|------|----------|--------|-------|------|--------|------|
| ENG | 6068.65 | 2.00 | 0.21 | 9.61 | 7.35e-22 | 1.22e-17 |
| SERPINA3 | 418.56 | 6.02 | 0.69 | 8.72 | 2.87e-18 | 2.39e-14 |
| HTRA4 | 7503.86 | 2.69 | 0.35 | 7.66 | 1.93e-14 | 1.07e-10 |
| AMD1 | 3435.43 | 0.81 | 0.11 | 7.39 | 1.42e-13 | 5.90e-10 |
| ABCA7 | 161.83 | 1.36 | 0.19 | 7.19 | 6.32e-13 | 2.10e-09 |
| GPIHBP1 | 83.04 | 1.93 | 0.27 | 7.02 | 2.22e-12 | 6.17e-09 |
| ERO1A | 1289.96 | 1.31 | 0.19 | 6.76 | 1.34e-11 | 2.48e-08 |
| TMEM45A | 279.25 | 2.06 | 0.30 | 6.77 | 1.25e-11 | 2.48e-08 |
| PAM | 6397.76 | 0.94 | 0.14 | 6.78 | 1.19e-11 | 2.48e-08 |
| PRRG1 | 919.37 | 0.90 | 0.13 | 6.68 | 2.41e-11 | 3.56e-08 |
---
Figure 1. Table of the top 10 differentially expressed genes. baseMean is a gene’s average normalized count across all samples, roughly how many reads it gets in a typical sample. The highlighted gene, GPIHBP1, has a moderate base mean. 


Preeclampsia is one of the leading causes of maternal and infant illness and mortality, affecting an estimated 2-8% of all pregnancies worldwide. It is characterized by high blood pressure, high levels of protein in urine that indicate kidney damage, or other signs of organ damage. Often classified into two categories, we examine whether early-onset preeclampsia and late-onset preeclampsia tell different biological stories. 

Our data comes from a public study of 30 placentas collected at delivery. From these placentas, researchers took a piece of villous tissue, the part of the placenta that exchanges nutrients with the mother’s blood. Bulk RNA sequencing was then used to measure a whole tissue piece at once. Then, from the metadata table describing the pregnancy, we compared two groups. Our group column was the preeclampsia status of the pregnancy; the control was no preeclampsia, and the case was those with preeclampsia. Our covariates were the weeks of pregnancy at delivery and maternal age. Then, we ran a differential expression analysis, setting the adjusted p-value cutoff to 0.05 and the log2 fold change cutoff to 0.5. Using the single-cell data, we pseudobulked the counts for each donor to have a count of each gene. We repeated this method for the comparison of early vs. late-onset preeclampsia using the pseudobulk data. 

When we compared placentas from pregnancies with preeclampsia to those without, we tested 26, 485 genes to determine which ones were more or less active. Gene activity means how much mRNA a gene produced, so more mRNA means the gene was more active. We measured this as “fold change”, which tells you how many times higher or lower a gene’s activity was in one group compared to the other. 
Using our adjusted p-value cutoff of 0.05 and log2 fold change cutoff of 0.5, we found that 836 genes passed. 512 were higher in pregnancies with preeclampsia, and 324 were lower. Among the strongest results were ENG, SERPINA3, and HTRA4. ENG had a log2 fold change of 2 and an adjusted p-value of 1.22e-17. ENG is involved in vascular signaling and provides instructions for making a protein called endoglin, which is found on the surface of cells, especially in the lining of developing arteries. SERPINA3, an encoder for a plasma serine protease inhibitor, had an even higher log2 fold change of 6 and an adjusted p-value of 2.87e-18. HTRA4, which encodes a secreted serine protease (an enzyme that cleaves peptide bonds in proteins), had a log2 fold change of 2.69 and an adjusted p-value of 1.93e-14. 
To see which genes may be known markers of broad placental types, we cross-referenced our results with a table of known placental cell-type markers. Four of the five genes were markers of maternal cell types. These included KLRD1, which encodes a protein that helps immune cells distinguish between healthy and infected cells; KIT, which encodes a kinase that regulates cell survival; CLDN5, which produces a membrane protein found between endothelial and epithelial cells; and PDGFRA, which encodes a kinase that regulates cellular growth. The remaining gene, CGA, was identified as a marker of fetal cell types and encodes glycoprotein hormones. 
To compare early-onset vs. late-onset preeclampsia, we used the single-cell pseudobulk donor data. Among the most significant were SGOL2 (log2FC = 0.78, padj = 0.0006) and UHRF1 (log2FC = 0.95, padj = 0.001), both markers of actively dividing cells. This pattern, combined with other genes that encode protein kinases regulating cell division in our results, such as BUB1B, NEK2, and AURKA, suggests that early-onset preeclampsia placentas may have more actively proliferating cells than late-onset cases. More overexpressed genes of cell proliferation may trigger preeclampsia by disrupting how the placenta anchors and connects to the mother’s blood supply. 

---

Figure 2:  PCA plots for preeclampsia versus control and early onset and clinical group.

Figure 3: Volcano plot showing the significant genes expressed for preeclampsia versus control and early onset versus late onset preeclampsia.

[Figure 4: Venn diagram showing the overlap in differential gene expression in three comparisons (early vs late, early vs. control, and late vs. control).

Unanswered Questions:
The analysis revealed some differences regarding early and late-onset preeclampsia, but it was not able to determine if preeclampsia causes early delivery. We analyzed fetal growth as a binary variable, but it would be interesting to look at the mass of the baby at delivery to determine if cases that show greater severity in the marker genes are related to restriction in growth, specifically in the early-onset cases. The late-onset cases would also be valuable in exploring how much of a difference early onset vs. late onset has on fetal growth and development. Additionally, exploring blood pressure would be extremely valuable in diagnosis if this may help characterize severity or late vs. early onset.

Conclusions, Limitations and Next Steps:
For analysis of early versus late, counts were summed across all cell types within each donor, leading to a limitation in a differential expression analysis, as differences could reflect shifts in cell-type composition rather than within-cell-type changes.
Future directions would include further analysis regarding early and late-onset preeclampsia. The initial exploratory analysis offered some insights about possible pathways that differ, but analyzing bulk RNA would not be limited as our study had.
Data and Code
Repository: https://github.com/annikapohlo/OpenBioHackathon.git 
Data sources: [list each dataset with its link]
Acknowledgements
