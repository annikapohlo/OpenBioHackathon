Analysis Plan

Research Question:
Do early-onset and late-onset preeclampsia tell different biological stories? 

Datasets:
1. track01_metadata_vt.csv (sample metadata) - Describes the pregnancy; we used this to define groups, comparisons, and covariates.
2. track01_counts_vt.csv (count data) - Provides the RNA reads, so we can see gene activity.
3. Zeisel/Admati Gene Browser (cell-type interpretation) - Allows us to look up which placental cell types use that gene and compare it to other genes. 
4. track01_pseudobulk_counts.csv (count data) - Used to compare early vs. late onset of preeclampsia. 
5. track01_pseudobulk_donors.csv (donor data) - Gives us information on early vs. late preeclampsia and the donors. 

Methods:
Loaded the count and metadata tables and checked if they fit together.
We compared PE vs. no_PE using the pe_status column. This allows us to look at preeclampsia’s effect before splitting into early vs. late onset. Then, we compared early vs. late onset of preeclampsia to determine the differences between genes in early vs. late onset. 
Ran a differential expression analysis using PyDESeq2. We used an adjusted p-value cutoff of 0.05 and a log2 fold change cutoff of 0.5.
We looked up ENG, SERPINA3, HTRA4, and others in the Zeisel/Admati browser and recorded which cell types express them. 
We generated a volcano plot highlighting passing genes and cross-referenced results with the marker table. 

Confounders and Controls:
1. Maternal age - Included maternal age as a covariate
2. Weeks of pregnancy at delivery - Included ga_delivery_weeks as a covariate

Expected Figures:
1. Table
2. Volcano plot
3. Scatterplot
4. Venn Diagram
