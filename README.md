# Heart Health Dataset

This dataset contains clinical and diagnostic information for patients and is commonly used to predict heart disease presence. It includes demographic, diagnostic, and lab result features.

## Dataset Description

### Columns
| **Feature**         | **Description**                                                                                         |
|----------------------|---------------------------------------------------------------------------------------------------------|
| **age**             | Age of the patient in years.                                                                           |
| **sex**             | Sex of the patient:                                                                                     |
|                      | - `1`: Male                                                                                            |
|                      | - `0`: Female                                                                                          |
| **cp**              | Chest pain type:                                                                                        |
|                      | - `1`: Typical angina                                                                                  |
|                      | - `2`: Atypical angina                                                                                 |
|                      | - `3`: Non-anginal pain                                                                                |
|                      | - `4`: Asymptomatic                                                                                    |
| **trestbps**        | Resting blood pressure (in mm Hg) on admission to the hospital.                                         |
| **chol**            | Serum cholesterol level in mg/dl.                                                                      |
| **fbs**             | Fasting blood sugar > 120 mg/dl:                                                                        |
|                      | - `1`: True                                                                                            |
|                      | - `0`: False                                                                                           |
| **restecg**         | Resting electrocardiographic results:                                                                   |
|                      | - `0`: Normal                                                                                          |
|                      | - `1`: ST-T wave abnormality (e.g., T wave inversions, ST elevation or depression > 0.05 mV)            |
|                      | - `2`: Probable or definite left ventricular hypertrophy by Estes' criteria                            |
| **thalach**         | Maximum heart rate achieved during exercise.                                                           |
| **exang**           | Exercise-induced angina:                                                                                |
|                      | - `1`: Yes                                                                                             |
|                      | - `0`: No                                                                                              |
| **oldpeak**         | ST depression induced by exercise relative to rest.                                                    |
| **slope**           | Slope of the peak exercise ST segment:                                                                  |
|                      | - `1`: Upsloping                                                                                       |
|                      | - `2`: Flat                                                                                            |
|                      | - `3`: Downsloping                                                                                     |
| **ca**              | Number of major vessels (0-3) colored by fluoroscopy.                                                  |
| **thal**            | Thalassemia test results:                                                                               |
|                      | - `3`: Normal                                                                                          |
|                      | - `6`: Fixed defect                                                                                    |
|                      | - `7`: Reversible defect                                                                               |
| **heart_disease**   | Diagnosis of heart disease (angiographic disease status):                                               |
|                      | - `0`: < 50% diameter narrowing (no disease)                                                           |
|                      | - `1`: > 50% diameter narrowing (presence of disease)                                                  |
|                      | - `2-4`: Presence of more severe disease categories (based on severity levels).                        |

## Target Variable
- **heart_disease** is the target variable for prediction. Values include:
   - `0`: Absence of heart disease (< 50% narrowing)
   - `1, 2, 3, 4`: Presence of heart disease (> 50% narrowing)

## Usage
This dataset can be used for:
1. **Exploratory Data Analysis (EDA)**: Understanding trends, distributions, and correlations.

## INSIGHTS OF THE DATASET AFTER EXPLORATORY DATA ANALYSIS
### Significant Predictors of Heart Disease

1. **Distribution of Heart Disease**

    `Key Findings:`

    The majority of individuals without heart disease (heart_disease = 0) have a higher count in the rest_ecg categories, particularly indicating no abnormality.

    As the severity of heart disease increases (from 1 to 4), counts in rest_ecg categories showing left ventricular hypertrophy and ST-T wave abnormalities also increase.

    `ECG Abnormalities:`

    Patients with severe heart disease (category 4) exhibit significant ECG abnormalities, suggesting these findings may be predictive of heart disease.

    `Diagnostic Insights:`

    rest_ecg could serve as a useful diagnostic tool for identifying patients at risk.

    ![restecg](Images/restecg.png)


2. **Heart Disease Distribution by Gender**

    `Key Findings:`

    Males have a significantly higher occurrence of heart disease compared to females.

    Across all heart disease severity levels (1–4), males show higher counts.

    Males also have more individuals in the "no heart disease" category than females.

    `Trends:`

    Severe heart disease (categories 3 and 4) is notably higher in males, whereas females show fewer cases in these categories.

    `Conclusion:`

    Males appear to be more susceptible to heart disease at all levels.



3. **Chest Pain Types Distribution**

    `Key Findings:`

    Individuals without heart disease (heart_disease = 0) predominantly experience Asymptomatic and Non-anginal Pain types.

    Non-anginal Pain is most common across all categories but more frequent in healthy individuals.

    `Severity Correlation:`

    As heart disease severity increases (1–4), Typical Angina and Atypical Angina counts increase.

    `Insights:`

    Typical and Atypical Angina types are linked to higher heart disease risk.

    Comprehensive evaluation of symptoms and risk factors remains essential.



4. **Fasting Blood Sugar Distribution**

    `Key Findings:`

    Individuals without heart disease (heart_disease = 0) generally have normal fasting blood sugar (False).

    Higher fasting blood sugar levels (True) are associated with increased heart disease severity.

    `Risk Indicators:`

    Elevated fasting blood sugar may serve as a potential risk factor for heart disease.




5. **Max Heart Rate by Heart Disease Severity**

- `Key Findings:`

    Individuals with heart disease severity levels 1 and 2 show lower maximum heart rates compared to healthy individuals (heart_disease = 0).

    `Gender Trends:`

    Males generally exhibit higher maximum heart rates across all heart disease levels compared to females.

    Variability in heart rates within each severity level remains consistent across genders.

    `Clinical Implications:`

    The decreasing trend in maximum heart rate with increasing heart disease severity suggests reduced cardiovascular fitness.

    Gender differences may influence cardiovascular responses.



## Notable Patterns

   - Gender Differences in Chest Pain Types

    `Key Observations:`

    Males show a higher prevalence of Typical Angina and Atypical Angina.

    Females more commonly report Non-anginal Pain and Asymptomatic Pain.

    `Insights:`

    Gender-specific patterns suggest differences in how men and women experience or report chest pain.

    Age Influence on Chest Pain Types

    `Observations:`

    The average age for Typical Angina and Atypical Angina is higher compared to Non-anginal Pain and Asymptomatic Pain.

    Older individuals are more likely to experience severe chest pain types.

    `Variability:`

    Error bars indicate overlapping age ranges across pain types, highlighting individual variability.

## Summary 
- ECG Findings and Fasting Blood Sugar levels show potential as diagnostic tools for predicting heart disease risk.

    Gender Differences: Males are more susceptible to severe heart disease, with specific patterns in chest pain types.

    Chest Pain Types:

    Typical Angina and Atypical Angina are associated with severe heart disease.

    Non-anginal Pain and Asymptomatic Pain are more common in healthy individuals, particularly among females.

    Max Heart Rate: Decreases with heart disease severity and shows gender-specific differences.

