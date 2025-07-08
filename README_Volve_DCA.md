
# Material Balance & Decline Curve Analysis – Volve Field, Norway

This project analyzes production data from the **Volve Field (Norwegian Continental Shelf)** to estimate reserves, evaluate production decline, and forecast future oil output using classic decline curve models.

We apply decline curve analysis (DCA) and simplified material balance methods using Python workflows to gain insights into reservoir performance.

---

## 🎯 Objective

To evaluate reservoir performance by:
- Applying DCA models (exponential, harmonic, hyperbolic)
- Estimating **Original Oil in Place (OOIP)**
- Forecasting **future production and Estimated Ultimate Recovery (EUR)**
- Supporting decision-making with **clean, visual plots**

---

## 🧠 Methodology

We follow a structured workflow:

```
Excel Data → Inspect → Filter Best Well(s) → Apply DCA Models → Forecast → Interpret
```

---

## 📊 Key Findings

### Decline Curve Fitting
Three decline models were evaluated:
- **Exponential**
- **Harmonic**
- **Hyperbolic**

Model performance was assessed using **RMSE** and **R²** scores. The hyperbolic model showed the best fit for the selected well (15/9-F-12).

### OOIP Estimation

OOIP was estimated using hyperbolic model parameters and a simplified material balance equation:
\[
\text{OOIP} = \frac{q_i}{D \cdot b} \cdot B_o
\]
Assumed \( B_o = 1.2 \), until full PVT data is accessible.

### Forecasting & Economic Limit

Future production was forecasted for 5 years. A **cutoff rate** of 100 Sm³/day was applied to estimate the **economic limit** and **EUR**.

---

### 📈 Visual Outputs

- Oil Rate vs Time plots  
- Decline Curve Model fits  
- Forecast with Economic Limit overlay  
- EUR estimation

*(Include screenshots here if uploading to GitHub)*

---

## 🧰 Tools & Libraries

- `pandas` – Data cleaning & manipulation  
- `matplotlib` – Visualization  
- `numpy` – Numerical computation  
- `openpyxl` – Excel file reading  
- `scipy.optimize.curve_fit` – Decline model fitting  
- `sklearn.metrics` – Model evaluation (RMSE, R²)

---

## 📁 Dataset

**Source**: [Equinor – Volve Field Dataset](https://www.equinor.com/energy/volve-data-sharing)  
**Data**: Daily oil production from 7 wellbores, including oil, gas, and water volumes.

### 📚 Acknowledgment

> This project uses publicly available data from **Equinor ASA**’s Volve Field.  
> We acknowledge **Equinor ASA** for sharing this dataset for open research and education.  
> All rights to the data belong to Equinor.

⚠️ *At the time of this analysis, the full PVT dataset was temporarily unavailable due to maintenance. Assumed values were used where needed.*

---

## 💻 Usage

1. Clone the repository  
2. Place the Excel file in the `data/` folder  
3. Run the notebook:
```bash
jupyter notebook Volve_DCA_Analysis.ipynb
```

---

## 🔍 Summary

This project demonstrates how decline curve analysis and material balance principles can be combined to estimate reserves, identify decline trends, and predict future oil production from historical data.

---

## 👩🏽‍🔬 Author

**Anuri Nwagbara**  
Reservoir & Process Engineer  

---

## 📄 License

This project is licensed under the MIT License.
