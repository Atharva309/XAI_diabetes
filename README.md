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
![CNN-SHAPSummary](Output/SHAP summary plots/CNN - SHAP summary.png)
![MLP-SHAPSummary](Output/SHAP summary plots/MLP - SHAP summary.png)
![RNN-SHAPSummary](Output/SHAP summary plots/RNN - SHAP summary.png)
![REG-SHAPSummary](Output/SHAP summary plots/REG - SHAP summary.png)

### LIME plots
![CNN-LIME](XAI_diabetes/Output/LIME plots/CNN - LIME.png)
![MLP-LIME](Output/LIME plots/MLP - LIME.png)
![RNN-LIME](Output/LIME plots/RNN - LIME.png)
![REG-LIME](Output/LIME plots/REG - LIME.png)

### SHAP vs LIME plots
![CNN-SHAPvsLIME](Output/SHAP vs LIME plots/CNN - SHAP vs LIME.png)
![MLP-SHAPvsLIME](Output/SHAP vs LIME plots/MLP - SHAP vs LIME.png)
![RNN-SHAPvsLIME](Output/SHAP vs LIME plots/RNN - SHAP vs LIME.png)
![REG-SHAPvsLIME](Output/SHAP vs LIME plots/REG - SHAP vs LIME.png)

### ALE plots
![CNN-ALE](Output/ALE plots/CNN - ALE.png)
![MLP-ALE](Output/ALE plots/MLP - ALE.png)
![RNN-ALE](Output/ALE plots/RNN - ALE.png)
![REG-ALE](Output/ALE plots/REG - ALE.png)

## Acknowledgments
- Credit to the creators of the Pima Indian Diabetes dataset.
- Thanks to the developers and contributors of SHAP, LIME, and ALE for their accessible and powerful XAI frameworks.
