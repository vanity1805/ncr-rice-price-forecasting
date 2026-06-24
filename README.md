# NCR Retail Rice Price Forecasting & Explainability

An interactive **Streamlit** dashboard that visualizes the outputs of two Stacked
LSTM models (multivariate vs. univariate) for forecasting weekly Regular-Milled
retail rice prices in the National Capital Region (NCR), with SHAP-based
explainability.

## Modules
- **Price Forecast** — 12-week forecast vs. actual prices, with summary cards.
- **Benchmarking** — RMSE / MAE / MAPE / R² metrics, comparison table, and the
  Diebold-Mariano significance test.
- **Explainability** — global SHAP (bar / beeswarm), a local SHAP waterfall
  per forecast week, and a feature dependence plot.

A global model selector in the header switches all visualizations between the
multivariate and univariate models.

## Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
```

## Note
This is a mock-up: all displayed values are placeholder/seeded data pending
training of the Stacked LSTM models. Once the models are trained, replace the
mock dictionaries and `local_shap()` body in `app.py` with the real exported
predictions, metrics, and SHAP values.
