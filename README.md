# XAI Analysis for Diabetes Prediction

## Description
This project applies Explainable AI (XAI) methods to the Pima Indian Diabetes dataset, leveraging various machine learning models to predict diabetes. The models used include Convolutional Neural Networks (CNN), Multi-Layer Perceptrons (MLP), Random Forest Regression, and Recurrent Neural Networks (RNN). Each model's predictions are interpreted using SHAP, LIME, and ALE, three of the most prominent XAI techniques, to provide insights into the decision-making process of each algorithm.

## XAI Techniques
- **SHAP (SHapley Additive exPlanations)**: SHAP values interpret the impact of having a certain value for a given feature in comparison to the prediction we'd make if that feature took some baseline value. It's a game theoretic approach to explain the output of any machine learning model.
  
- **LIME (Local Interpretable Model-agnostic Explanations)**: LIME helps us understand the predictions of any classifier in an interpretable and faithful manner, by approximating it locally with an interpretable model.
  
- **ALE (Accumulated Local Effects)**: ALE plots show the main effects of features and are a faster alternative to partial dependence plots (PDPs), which explain the features' contributions based on the accumulation of local effects.

## Model Performance
The accuracies achieved by our models on the Pima Indian Diabetes dataset are as follows:
- MLP: 75%
- CNN: 70%
- RNN: 80%
- Random Forest Regression: F-score of 30%

## Dataset
The dataset utilized is the Pima Indian Diabetes dataset, which consists of several medical predictor variables and one target variable, Outcome. Predictor variables include the number of pregnancies the patient has had, their BMI, insulin level, age, and so on.

## Output
Multiple graphs for each XAI model under each ml model were compared which can be seen in the Comparative Study PDF.

The primary comparisons were:

### SHAP summary plots 

<p align="center">
  <img src="Output/SHAP summary plots/CNN - SHAP summary.png" title="CNN SHAP Summary Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP summary plots/RNN - SHAP summary.png" title="RNN SHAP Summary Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP summary plots/REG - SHAP summary.png" title="REG SHAP Summary Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP summary plots/MLP - SHAP summary.png" title="MLP SHAP Summary Plot" width="500" height="auto" />
</p>

SUMMARY - 
Common Important Features: Across all models, Glucose, BMI, and Age consistently emerge as key predictors.
Variability Across Models: The RNN model emphasizes Age and BMI more than the others, while the CNN and Regression models strongly highlight Glucose. The MLP model shows a broader distribution of feature impacts, reflecting the non-linear interactions it captures.
Model-Specific Insights: Each model's unique architecture influences how it prioritizes different features, providing complementary perspectives on feature importance.

### LIME plots

<p align="center">
  <img src="Output/LIME plots/CNN - LIME.png" title="CNN LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/LIME plots/RNN - LIME.png" title="RNN LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/LIME plots/REG - LIME.png" title="REG LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/LIME plots/MLP - LIME.png" title="MLP LIME Plot" width="500" height="auto" />
</p>

SUMMARY - 
The LIME plots compare four models: CNN, MLP, RNN, and a regression model. While the classification models (CNN, MLP, RNN) share similar feature importance rankings, their predictions vary significantly. The CNN predicts class 1 (67% probability), while MLP and RNN predict class 0 (84% and 86% respectively). The regression model uses a different scale and feature values, predicting 0.50 on a 0-1 scale. MLP and RNN plots are very similar, while the CNN plot shows more distinct probabilities. The regression plot stands apart due to its different format and scale. These differences highlight how various model architectures interpret the same features differently, resulting in distinct predictions and explanations.

### SHAP vs LIME plots

<p align="center">
  <img src="Output/SHAP vs LIME plots/CNN - SHAP vs LIME.png" title="CNN SHAP vs LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP vs LIME plots/RNN - SHAP vs LIME.png" title="RNN SHAP vs LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP vs LIME plots/REG - SHAP vs LIME.png" title="REG SHAP vs LIME Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/SHAP vs LIME plots/MLP - SHAP vs LIME.png" title="MLP SHAP vs LIME Plot" width="500" height="auto" />
</p>


### ALE plots

<p align="center">
  <img src="Output/ALE plots/CNN - ALE.png" title="CNN ALE Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/ALE plots/RNN - ALE.png" title="RNN ALE Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/ALE plots/REG - ALE.png" title="REG ALE Plot" width="500" height="auto" />
</p>

<p align="center">
  <img src="Output/ALE plots/MLP - ALE.png" title="MLP   ALE Plot" width="500" height="auto" />
</p>

## Acknowledgments
- Credit to the creators of the Pima Indian Diabetes dataset.
- Thanks to the developers and contributors of SHAP, LIME, and ALE for their accessible and powerful XAI frameworks.
