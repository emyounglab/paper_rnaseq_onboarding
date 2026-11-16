# rnaseq-onboarding
Oleaginous yeast biology elucidated with comparative transcriptomic

Extremophilic yeasts have favorable metabolic and tolerance traits for biomanufacturing- like lipid biosynthesis, flavinogenesis, and halotolerance- yet the connection between these favorable phenotypes and strain genotype is not well understood. To this end, this study compares the phenotypes and gene expression patterns of biotechnologically relevant yeasts Yarrowia lipolytica, Debaryomyces hansenii, and Debaryomyces subglobosus grown under nitrogen starvation, iron starvation, and salt stress. To analyze the large dataset across species and conditions, two approaches were used: a ’network first’ approach where a generalized metabolic network serves as a scaffold for mapping genes and a ’cluster first’ approach where unsupervised machine learning co-expression analysis clusters genes. Both approaches provide insight into strain behavior. The network first approach corroborates that Yarrowia up-regulates lipid biosynthesis during nitrogen starvation and provides new evidence that riboflavin overproduction in Debaryomyces yeasts is overflow metabolism that is routed to flavin cofactor production under salt stress. The cluster-first approach does not rely on annotation; therefore, the coexpression analysis can identify known and novel genes involved in stress responses, mainly transcription factors and transporters. Therefore, this work links the genotype to the phenotype of biotechnologically relevant yeasts and demonstrates the utility of complementary computational approaches to gain insight from transcriptomics data across species and conditions. 

Companion data and code to transcriptomics paper.

## Run
none. The analyses are R Markdown files and Jupyter notebooks opened interactively; there is no command-line entry point. Order, per species (`dh`, `ds`/`dsub`, `yl`):
1. `dh.Rmd`, `dsub.Rmd`, `yl.Rmd`: DESeq2 normalisation and differential expression from the `counts_*.txt` tables.
2. `WGCNA_dh.Rmd`, `WGCNA_ds.Rmd`, `WGCNA_yl.Rmd`: co-expression modules from the normalised counts and DEGs.
3. `20220923_DEGclustering_n4_*.ipynb`: k-means clustering (4 clusters) of the significant DEGs.

## Known errors
- The Rmd files and notebooks use paths from the author's Mac (`~/Library/Mobile Documents/...`) and per-species folders (`dh/data/`, `dh/output/`, `../output/`) that are not in this repo. Point them at the files in the repo root (`counts_*.txt`, `norm_counts_*.txt`, `*_annotation*.csv`) before running.
