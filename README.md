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

### Workload

1. **Project Planning and Data Collection** 

   * Problem Definition & Research on Environmental Regulations and NOx Management
   * Data Availability Assessment
   * Data Collection
   * Defining Data Requirements

2. **Data Preprocessing and Exploratory Data Analysis (EDA)**

   * Exploratory Data Analysis (EDA)
   * Visual Insights Extraction
   * Preprocessing
   * Variable Definition

3. **Model Development and Evaluation**

   * Training Strategy and Model Design
   * Baseline Model Development
   * Performance Metric Calculation & Optimization
   * Final Model Selection

4. **Project Outcome and Presentation**

   * Summarizing Analysis Results and Extracting Implications
   * Organizing Utilization Strategies
   * PPT Creation and Visual Material Preparation

### Main Tasks

> **Mainly responsible for Research on Environmental Regulations and NOx Management, EDA, Visual Insights Extraction, and Model Development and Evaluation**

### Key Contributions

* **Time-Series Analysis:** ACF (4-day autocorrelation), lag features
* Engineered time features + lag variables
* Engineered NOx conversion (ppm → g)
* Modeling: `XGBoost`


### 📈 Results

| Unit | RMSE (g) | R²   |
| ---- | -------- | ---- |
| 3    | 504.52   | 0.90 |
| 4    | 492.65   | 0.85 |
| 5    | 219.48   | 0.93 |
| 6    | 282.72   | 0.92 |

---

### Web Service Demonstration

