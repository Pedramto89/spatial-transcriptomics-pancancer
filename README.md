# spatial-transcriptomics-pancancer
## Live Updates: Spatial Transcriptomics Studies in Pancreatic Cancer

This repository automates the generation of a live trend plot showing the number of publications on **spatial transcriptomics** studies in **pancreatic cancer** (searched in the title/abstract) from PubMed. The plot is updated weekly using GitHub Actions.

## Overview

The pipeline consists of:
- A Jupyter Notebook (`single_cell_studies_over_time.ipynb`) that:
  - Uses the NCBI Entrez API (via Biopython) to query PubMed with the search:
    ```
    "spatial transcriptomics"[Title/Abstract] AND "pancreatic cancer"[Title/Abstract]
    ```
  - Generates a trend plot displaying the number of publications per year.
- A GitHub Actions workflow that:
  - Executes the notebook weekly.
  - Commits and pushes the updated plot to the repository.

## Data Source

I use PubMed as the data source. If you use this data elsewhere, please remember to cite PubMed appropriately.

## Requirements

- Python 3.8+
- [Biopython](https://biopython.org/)
- [matplotlib](https://matplotlib.org/)
- [Jupyter](https://jupyter.org/)

All dependencies are listed in the [`requirements.txt`](requirements.txt) file.

## Setup and Usage

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/spatial-transcriptomics-pancancer.git
   cd spatial-transcriptomics-pancancer

