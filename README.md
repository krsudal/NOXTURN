# NOXTURN: Power Plant NOx Emission Prediction

### Background

* With rising electricity demand, emissions are also increasing, highlighting the need for effective reduction strategies.
* Nitrogen oxides (NOx) is a major contributor to fine dust, crop damage, and acid rain, negatively impacting public health and industrial activities.
* The emission sources in the energy sector are clearly identifiable and can be directly regulated through policy.
* Targeted power plant is planning to be equipped with a digital operating system, and has consistently been listed among the top NOx-emitting facilities.

### Project Objective

* Predict NOx emissions without internal sensored-data using only public external data
* Provide a low-cost, practical model for plants

---

### Dataset

* **KOEN:** Generation, operating hours, flow, NOx, O₂
* **KPX:** National demand, plant-level trading volume
* **KMA:** Temperature, humidity, wind (for missing values)

### ⚙️ Methodology

* **Preprocessing:** Unit unification (daily), NOx conversion (ppm → g), missing value imputation
* **Time-Series Analysis:** ACF (4-day autocorrelation), lag features, weekday/holiday effects
* **Modeling:**

  * Step 1: Flow prediction (`XGBoost`)
  * Step 2: NOx prediction using predicted flow + weather + generation
* **Optimization:** Hyperparameter tuning with `Optuna`

### 📈 Results

| Unit | RMSE (g) | R²   |
| ---- | -------- | ---- |
| 3    | 504.52   | 0.90 |
| 4    | 492.65   | 0.85 |
| 5    | 219.48   | 0.93 |
| 6    | 282.72   | 0.92 |

---

### Key Contributions

* Built integrated dataset from multiple public sources
* Engineered **time features + lag variables** for higher accuracy
* Designed a **two-step model** (Flow → NOx)
* Improved model performance through **per-unit optimization**
