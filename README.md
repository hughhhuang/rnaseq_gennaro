# DB Search for THZ1 CDK9 inhibitor data

### 2020-01-13

- Find THZ1 Cell paper (2016), download data and analyze
- Find a more recent paper where they created a THZ1 analog that degrades CDK9. Find the dataset with the alternate inhibitor
- Find the Protac THZ1 paper. Get RNA-Seq data and analyze.


### 2019-12-18

From Dr. Issa :  look in public databases to see if there are gene expression datasets related to CDK4/6 and 7? In particular data before and after treatment with CDK4/6 and CDK7 inhibitors? Prioritize CDK7 (one inhibitor is called THZ1).

**The plan is to download a few of these datasets, map them to the transcriptome with Salmon, collapse to the gene level, and get counts. One all studies have counts for each sample, combine the data and try to adjust for batch efects. Then plot RPKM values for the CDK and Cyclin genes**

# Data

## Cayrol 2017 (data/cayrol2017)

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5290269/

Experiment type : Expression profiling by high throughput sequencing

Summary : Peripheral T-cell lymphomas (PTCL) are aggressive diseases with poor response to chemotherapy and dismal survival. Identification of effective strategies to target PTCL biology represents an urgent need. Here we report that PTCL are sensitive to transcription-targeting drugs, and, in particular, to THZ1, a covalent inhibitor of cyclin-dependent kinase 7 (CDK7). The STAT-signaling pathway is highly vulnerable to THZ1 even in PTCL cells that carry the activating STAT3 mutation Y640F. In mutant cells, CDK7 inhibition decreases STAT3 chromatin binding and expression of highly transcribed target genes like MYC, PIM1, MCL1, CD30, IL2RA, CDC25A and IL4R. In surviving cells, THZ1 decreases the expression of STAT-regulated anti-apoptotic BH3 family members MCL1 and BCL-XL sensitizing PTCL cells to BH3 mimetic drugs. Accordingly, the combination of THZ1 and the BH3 mimetic obatoclax improves lymphoma growth control in a primary PTCL ex vivo culture and in two STAT3-mutant PTCL xenografts, delineating a potential targeted agent-based therapeutic option for these patients.
  	
Overall design : OCI-Ly13.2 cells were treated with 500 nM THZ-1 or vehicle for 3 h or 6 h in triplicate. Total RNA was harvested from cells and used for expression profiling via RNA-seq.

## Olson 2018 (data/olson2018)

Experiment type : Expression profiling by high throughput sequencing

Summary : Development of a selective CDK9 degrader from a multi-targeted CDK inhibitor. Cyclin dependent kinase 9 (CDK9), a key regulator of transcriptional elongation, has long been considered a promising target for cancer therapy, particularly for cancers driven by transcriptional dysregulation. However, despite promising early clinical data in blood cancers using pan-CDK inhibitors that potently inhibit CDK9 such as Dinaciclib and Flavopiridol, no selective CDK9 inhibitors have been clinically approved. Here we show that a multi-targeted CDK inhibitor can be used to develop a selective CDK9 degrader exemplified by THAL-SNS-032, a hetero-bifunctional molecule composed of SNS-032, a CDK2,7,9 inhibitor conjugated to thalidomide, a small molecule binder of Cereblon. We demonstrate that THAL-SNS-032 can recruit the E3 ubiquitin ligase Cereblon to CDK9 and induce its proteasome-mediated degradation. Treatment of cells with low nanomolar concentrations of THAL-SNS-032 resulted in rapid and efficient CDK9 degradation but did not affect levels of other SNS-032 targets, including CDK2 and CDK7. Consistent with this selective degradation phenotype, transcriptional profiling of THAL-SNS-032 indicated that its transcriptional effects were more similar to that of a selective CDK9 inhibitor, NVP2, than that of the nonselective SNS-032 parent compound. Moreover, THAL-SNS-032, in contrast to traditional CDK9 inhibitors, retained potent pro-apoptotic activity even after compound removal from cells. This suggests that degradation of CDK9 leads to prolonged cytotoxic effects as compared to CDK9 inhibition. Thus, our findings suggest that thalidomide conjugation may be a promising strategy for converting multi-targeting inhibitors into selective degraders, and that the pharmacological effects of kinase degradation can be distinct from kinase inhibition. Overall design: RNA-seq of MOLT4 cells treated with DMSO, SNS-032, THAL-SNS-032, or NVP-2 for 6 hours Please note that the data column headers (and their order) in the in the 'molt4_cdk9_all_fpkm_exprs_norm.txt' file are different from the Sample title. The corresponding data column for each sample is indicated in the sample description field.

## Olson 2019 (data/olson2019)

Experiment type : Expression profiling by high throughput sequencing

Summary : Development of a selective CDK7 covalent inhibitor reveals predominant cell cycle phenotype. The relationship between promoter proximal transcription factor-associated gene expression and super-enhancer-driven transcriptional programs are not well-defined. Some level of their distinct genomic occupancy may suggest a mechanism with specific target gene control. We explored the transcriptional and functional interrelationship between E2F transcription factors and BET transcriptional co-activators in multiple myeloma. Global chromatin analysis reveals distinct regulatory axes for E2F and BETs, with E2F predominantly localized to active gene promoters of growth/proliferation genes and BETs disproportionately at enhancer- regulated tissue specific genes. Depletion of E2F selectively down-regulates its regulatory axis and is generally synergistic with BET inhibition. In vivo, combined inhibition of BETs and E2F strongly reduces tumor growth, implicating E2F as a myeloma dependency that is potently leveraged with BET inhibition. Overall design: Cyclin-dependent kinase 7 (CDK7) regulates both cell cycle and transcription, but its precise role remains elusive. We previously described THZ1, a CDK7 inhibitor, which dramatically inhibits super-enhancer associated gene expression. However, potent CDK12/13 off-target activity obscured CDK7s contribution to this phenotype. Here, we describe the discovery of a highly selective, covalent CDK7 inhibitor. YKL-5-124 causes arrest at the G1/S transition and inhibition of E2F-driven gene expression; these effects are rescued by a CDK7 mutant unable to covalently engage YKL-5-124, demonstrating on-target specificity. Unlike THZ1, treatment with YKL-5-124 resulted in no change to Pol II CTD phosphorylation; however, inhibition could be reconstituted by combining YKL-5-124 and THZ531, a selective CDK12/13 inhibitor, revealing potential redundancies in CDK control of gene transcription. These findings highlight the importance of CDK7/12/13 polypharmacology for anti-cancer activity of THZ1 and posit that selective inhibition of CDK7 may be useful for treatment of cancers marked by E2F misregulation.
