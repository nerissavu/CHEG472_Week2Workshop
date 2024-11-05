# CHEG472_Week2Workshop

# Biochar Sorption Dataset Analysis

## Objective
This study investigates the relationships between biochar characteristics, production parameters, and their effectiveness in removing pharmaceutical compounds from water.

## Dataset Overview
- Source data contains biochar properties and pharmaceutical sorption characteristics
- 86 samples with 13 original columns
- Focuses on biochar production conditions and sorption capacity

## Features
- Production parameters:
  - Temperature (TemP): 300-950°C
  - Time: 0.1-480 min
  - PS (Particle Size)
  - BET Surface Area
  - PV (Pore Volume)
- Chemical properties:
  - C, H, N, O content
- Various biomass types and target pharmaceuticals (TPs)

## Data Processing
1. Cleaned missing values
2. Removed first index column
3. One-hot encoded categorical variables:
   - Biomass types
   - Target pharmaceuticals (TPs)
4. Split into features (X) and target (y):
   - Target: BET surface area
   - Features: All other parameters

## Key Visualizations
- Correlation heatmap
- Pair plots
- Distribution plots (histogram, boxplot)
- Scatter plots
- Violin plots for categorical analysis

## Usage
```python
import pandas as pd
df = pd.read_excel('Dataset Clean.xlsx')
df_encoded = pd.get_dummies(df, columns=['Biomass', 'TP'])
```

## Dependencies
- pandas
- seaborn
- matplotlib
- scikit-learn
