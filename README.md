# Battery Remaining Useful Life Prediction

Predict the Remaining Useful Life (RUL) of batteries based on features derived from voltage and current behavior.

The dataset, obtained from the Hawaii Natural Energy Institute, includes information on 14 NMC-LCO 18650 batteries. These batteries, with a nominal capacity of 2.8 Ah, were cycled over 1000 times at 25°C with a CC-CV charge rate of C/2 and a discharge rate of 1.5C.

### Dataset Information
- **Variables:**
  - Cycle Index: number of cycles
  - F1: Discharge Time (s)
  - F2: Time at 4.15V (s)
  - F3: Time Constant Current (s)
  - F4: Decrement 3.6-3.4V (s)
  - F5: Max. Voltage Discharge (V)
  - F6: Min. Voltage Charge (V)
  - F7: Charging Time (s)
  - Total time (s)
  - RUL: target

### Dataset Source
You may access the dataset on Kaggle: [Battery Remaining Useful Life (RUL)](https://www.kaggle.com/datasets/ignaciovinuales/battery-remaining-useful-life-rul)

## Content

1. **Data Exploration:**
   - Summary statistics of the dataset.

2. **Exploratory Data Analysis (EDA):**
   - Distribution of Remaining Useful Time (RUL).
   - Correlation heatmap of features with RUL.
   - Pair plot of selected features and RUL.

3. **Data Preprocessing:**
   - Removal of the Cycle_Index feature.
   - Data splitting into target and independent variables.
   - Standardization of features using StandardScaler.

4. **Model Selection and Evaluation:**
   - Training and evaluation of various regression models:
     - RandomForestRegressor, AdaBoostRegressor, GradientBoostingRegressor, BaggingRegressor, SVR, DecisionTreeRegressor, ExtraTreeRegressor, LinearRegression, SGDRegressor, KNeighborsRegressor.
   - Selection of the best-performing model (BaggingRegressor).

5. **Feature Importance Analysis:**
   - Evaluation of feature importances for the selected model.

6. **Ensemble Modeling:**
   - Stacking of multiple models (RandomForestRegressor, BaggingRegressor, KNeighborsRegressor, ExtraTreeRegressor, DecisionTreeRegressor).
   - Training and evaluation of a meta-model (Lasso regression) on stacked predictions.

7. **Results:**
   - Presentation of model scores, feature importances, and visualizations.

8. **Conclusion:**
   - Summary of findings and insights.

## Note
This analysis is part of the broader task of predicting the remaining useful life of batteries, providing valuable information for maintenance and resource planning. The choice of models, preprocessing techniques, and ensembling strategies aims to achieve accurate predictions and robust performance.
