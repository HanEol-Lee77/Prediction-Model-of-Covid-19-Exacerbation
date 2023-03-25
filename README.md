# Prediction-Model-of-COVID-19-Exacerbation

## Abbreviations of Dataset
We open two datasets `master.xlsx`, and `vital.xlsx`. `master.xlsx` is a comprehensive EMR chart dataset for patients hospitalized for each inpatient event. `vital.xlsx` is dataset corresponding to vital sign time series dataset of patients.
 composed of 'serial', 'bt', 'pr', 'spo2', 'sbp', 'dbp' columns. 
The datasets are in ./data folder. The folder structure is as belows:
```
.
├── data
    └── master.xlsx
    └── vital.xlsx
└── README.md
```

These raw datasets are original dataset before data cleaning preprocess. Notice few columns values related to identification information of patients were transformed. Especially we random shifted the 'ins' column information and align 'out', 'occur' columns to ins column for securing private identification information of patients.

- Total number of events: 3748
- Total number of objects: 3743
- Details of columns: 
    - serial : randomly shifted index number of events
    - ins (str dtype): date(YYYY-MM-DD) of patients entering in hospital 
    - out (str dtype): date(YYYY-MM-DD) of a patient going out hospital 
    - occur (str dtype): occuring date(YYYY-MM-DD) of patients showing their symptoms
    - trans (str dtype): binary categorical value whether the patient is transferred to next hospital like tertiary general hospital under Korean Hostpital system at that event ('전원' corresponds to 'transferred', and blank corresponds to 'not transfrred', at that event)
    - trans_date (st dtype): (HH-MM) time value of being transffered
    - gender (str dtype):
    - age (int dtype)
    - abroad (str dtype): O corresponds to True wheter the patients have experience going abroad recently at that evenvt
    - high_risk dtype)
    - history_yn (str dtype): Categorical values of which '유', '무' correspond to True, False respectively 
    - history (str dtype): notes of patient's disease history
    - symptom1 (str dtype): initial symptoms of a patient at the event
    - symptom (str dtype): symptoms of a patient during hospitalization
    - bt, pr, spo2, sbp, dbp (str dtype): vital sign values of the patients at that event (We recommend you converting columns' data dtype from str to float or int dtype.)
    - result (str dtype)
    - wbc, crp, bun, cratinine, tbilirubin, procalcitinin (str dtype): blood test results of a patitent (We recommend you converting columns' data dtype from str to float or int dtype.)

## Contributers
Corresponding Author

## License
Corresponding Author