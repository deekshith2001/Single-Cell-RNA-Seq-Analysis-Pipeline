# Single-Cell RNA-Seq Analysis Pipeline

This repository hosts a comprehensive and modular pipeline for analyzing single-cell RNA sequencing (scRNA-seq) data. The workflow integrates advanced preprocessing, dimensionality reduction, clustering, and visualization techniques, making it a robust tool for understanding cellular heterogeneity. Designed with scalability in mind, the pipeline is suitable for research, education, and large-scale bioinformatics applications.

---

## Project Overview

### Objectives
The pipeline enables researchers to:

1. Efficiently preprocess and normalize scRNA-seq datasets.
2. Identify distinct cell subpopulations using cutting-edge clustering techniques.
3. Visualize high-dimensional scRNA-seq data through dimensionality reduction methods.

### Key Features
- **Dimensionality Reduction:** Implements PCA, t-SNE, and UMAP, optimized for high-dimensional data representation.
- **Clustering Algorithms:** Supports Gaussian Mixture Models (GMM) and DBSCAN with automated model selection for GMM using the Bayesian Information Criterion (BIC).
- **Visualization Tools:** High-quality 2D/3D scatter plots, clustering maps, and posterior probability distributions.
- **Scalability:** Modular design with object-oriented programming principles, facilitating easy integration into larger workflows.

---

## Workflow

1. **Data Input:** Load scRNA-seq datasets in `.csv` format, structured with cells as rows and genes as columns.
2. **Preprocessing:** Normalize the data and filter out low-quality features while identifying highly variable genes.
3. **Dimensionality Reduction:** Reduce data complexity with PCA, t-SNE, and UMAP for meaningful data visualization.
4. **Clustering:** Use GMM or DBSCAN to group cells into biologically meaningful clusters. For GMM, optimal cluster numbers are selected automatically based on BIC.
5. **Visualization:** Generate visual representations to interpret clustering and underlying data structure.
6. **Output:** Save clustering results as `.csv` files for downstream analysis.

---

## Results

The pipeline has been validated with a sample dataset containing 137 cells and 54,675 genes. It successfully reduced dimensionality, identified biologically relevant clusters, and produced insightful visualizations. Example results and workflows are available in the Jupyter Notebook `scRNAseq_data_analysis.ipynb`.

---

## Installation

### Prerequisites
- Python 3.8 or later

### Dependency Installation
Install the required Python packages using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn umap-learn
```

---

## Repository Structure

- **`codebase.py`**: Core implementation of the pipeline encapsulated in the `DataPipeline` class.
- **`scRNAseq_data_analysis.ipynb`**: Jupyter Notebook demonstrating the use of the pipeline step-by-step.
- **`data/`**: Directory for input (`RNA-seq.csv`) and output (`labels.csv`) files.
- **`documents/`**: Supplementary materials, including documentation and feedback.

---

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/username/scRNAseq-Analysis-Pipeline.git
   cd scRNAseq-Analysis-Pipeline
   ```

2. Place your scRNA-seq dataset in the `data/` directory.

3. Run the pipeline interactively via the Jupyter Notebook:
   ```bash
   jupyter notebook scRNAseq_data_analysis.ipynb
   ```

4. Alternatively, execute the pipeline directly using the `codebase.py` script.

---

## Future Work

Planned enhancements include:
- Integration with spatial transcriptomics tools like SpatialDE.
- Automated batch effect correction using Harmony or Mutual Nearest Neighbors (MNN).
- Cloud-based scalability on AWS or Google Cloud for large datasets.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

For questions, contributions, or issues, please open an issue or contact the repository maintainer.
