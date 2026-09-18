# Reproducibility Package — JBI Hybrid SEIR-LSTM

This repository contains the reproducibility artifacts for the manuscript:

> **Constraint-Aware Hybrid Mechanistic–Machine Learning Models for
> Infectious Disease Forecasting: A Methodological Review**

submitted to the *Journal of Biomedical Informatics*.

## Authors

- **Kanza Arshad** (corresponding author) — kanza.arshad@cinvestav.mx

## Contents

| File | Description |
|---|---|
| `notebook.ipynb` | Full reproducibility notebook (Colab-compatible) |
| `table3_FINAL.csv` | Table 3 of the manuscript (model comparison) |
| `table4_FINAL.csv` | Table 4 of the manuscript (ablation analysis) |
| `fig2_train_test_split.png` | Figure 2 (chronological train–test split) |
| `fig3_FINAL.png` | Figure 3 (SMAPE and WMAPE bar charts) |
| `validation_countries_high_medium_low.csv` | Derived signal-strength summary for 9 validation countries |

## How to run

1. Open the notebook in Google Colab:

   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kanza/jbi-hybrid-seir-lstm/blob/main/notebook.ipynb)

2. Upload the raw JHU CSSE dataset `time_series_covid19_confirmed_global.csv`
   to the Colab working directory when prompted (see **Data source** below).

3. Run all cells: **Runtime → Run all**. Runtime is approximately 3 minutes
   on the Google Colab free tier with a T4 GPU.

## Environment

- Python 3.10
- TensorFlow 2.x
- statsmodels 0.14
- scikit-learn 1.x
- pandas 2.x
- numpy 1.x

## Data source

Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE)
COVID-19 dataset:

https://github.com/CSSEGISandData/COVID-19

## Notes

- All random seeds, solver tolerances, and hyperparameters are documented
  inside `notebook.ipynb`.
- The hybrid SEIR–LSTM configuration explored in Section 6.8 of the
  manuscript (negative result) is documented in **Appendix A** of the
  notebook.
- The chronological 70/30 train–test split (22 January 2020 – 31 March 2022
  for training; 1 April 2022 – 9 March 2023 for testing) is enforced in
  Section 4 of the notebook.

## Citation

If you use this code or data, please cite:

> Arshad, K., & Meneses-Viveros, A. (2026). *Constraint-Aware Hybrid
> Mechanistic–Machine Learning Models for Infectious Disease Forecasting:
> A Methodological Review.* Manuscript submitted to the Journal of
> Biomedical Informatics.

## License

MIT License (see `LICENSE` file, if present).
