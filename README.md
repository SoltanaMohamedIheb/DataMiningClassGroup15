# Healthcare Provider Fraud Detection (Cost-Sensitive Replication)

Course project: **Cost-Sensitive Predictive Modeling for Healthcare Provider Fraud Detection** — adapting Shi et al. (2023), *IEEE TKDE*, to the [Kaggle Healthcare Provider Fraud Detection](https://www.kaggle.com/datasets/rohitrox/healthcare-provider-fraud-detection-analysis) dataset.

**Team:** Mortadha Ghnimi, Firas Frouja, Mohamed Iheb Soltana, Ghofrane Bousbih

## Repository layout

| Path | Description |
|------|-------------|
| `fraud_detection.ipynb` | Full pipeline: data fusion, feature engineering, models (LR, RF, GBM, MLP), cost-sensitive evaluation, figures |
| `Fraud_Detection_Report.docx` | Conference-style write-up (regenerate with `generate_paper_10pages.py` if needed) |
| `Data/` | Original CSVs (train/test labels, beneficiaries, inpatient, outpatient) |
| `figures/` | PNG exports from the notebook (optional; notebook can regenerate) |
| `generate_paper_10pages.py` | Script that builds `Fraud_Detection_Report.docx` |

## Requirements

- Python 3.9+ (tested with 3.11)
- Packages: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`, `scipy`

Install:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn scipy
```

Optional (to execute the notebook from the CLI):

```bash
pip install jupyter nbconvert ipykernel
```

## Reproducibility

1. Clone or download this folder and keep the `Data/` CSV structure unchanged.
2. Open `fraud_detection.ipynb` in Jupyter / VS Code and **Run All** (runtime ~7–10 minutes on a typical laptop; 200 model fits).
3. Figures save under `figures/` if the notebook export cells are run; the notebook also prints all tables and metrics.

To regenerate the Word report:

```bash
python generate_paper_10pages.py
```

Update the **repository URL** on the report title page and in this README after you publish to GitHub.

## References

1. H. Shi *et al.*, “Cost-Sensitive Learning for Medical Insurance Fraud Detection With Temporal Information,” *IEEE Trans. Knowl. Data Eng.*, vol. 35, no. 10, pp. 10451–10463, 2023. [IEEE Xplore](https://doi.org/10.1109/TKDE.2023.3240431)
2. Kaggle dataset and community notebooks: [Healthcare Provider Fraud Detection Analysis](https://www.kaggle.com/code/farelarden/healthcare-provider-fraud-detection-analysis)

## License / use

The Kaggle data are subject to their terms of use. This code is for educational use; fraud scores are not legal determinations of fraud.
