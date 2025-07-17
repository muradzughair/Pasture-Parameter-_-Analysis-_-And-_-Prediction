# Pasture Parameter Estimation Using Remote Sensing and Weather Data

This project provides descriptive and predictive data analysis for **pasture parameter estimation**, using a dataset from the research paper:  
📄 _"A dataset for pasture parameter estimation based on satellite remote sensing and weather variables"_  
➡️ [Read the Paper](https://www.sciencedirect.com/science/article/pii/S235234092400177X)

---

## 📌 Objective

The goal of this project is to analyze biomass and forage quality in pasture environments using weather and satellite data. We apply:
- **Descriptive analytics** to explore patterns in pasture biomass and quality
- **Predictive modeling** to forecast key forage variables using machine learning
- Data-driven insights for sustainable agriculture and improved pasture management

---

## 📂 Project Structure

```bash
PastureParameterEstimation/
│
├── data/
│   └── Complete_Dataset_updated.csv      # Dataset sourced from research paper
│
├── 1_Descriptive_Pasture_Analysis.ipynb  # Visualization, correlation, forage quality analysis
├── 2_Predictive_Pasture_Modeling.ipynb   # ML modeling: Linear Regression, Decision Tree, LSTM
│
├── README.md
└── requirements.txt
```
Dataset Overview
Source: Satellite remote sensing + weather + field-measured forage data

Features include:

Biomass (kg/ha)

Vegetation indices (e.g., SAVI)

Weather parameters (Temperature, Rainfall, Wind, Solar Radiation, etc.)

Forage quality metrics: NDF, ADF, Crude Protein

Grazing activity (animal presence)

Target variables: Biomass, forage quality indicators (CP, NDF, ADF)

📊 Descriptive Analytics Highlights
Biomass Distribution

Mean: ~4302 kg/ha; Median: ~3190 kg/ha → indicates right-skewed distribution.

Grazed areas showed consistently lower biomass values.

Spatial Analysis

Scatter plots show non-uniform biomass distribution due to environmental and grazing effects.

High SAVI correlates with high biomass → healthy vegetation = better forage.

Impact of Environmental Factors

SAVI: Strong positive correlation with biomass

Evapotranspiration (EVAPOT): Negative correlation → high water loss reduces productivity

Radiative Direct Avg: Weak correlation with biomass

Grazing Impact

Grazed paddocks showed lower biomass vs. ungrazed (S1, S2)

Suggests overgrazing reduces growth → rotational grazing recommended

Forage Quality Insights

Low NDF/ADF and high CP = high-quality forage

Best forage observed under:

Low rainfall (2–3 mm)

Moderate temperatures (~30–32°C)

Moderate wind speed (9–15 m/s)

🤖 Predictive Modeling Summary
Preprocessing

Handled datetime conversion

Applied one-hot encoding for categorical variables

Used SelectKBest and RFE for feature selection

Models Implemented

Linear Regression

Decision Tree Regressor

Exponential Smoothing (time series)

LSTM (Neural Network for sequence learning)

Results Summary

Model	R² Score	MAE	Notes
Linear Regression	~0.65	Moderate	Simple, consistent across splits
Decision Tree	~0.82	Lower	High variance across random splits
Exponential Smoothing	1.00	0	Excellent fit (trend-based)
LSTM	0.77	~883	Strong temporal modeling

📈 Key Insights for Decision-Making
Data analytics supports grazing strategy optimization (e.g., identify overgrazed areas).

Environmental conditions can guide planting and irrigation decisions for higher forage quality.

Biomass prediction models help farmers plan livestock feeding and pasture rotation effectively.

Visualizations (heatmaps, scatter plots, box plots) allow intuitive understanding of complex environmental relationships.

🛠️ Tools & Technologies
Python

pandas, NumPy

scikit-learn, seaborn, matplotlib

Keras (for LSTM)

statsmodels (for smoothing)

📎 Citation (Dataset Source)
Jiménez-Muñoz, Estelí et al. “A dataset for pasture parameter estimation based on satellite remote sensing and weather variables.” Data in Brief (2024).
https://doi.org/10.1016/j.dib.2024.110634

