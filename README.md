# Predicting-10-Year-Coronary-Heart-Disease-Risk-using-Machine-Learning-Calibration-Explainability
Accepted at 6th International Conference on Innovative Computing (ICIC) in December 2025. 
One of the primary causes of death in the globe is still heart disease.

The goal of this study is to apply machine learning to estimate the 10-year risk of coronary heart disease (CHD).

Pursuing more precision wasn't the only objective. Rather, the emphasis was on issues that are crucial in a hospital environment:

Making trustworthy risk assessments (without being blindly optimistic)
Knowing the rationale behind the model's choices
Examining the differences in performance between various patient groups
Examining the model's performance on fresh, untested populations

**Methods** 
The project adheres to a planned pipeline:
1. Information
• About 4,000 patients in the Framingham Heart Study
• Goal: TenYearCHD (0 = No illness, 1 = CHD)

2. Preparation
• Missing values (mean, median, and mode) are addressed
• Scaling features (standardization)
• Binary encoding (sex, for example)
3. Engineering Features
Systolic blood pressure minus diastolic blood pressure equals pulse pressure.
• Total cholesterol divided by HDL is the cholesterol ratio.
• Indicators of missing values
4. Models
• Logistic regression (the model that was ultimately chosen)
The Random Forest
5. Assessment
Models were assessed using:
• AUROC (ability to discriminate)
• AUPRC (performance on data that is unbalanced)
• Brier Score (quality of calibration)
• Curves for calibration
• Analysis of subgroups (age, gender, diabetes)
• Analysis of Decision Curves (clinical utility)
<img width="2100" height="1800" alt="roc_all (3)" src="https://github.com/user-attachments/assets/32a57189-89e4-4fce-82f0-0786849d0f68" />
<img width="2400" height="1800" alt="decision_curve (1) (2)" src="https://github.com/user-attachments/assets/06ff8545-f8ca-425d-a7b8-d8c60defaa16" />


**Findings**

Logistic Regression achieved AUROC = 0.69
Provided the most reliable probability estimates
Random Forest showed compartively lower performance and poorer calibration


**External Verification**

A Pakistani dataset (Faisalabad Institute of Cardiology) was used to test the model.

**Results**:
On the new population, performance declined
Forecasts grew overconfident

This focuses on an essential technical issue:
Models may not always be applicable to different populations.

**Subgroup analysis between groups**

Age groups
Gender
Patients with diabetes versus those without

**How to Run**

1. Download or clone the repository 2. Install required Python libraries (pandas, numpy, scikit-learn, matplotlib, seaborn, shap) 3. Run the training or evaluation scripts

Author
Azhan Khan
