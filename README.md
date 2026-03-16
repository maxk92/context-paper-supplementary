# Supplementary Material: Confounding in Match Analysis Research

This repository contains the analysis code accompanying the paper *"The Role of Contextual Factors in Match Analysis Research and their Potential for Confounding Effects"*.

## Notebooks

- **`aggregation_experiment_dataprocessing.ipynb`** — Loads publicly available event data from the [StatsBomb open data repository](https://github.com/statsbomb/open-data) (1. Bundesliga 2015/16, 306 matches) via `statsbombpy`, extracts 16 performance indicators, and aggregates them at three levels: season, match, and scoreline segment.

- **`aggregation_experiment_modeling.ipynb`** — Fits ordered probit models for each performance indicator at each aggregation level and produces the figures and tables reported in the paper.

- **`create_thoughtexperiment.qmd`** — Generates the figure and descriptive table for the thought experiment presented in the paper, illustrating how match-level aggregation can reverse a PI–success association when the scoreline varies within a match.

## Data

Processed datasets at each aggregation level are available in the `data/` subfolder for direct use without re-running the data processing step:

| File | Description |
|---|---|
| `df_seasonlevel.csv` | One row per team, season-level aggregates |
| `df_matchlevel.csv` | One row per team per match |
| `df_scorelinelevel.csv` | One row per scoreline segment per match |
| `df_coefs_probit.csv` | Model coefficients and confidence intervals (all indicators × all levels) |
