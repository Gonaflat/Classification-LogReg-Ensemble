# Classification - HEART DISEASE PREDICTION
# Introduction
World Health Organization has estimated 12 million deaths occur worldwide, every year due to Heart diseases. Half the deaths in the United States and other developed countries are due to cardio vascular diseases. The early prognosis of cardiovascular diseases can aid in making decisions on lifestyle changes in high risk patients and in turn reduce the complications. This research intends to pinpoint the most relevant/risk factors of heart disease as well as predict the overall risk using logistic regression

# Variables
Each attribute is a potential risk factor. There are both demographic, behavioral and medical risk factors.

# Demographic:
- Sex: male or female(Nominal)
- Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)
# Behavioral
- Current Smoker: whether or not the patient is a current smoker (Nominal)
- Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)
# Medical( history)
- BP Meds: whether or not the patient was on blood pressure medication (Nominal)
- Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
- Prevalent Hyp: whether or not the patient was hypertensive (Nominal)
- Diabetes: whether or not the patient had diabetes (Nominal)
# Medical(current)
- Tot Chol: total cholesterol level (Continuous)
- Sys BP: systolic blood pressure (Continuous)
- Dia BP: diastolic blood pressure (Continuous)
- BMI: Body Mass Index (Continuous)
- Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)
- Glucose: glucose level (Continuous)
# Predict variable (desired target)
- 10 year risk of coronary heart disease CHD (binary: “1”, means “Yes”, “0” means “No”)
# What was applied?
- Data preprocessing.
  - Processing of missing values and duplicates.
  - Initial visualization: Box Plot (for outlier visualization), Histograms (for distribution visualization).
  - Manual correction of some data points that are outliers in features.
  - Application of the Z-score method to identify outliers, followed by adjusting data so that they fall within about 2 - 2.5 standard deviations from the mean (initial outlier values > 3.5 standard deviations).
  - After data preprocessing, a correlation matrix was visualized and the variance_inflation_factor method applied for visual analysis of correlation between features and identifying multicollinearity.
# What models and evaluation were applied?
- Such models as:
  - Logistic Regression,
  - GradientBoostingClassifier,
  - XGBoost,
  - CatBoostClassifier
- Specific pipelines were created for each model, and the GridSearch method was utilized.
- All models employed the Scaler - StandardScaler.
- The models were evaluated based on:
  - F1-Score,
  - Roc-Auc score,
  - Accuracy and were fine-tuned using the Accuracy method,
  - Mean cross-validated accuracy and Classification Report were also used for model evaluations.
- For the visualization of results:
  - Roc-Auc,
  - Precision - Recall
