# Heart-Failure-Prediction
Data Analysis and Machine Learning Classification Work for Classifying Death Condition of Heart Failure

Features:

1. **age** : age of person

1. **anaemia** : Decrease of red blood cells or hemoglobin (boolean)

1. **creatinine_phosphokinase** : Level of the CPK enzyme in the blood (mcg/L)

1. **diabetes** : If the patient has diabetes (boolean)

1. **ejection_fraction** : Percentage of blood leaving the heart at each contraction (percentage)

1. **high_blood_pressure** : If the patient has hypertension (boolean)

1. **platelets** : Platelets in the blood (kiloplatelets/mL)

1. **serum_creatinine** : Level of serum creatinine in the blood (mg/dL)

1. **serum_sodium** : Level of serum sodium in the blood (mEq/L)

1. **time** : Follow-up period (days)


---

## Results

### Analysis

1. Age, ejection_fraction, serum_creatinine and time have correlation with death event. 

1. Time is not an always preferable feature for predicting decease cases.  

1. Level of serum_creatinine in the blood slightly causes increment of percentage of blood leaving the heart at each contraction Also percentage of blood leaving the heart at each contraction is slghtly higher on men than women generally.

1. Percentage of blood leaving the heart at each contraction increases by getting old on deceased ones.

1. Deceased ones have low ejection_fraction values most likely. Also the ones that have extreme serum_creatinine values are the deceased ones.  

1. Serum_creatinine, ejection_fraction and age have correlation among themselves so there is a possibility that they cause each other.

1. Smoking and Diabetes have a less or none effect on death from a heart attack. 

1. Created 3 null hypothesis for Serum_creatinine, ejection_fraction and age for identifying whether they cause each other using pearson's correlation coefficient and spearman's correlation coefficient. The null hypothesis about being age and ejection_Fraction being independent from each other are accepted, others are rejected. 

### Classification 

1. Training data balanced for classification using ***oversampling*** on minority class

1. ***Bagging Classifier*** and ***Random Forest Classifier*** gets %90 accuracy on validation data that is 20 percent of the original data

1. ***Gradient Boost Classifier*** gets %95 accuracy on validation data, with %93 precision on deceased and 100% precision on survivors.

1. ***Stacking*** ***Gradient Boost Classifier*** and ***Random Forest Classifier*** using ***Support Vector Classifier*** as Estimator gets same result as before 

1. Without using time feature, model can reach up to %80 accuracy

