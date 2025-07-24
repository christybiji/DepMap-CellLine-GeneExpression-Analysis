# Gene Expression Analysis & Visualization of Cancer Cell Lines (DepMap Data)

This Google Colab notebook provides a comprehensive workflow for analyzing gene expression data from the DepMap Public portal, with a particular focus on cancer cell lines.

## Project Overview:

This notebook demonstrates key computational biology steps for:
1.  **Data Loading & Preprocessing:** Efficiently loading large `.csv` files from DepMap (e.g., Omics Expression, Model Info).
2.  **Data Quality Control (QC):**
    * Initial DataFrame inspection (`.head()`, `.info()`, `.describe()`).
    * Checking for missing values (NAs) and duplicate entries.
    * Standardizing cell line (ModelID) and gene naming conventions across datasets.
    * Visualizing overlap between datasets using Venn diagrams for ModelIDs and genes.
3.  **Target Cell Line Identification:** Filtering and verifying the existence of specific cell lines of interest (e.g., AML cell lines) and designated control cell lines within the dataset.
4.  **Differential Gene Expression Analysis:**
    * Calculating Log2 Fold Change (Log2FC) for genes in individual "test" cell lines compared to a pooled "control" baseline.
    * **Note on P-values:** For demonstration purposes, p-values are simulated in this notebook. For rigorous scientific analysis, biological replicates are essential for calculating valid statistical p-values.
5.  **Data Visualization:**
    * Bar plots to highlight the top upregulated and downregulated genes.
    * Volcano plots to simultaneously visualize Log2FC and (simulated) significance, with annotations for key genes.

## Data Used:
* DepMap Public data: `OmicsExpressionProteinCodingGenesTPMLogp1.csv`, `Model.csv`, and others.

## Libraries Used:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `matplotlib-venn`

## How to Use:
1.  Ensure you have downloaded the necessary DepMap `.csv` files to your Google Drive and updated the file paths in the notebook's initial cells.
2.  Run all cells sequentially.
3.  Review the output and generated plots for insights into gene expression patterns.

---
