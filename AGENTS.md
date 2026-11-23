# paper_rnaseq_onboarding

Companion data and code to a comparative transcriptomics paper on the oleaginous and halotolerant yeasts Yarrowia lipolytica, Debaryomyces hansenii and Debaryomyces subglobosus (nitrogen starvation, iron starvation, salt stress). It holds the count tables, annotations, R Markdown analyses (DESeq2, WGCNA) and Jupyter notebooks (k-means clustering of DEGs) behind the paper's figures.

## For whom
- The repo as a whole: Eric, for data analysis now; it becomes the paper's supplement later (GitHub: emyounglab/paper_rnaseq_onboarding). Not a tool.
- Feeds nothing and reads no other repo.

## Where
- Runs on: Eric's Mac, in RStudio and Jupyter (the Rmd files set a `~/Library/Mobile Documents/.../WPI/Young/data` working directory). Not run on the Windows PCs. Remote: GitHub, public.
- Data: the count tables, annotation CSVs and result workbooks sit at the repo root; the Rmd and notebooks expect them under `dh/`, `ds`/`dsub/` and `yl/` folders that are not in the repo. Ground truth: the paper's published results.
