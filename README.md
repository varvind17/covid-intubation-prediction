# covid-intubation-prediction

Instructions:
1. Arrange Data
  a. Arrange timeseries data into a dataframe/ worksheet in the following order where each row represents a timestamp, and each row corresponds to the following variables in order: 'PAO2', 'PACO2', 'HCO3', 'PH_x', 'Oxygen saturation','C REACTIVE PROTEIN', 'Creatinine', 'D-DIMER', 'Platelets', 'WBC_x', 'CAC - TEMPERATURE', 'CAC - PULSE', 'CAC - RESPIRATIONS', 'systolic', 'diastolic'.

  b. Arrange static data in the following order: COPD, Diabetes (Y/N), Diabetes With Complications (Y/N), Renal Disease (Y/N), Liver Disease (YN), HTN (Y/N), Hypertension with Complications (Y/N).

2. Use function dfinterpolate() to interpolate data from dataframe, and merge_train_c() to merge timeseries and static data.

3. Load modeland make prediction:
  a.Load pickeled model
  ```import pickle
with open('/home/jkim/varun/models/04_27_2020_rfmodel.pickle', 'rb') as handle:
    clf = pickle.load(handle)```
    
  b. Use clf.predict_proba() to generate prediction from model.
