# journal-ranking-pca
A data science capstone project that refines academic journal ranking systems by integrating traditional metrics (SJR, CiteScore, H-index) with expert insights and Principal Component Analysis (PCA).

# Principled Ranking for Academic Journals

This repository contains the code, data, and documentation for a data science capstone project at City University of Hong Kong (SDSC4116, Academic Year 2023/24). The project critically evaluates existing academic journal ranking systems and proposes an improved framework by integrating expert-assigned weights and Principal Component Analysis (PCA).

## Project Overview

Academic journal rankings play a vital role in research dissemination, career advancement, and funding allocation. Traditional metrics like Impact Factor, CiteScore, and H-index have known limitations — including susceptibility to self-citation, legacy bias, and over-emphasis on quantity over quality.

This project addresses these shortcomings by:
- Scraping and consolidating journal metadata from Scopus, Scimago, and Web of Science.
- Normalizing and cleaning a dataset of 18,000+ journals.
- Applying expert-driven weights to selected metrics.
- Using Principal Component Analysis (PCA) for dimensionality reduction and objective ranking.
- Comparing results across original, expert-weighted, and PCA-based ranks.

## Key Metrics Used

- SJR Index – Weighted citation impact from Scimago
- H-index – Productivity and impact measure
- CiteScore – 3-year citation per document score
- Cites/Doc (2y) – Citation density
- Total Cites (3y) – Recent influence indicator
- Refs/Doc – Controls over-referencing

## Methodology

1. Data Collection: Journal metadata from multiple sources (Kaggle, APIs, manual scraping)
2. Cleaning: Removing incomplete rows, deduplication, merging on journal titles
3. Weight Assignment: Expert interviews used to assign domain-informed weights
4. PCA Implementation: Conducted on selected metrics to extract principal components explaining 95% of variance
5. Ranking Comparison: Rankings from three systems are compared using Kendall’s Tau correlation

## Results Summary

- Positive correlation between PCA-based and expert-weighted rankings (Kendall’s Tau: 0.88)
- Journal "Cell" remained top-ranked in all systems
- PCA penalized "Science", possibly due to outlier sensitivity or data sparsity

## Files Included

- `journal_ranking_analysis.ipynb` – Jupyter Notebook with full codebase
- `principled_journal_ranking_report` – Full academic report with methodology, discussion, and citations
- `journal_ranking_data.csv` – Cleaned journal dataset with 59 columns and approximately 18,000 entries

## Technologies

- Python (Pandas, Scikit-learn, NumPy, Matplotlib)
- Excel (VLOOKUP, preprocessing)
- Jupyter Notebook
- Data sources: Scopus, Web of Science, Scimago, Kaggle

## Citation

If you use this repository in your own research, please cite it as:

Mak, Long Ho. (2024). *Principled Ranking for Academic Journals*. City University of Hong Kong, Data Science Capstone Project.

## Supervisor

Prof. Qing Ke – City University of Hong Kong

## Contact

For inquiries or feedback, please open an issue or contact the project author via GitHub.
