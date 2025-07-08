# 📈 Material Balance & Decline Curve Analysis – Volve Field, Norway

This project performs **Decline Curve Analysis (DCA)** and **Material Balance calculations** using real production data from the **Volve Field** on the Norwegian Continental Shelf, provided by **Equinor ASA**.

---

## 🔖 Project Objective
To evaluate reservoir performance and estimate key production parameters by:
- Applying **Decline Curve Models** (Exponential, Harmonic, Hyperbolic)
- Estimating **Original Oil in Place (OOIP)**
- Forecasting **future oil production** and **ultimate recovery**
- Visualizing **production trends** and **forecast results**

---

## ⚖️ Methodology
1. **Data Preparation**
   - Load and inspect Excel data (daily oil production)
   - Filter individual wells
   - Sort and clean production records

2. **Production Trend Visualization**
   - Plot oil rate and cumulative production over time

3. **Decline Curve Fitting**
   - Fit Exponential, Harmonic, and Hyperbolic models using `curve_fit`
   - Evaluate model accuracy using **RMSE** and **R²**
   - Choose best-fit model based on both statistical and practical insights

4. **Reserves Estimation**
   - Estimate **OOIP** from hyperbolic model using simplified material balance
   - Forecast future oil rates
   - Determine **economic cutoff** and calculate **Estimated Ultimate Recovery (EUR)**

---

## 📊 Key Visualizations

| Model Fit Comparison | Production Forecast |
|----------------------|---------------------|
| ![Model Fit](./figures/model_fit.png) | ![Forecast](./figures/forecast.png) |

Additional figures include:
- Cumulative oil plots
- Decline curve overlays
- EUR shaded regions with economic limits

---

## ⚙️ Tools & Libraries Used
- `pandas` – data wrangling
- `matplotlib` – plotting
- `numpy` – numerical operations
- `scipy.optimize.curve_fit` – regression for DCA fitting
- `sklearn.metrics` – model evaluation (RMSE, R²)
- `openpyxl` – Excel file support

---

## 📂 Dataset
**Source:** [Equinor Volve Field Dataset](https://www.equinor.com/energy/volve-data-sharing)

This analysis uses publicly available data from **Equinor ASA** including:
- Oil, gas, and water production volumes (Sm³)
- Well names and production dates
- Metadata on production and injection

> **Note**: The **PVT dataset** was unavailable during analysis due to maintenance. An assumed formation volume factor (Bₒ = 1.2) was used.

---

## 📄 Summary of Findings
- **Best-Fit Model**: Hyperbolic model showed the best performance with lowest RMSE and highest R².
- **OOIP Estimate**: ~610 million Sm³ (based on hyperbolic decline and assumed Bₒ)
- **Forecast Horizon**: ~5 additional years until economic limit reached
- **EUR**: Estimated from cumulative forecasted volumes up to cutoff rate (100 Sm³/day)

---

## 👨‍💼 Author
**Anuri Nwagbara**  
Reservoir & Sustainability Analyst  
[LinkedIn](https://linkedin.com/in/anuri-nwagbara) | [GitHub](https://github.com/Anuri-ops)

---

## 🌐 License
This project is licensed under the **MIT License**. Please refer to the `LICENSE` file for details.

---

## 📃 Acknowledgments
We gratefully acknowledge **Equinor ASA** for providing high-quality open-access datasets for research and education.
All rights to the data belong to Equinor.

> This project is intended for educational and non-commercial purposes only.

