# Data Seeker

Find public sequencing datasets (ChIP-seq, CUT&RUN, RNA-seq, single-cell, ATAC-seq, Hi-C) for a gene or topic, see which ones to trust, and get a list of the exact files to download.

**Open the app:** https://mockingchicken.github.io/Data-seeker/

- Searches NCBI GEO, ENCODE and EBI ArrayExpress at once, with gene aliases from NCBI Gene (MyoD also finds MYOD1, Myod1, MYF3).
- Shows species, cell line or tissue, assay and study design for every dataset, and scores each one for reliability (Tier A, B or C) with the reasons listed.
- Star datasets to keep them, then build a download list: pick target and control samples and file types, and save one file list with every URL (GEO files, ENCODE files, SRA runs and ENA FASTQ links).
- Your workspaces are saved in your own browser and never uploaded. Only your search terms and the accessions you pick are sent to NCBI, ENCODE and EBI.

Always check antibodies, controls and replicates on the repository page before relying on a dataset.

Huang J., Roberts T.C. Data Seeker [software]. RNA Medicine Group, Department of Paediatrics, University of Oxford; 2026.

## Files

- `index.html` – the app (a single self-contained page).
