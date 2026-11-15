Preeclampsia is one of the leading causes of maternal and infant illness and mortality, affecting an estimated 2-8% of all pregnancies worldwide. It is characterized by high blood pressure, high levels of protein in urine that indicate kidney damage, or other signs of organ damage. Proteinuria is due to injury to the kidney’s filtering units, as a result of systemic endothelial dysfunction. Symptoms include severe headache, visual disturbances, upper abdominal pain, and sudden swelling. 

In early-onset preeclampsia, trophoblast cells fail to properly invade and remodel the maternal spiral arteries, leading to placental hypoperfusion and hypoxia. This causes an imbalance in angiogenesis, the process by which new blood vessels develop from pre-existing ones, characterized by elevated anti-angiogenic soluble FLT1 (sFLT1) and soluble endoglin (sEng) and reduced placental growth factor (PlGF) (Tomimatsu et al., 2017; Venkatesha et al., 2006). Late-onset preeclampsia shows a milder version of this imbalance and is thought to arise more from maternal cardiovascular and metabolic susceptibility. In both, many people have no early warning signs, which is why routine prenatal blood pressure and urine checks are critical, as diagnosis depends on detecting new hypertension.

Often classified into two categories, we additionally explored the expression differences in early-onset preeclampsia and late-onset preeclampsia.

We used datasets from GSE203507, a public bulk RNA sequencing study of placentas collected at delivery. Villous tissue was taken from 30 patients, 15 of those with preeclampsia. Fetal growth restriction was also characterized in 5 of 15 non preeclampsia placentas and 7 of the preeclampsia placentas. The data contains multiple samples from multiple tissues. The Zeisel/Admati Gene Browser was used to interpret the cell types observed in our analysis. Additionally, we used single cell RNA seq data from the Admati/Skarbianskis study, which measured 86,752 individual placental cells from 26 donors.

What did your analysis show? Be specific about the genes and cell types.


Proposed Mechanism
Trophoblast: hypoxic stress and anti-angiogenic factor release.
In early-onset preeclampsia, erroneous remodelling of the maternal spiral arteries causes hypoxia, shown in the increased ERO1A, TMEM45A. ERO1A encodes an endoplasmic reticulum oxidoreductase that promotes disulfide bond formation and supports protein folding in the secretory pathway; TMEM45A encodes a transmembrane protein localized primarily to the trans-Golgi apparatus and endomembrane system.
There’s also an increased production of ENG and HTRA4. Endoglin is cleaved from the cell surface and released into the maternal circulation as soluble endoglin (sEng). 
Circulating sEng binds TGF-β1 and blocks it from signalling through endothelial endoglin. Together with sFLT1, which binds VEGF and PlGF, this deprives the maternal endothelium of protective signals and causes systemic endothelial dysfunction, leading to hypertension and glomerular injury (proteinuria). Within the placenta, the modest increases in CLDN5 and PDGFRB may reflect remodelling of fetal villous capillaries and the cells around them under chronic hypoxia.

Decidual NK cells are the most abundant immune cells at the maternal–fetal interface in early pregnancy. They secrete factors such as VEGF, PlGF and interleukin-8 that help trophoblast invade and remodel the spiral arteries. Lower KLRD1, which encodes the NK receptor CD94, may indicate fewer or less active dNK cells. That could be an upstream cause of the failed artery remodelling that starts early-onset PE. Because villous samples contain few decidual cells, this part of the mechanism is a hypothesis to test rather than a finding.



Why the Result Is Biologically Plausible?
Our top hit, ENG, relates to PE in that placenta-derived soluble endoglin is elevated in preeclampsia and causes hypertension and proteinuria in animal models (Venkatesha et al., 2006), alongside sFLT1 (Maynard et al., 2003). The strength of this signal in early-onset cases fits early-onset PE being mainly placental in origin (Burton et al., 2019). HTRA4 and SERPINA3 have been reported as upregulated in PE placenta, and ERO1A and TMEM45A are hypoxia-induced genes, consistent with a poorly perfused placenta.

Alternative explanations / confounders
Fetal growth restriction: FGR overlaps with PE and shares placental pathology.
Cell composition: Although the gene browser shows which cell types express each gene, bulk data cannot distinguish between more of those cells and higher expression per cell.


Tomimatsu, Takuji, et al. “Pathophysiology of Preeclampsia: An Angiogenic Imbalance and Long-Lasting Systemic Vascular Dysfunction.” Nature News, Nature Publishing Group, 10 Nov. 2016, www.nature.com/articles/hr2016152. 

Venkatesha, Shivalingappa, et al. “Soluble Endoglin Contributes to the Pathogenesis of Preeclampsia.” Nature News, Nature Publishing Group, 4 June 2006, www.nature.com/articles/nm1429#Sec1. 
