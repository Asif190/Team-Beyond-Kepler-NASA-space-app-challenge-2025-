# Team-Beyond-Kepler-NASA-space-app-challenge-2025-

# AstroVeritas

**Finding truth in the cosmos.**

---

## 🌌 Overview

AstroVeritas is a machine learning–powered pipeline for **exoplanet candidate vetting**. It ingests raw light curves (TESS) and applies **synthetic transit injection, feature extraction, and LightGBM classification** to identify likely planetary signals.

The name *AstroVeritas* comes from *Astronomy* and *Veritas* (Latin for "truth"), symbolizing the search for genuine planetary candidates hidden in stellar noise.

---

###Our deployed app integrated with ML model
https://astroveritas.vercel.app/

for using the app , the demonstration has been provided in our youtube link, check out our youtube link for good understanding.

###you can avail the testing code directly from the below github source where we have uploaded
https://github.com/ahmmedalzubaeranam/astroveritas-app




## ✨ Features

* **Light Curve Ingestion**: Supports both local FITS/TPF files and Lightkurve-based searches.
* **Synthetic Injection**: Generates realistic planet-like signals for training when labeled datasets are limited.
* **Feature Extraction**: Computes BLS-derived and statistical features for robust vetting.
* **Fast Model Training**: Uses LightGBM/XGBoost with balanced datasets for high AUC in minutes.
* **Model Persistence**: Saves trained models for reuse and deployment.
* **Demo Pipeline**: Test new light curves with pre-trained weights and visualize predictions.
* **Explainability**: SHAP integration for feature importance and calibration checks.

---

## 📂 Pipeline Structure

1. **Data Preparation**

   * Load TOI/KOI or custom target tables.
   * Inject synthetic transits if labels are missing.

2. **Light Curve Processing**

   * Detrending, folding, and BLS search for candidates.
   * Generate global & local views for models.

3. **Feature Extraction**

   * Period, duration, depth, power, mean/variance, flux range.

4. **Model Training**

   * Train LightGBM with balanced splits.
   * Evaluate with ROC-AUC, precision-recall, Brier score.

5. **Demo Inference**

   * Run predictions on demo targets.
   * Output probability bars and ROC curves.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/username/AstroVeritas.git
cd AstroVeritas
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Run Training

Open the notebook and execute cells up to **Cell 13** to train the LightGBM model.

### 4. Save Model

The trained weights will be stored as:

```
vetting_lightgbm.pkl
```

### 5. Demo Inference

Run the **Demo Cell** to test the saved model on sample TESS targets.
(checkout github link provided for more elaborate inference code)
---

simply,
## Getting Started

1. Install dependencies via `pip install -r requirements.txt`  
2. Run notebook cells 1–13 to train model.  
3. Demo inference on sample light curves.  
4. Use saved model `vetting_lightgbm.pkl` for predictions.




## 📊 Results

* Dataset: ~100 real + ~400 synthetic signals
* Classifier: LightGBM
* Test ROC-AUC: **0.85–0.9** (typical range)
* Training Time: ~minutes instead of hours (compared to CNN)

---

## 🛠️ Tech Stack

* **Python 3.9+**
* [Lightkurve](https://docs.lightkurve.org/) (light curve processing)
* [LightGBM](https://lightgbm.readthedocs.io/) (fast gradient boosting)
* [scikit-learn](https://scikit-learn.org/) (metrics, calibration, pipeline tools)
* [Matplotlib](https://matplotlib.org/) (visualization)
* [SHAP](https://shap.readthedocs.io/) (explainability)

---

## 📜 License

MIT License – free to use and modify.

---

## 👩‍🚀 Authors & Contribution

Developed by **Mohammad Asif Hasan Sudipto Sarkar ** and other members of team beyond kepler.
Part of an effort to build **fast, explainable exoplanet vetting pipelines** for the research community.

---

## 🌠 Acknowledgements

* [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
* [Kepler & TESS Missions](https://exoplanets.nasa.gov/)
* Open-source ML community
*large language models (LLMs)

---
