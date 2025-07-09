
# ResCurve: A DCA & Forecasting Project Using Volve Data

This project analyzes production performance from the **Volve Field** on the Norwegian Continental Shelf using decline curve models and simplified material balance techniques.

---

##  Objective

Using historical production data for multiple wellbores, the project aims to:

- Apply **Decline Curve Analysis (DCA)** models: *Exponential*, *Harmonic*, and *Hyperbolic*
- Estimate **Original Oil in Place (OOIP)** via analytical equations
- Forecast future oil production and **Estimate Ultimate Recovery (EUR)**
- Visualize decline behavior and reservoir potential with insightful plots
P
---

##  Methodology

We follow a structured pipeline:

```
Excel Data → Load & Clean → DCA Fitting → OOIP Estimation → Forecasting → Interpretation
```

---

##  Key Findings

###  Decline Curve Fitting

The **hyperbolic model** showed the best fit with:
- **RMSE = 944.97**, **R² = 0.6769**
- This model was selected for production forecasting and reserve estimation.

![Decline Curve Fits](Decline_Curve_Fits.png)

---

### Forecasting & EUR

- Production was forecasted over 5,000 days using the hyperbolic fit.
- An economic cutoff rate of **100 Sm³/day** was assumed.
- **Economic limit** reached at ~4048 days  
- **Estimated Ultimate Recovery (EUR)** = **5,026,990 Sm³**

![Forecast with Economic Limit](Forcast_With_Economic_Limit.png)

---

### OOIP Estimation

Using a simplified material balance equation and assumed formation volume factor:

> **Estimated OOIP** = **609,865,650 Sm³**

---

## 🛠️ Tools & Libraries

- `pandas`, `numpy` – Data manipulation and numerical operations  
- `matplotlib` – Visualization  
- `scipy.optimize.curve_fit` – Nonlinear model fitting  
- `sklearn.metrics` – RMSE and R² evaluation  
- `openpyxl` – Excel reading  

---

##  Dataset

**Source:** [Equinor Volve Field Dataset](https://www.equinor.com/energy/volve-data-sharing)  
**Acknowledgment:**

> *We gratefully acknowledge Equinor ASA for providing the open Volve dataset for research and educational purposes.*

 *Note: PVT data was unavailable at the time due to site maintenance. A standard Bo of 1.2 reservoir bbl/STB was assumed.*

---

##  Plots

| Oil Rate – F-1 C | Oil Rate – F-12 | Rate & Cumulative |
|------------------|------------------|--------------------|
| ![F-1 C](Well_F-1.png) | ![F-12](Well_F_12.png) | ![Cumulative](Rate_&_Cumulative.png) |

---

##  How to Use

Clone the repo and run the notebook:

```bash
git clone https://github.com/yourusername/ResCurve-Volve.git
cd ResCurve-Volve
jupyter notebook "ResCurve A DCA & Forecasting Project Using Volve Data.ipynb"
```

---

##  Author

**Anuri Nwagbara**  
Reservoir & Process Engineer

---

##  License

MIT License – see `LICENSE.md` for details.
