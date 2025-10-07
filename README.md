# FWI Prediction for Bejaia and Sidi-Bel

## Project overview

This repository contains data and notebooks for predicting the Fire Weather Index (FWI) for two Algerian regions — **Bejaia** and **Sidi-Bel**. The goal is to explore the dataset, clean and preprocess the data, and train regression models (including Ridge and Lasso) to predict FWI and evaluate their performance.

## Contents

* `Algerian_forest_fires_dataset_UPDATE.csv` — Original or updated dataset (raw).
* `Algerian_forest_fires_cleaned_dataset.csv` — Cleaned / preprocessed dataset ready for modeling.
* `Model Training.ipynb` — Main notebook demonstrating data exploration, preprocessing, feature engineering, model training, evaluation, and saving of models.
* `Ridge, Lasso Regression.ipynb` — Focused notebook showing experiments with Ridge and Lasso regression (hyperparameter tuning, cross-validation, metrics).

## Dataset (summary)

The dataset contains weather and fire-related features collected for Algerian regions (Bejaia & Sidi-Bel). Typical columns include — date/time features, temperature, humidity, wind speed, precipitation-related variables, and the computed Fire Weather Index (FWI) as the target variable. See the cleaned CSV for exact column names and types.

## Key steps performed

1. Exploratory Data Analysis (EDA)

   * Visualizations and summary statistics to understand distributions, missingness, and correlations.
2. Data cleaning & preprocessing

   * Handling missing values, outlier detection, date/time parsing, and encoding if needed.
   * Feature scaling where required.
3. Feature engineering

   * Deriving temporal features (month, day, season), interaction terms, or aggregated statistics if applicable.
4. Modeling

   * Baseline regression models and more robust experiments with Ridge and Lasso (regularized linear models).
   * Cross-validation and hyperparameter tuning to find best regularization strengths.
5. Evaluation

   * Metrics used: RMSE, MAE, R².
   * Residual analysis and visual comparison of predictions vs actuals.

## How to run

1. Clone the repository:

   ```bash
   git clone https://github.com/suvancodes/FWI_Prediction_for_Bejaia_and_Sidi-Bel.git
   cd FWI_Prediction_for_Bejaia_and_Sidi-Bel
   ```

2. (Optional) Create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate   # macOS / Linux
   venv\Scripts\activate      # Windows
   ```

3. Install required packages:

   ```bash
   pip install -r requirements.txt
   ```

   *If `requirements.txt` is not present, install commonly used libraries:*

   ```bash
   pip install numpy pandas scikit-learn matplotlib seaborn jupyter
   ```

4. Open and run the notebooks:

   ```bash
   jupyter notebook
   ```

   * Start with `Model Training.ipynb` to follow the end-to-end pipeline.
   * Inspect `Ridge, Lasso Regression.ipynb` for specific regularized linear model experiments.

## Results (quick note)

* The notebooks include evaluation tables and plots comparing model performance (RMSE, MAE, R²). Check the final cells in `Model Training.ipynb` and `Ridge, Lasso Regression.ipynb` for best-found hyperparameters and test-set performance.

## Suggested next steps / improvements

* Try additional models: Random Forest, Gradient Boosting (XGBoost / LightGBM), or simple neural networks.
* Add time series cross-validation if temporal leakage is a concern.
* Expand feature engineering: meteorological indices, lag features, and spatial features if available.
* Deploy a lightweight API to serve predictions for new weather measurements.

## License

Specify a license (e.g., MIT) if you want others to reuse this work. Example:

```
MIT License
```

(Replace or add LICENSE file as needed.)

## Contact

For questions or contributions, open an issue or contact the repository owner: `suvancodes` on GitHub.
