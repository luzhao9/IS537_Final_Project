# IS537 Final Project: Analyzing the Relationship Between BWF Player Rankings and National Win Rates

This repository contains the final project submission for **IS537 – Data Cleaning and Data Quality (Spring 2025)** by **Xinglu Zhao**.

## Project Overview

This project investigates whether the international ranking of badminton players is associated with their country’s overall performance in BWF Super Series tournaments. In doing so, it demonstrates an end-to-end data quality assessment and cleaning workflow using real-world datasets.

## Research Question

**To what extent does a badminton player's world ranking correlate with their national win rate?**


##  Repository Structure

IS537_Final_Project/
├── data/                 # Raw datasets (not included, see README)
├── processed/            # Cleaned and merged datasets
├── results/              # Final outputs: cleaned data, visualizations
├── IS537_Final_Notebook.ipynb   # Full analysis notebook
├── requirements.txt      # Python dependencies
├── README.md             # This file

##  Datasets

Two publicly available datasets from Kaggle were used (originally sourced from the BWF website):

- [Flashscore Player Rankings Dataset](https://www.kaggle.com/datasets/jatinthakur706/top-100-badminton-players): Player-level statistics, including ranking, nationality, and BWF points.
- [BWF Super Series Match Results (2015–2017)](https://www.kaggle.com/datasets/canggih/badminton-game-data-bwf-super-series-20152017): Match-level outcomes used to compute country-level win rates.

Due to Kaggle’s terms, these datasets are not redistributed here. See the instructions below for access.


##  Key Cleaning and Integration Tasks

- **Profiling**: Initial assessment of missingness, outliers, and inconsistencies.
- **Standardization**: Normalized country names to lowercase/trimmed whitespace.
- **Merging**: Inner join on nationality with unmatched records logged.
- **Deduplication**: Removed 7 duplicate records in the match dataset.
- **Validation**: Constraint check on match types (MS, WS, MD, WD, XD).
- **Outlier Handling**: Visualized but retained top-performance outliers.
- **Reproducibility**: Step-by-step markdown documentation and version control.

##  Analysis Highlights

- Pearson correlation between player ranking and win rate: **r = -0.33**
- Regression R² score: **0.11** – indicating ranking alone explains 11% of variance.
- Win rate distributions showed performance skewed toward countries like **China**, **Spain**, and **Denmark**.

##  Reproducibility and Setup

The workflow is fully documented and executable via:

```bash
pip install -r requirements.txt


## Contact

Project by **Xinglu Zhao** for **IS537 (Spring 2025)**  
Email: `xingluz2@illinois.edu`

