# Early-Stage Diabetes Classification Tool
Sector: Clinical Health (Diagnostics)

Type: Supervised Machine Learning, Classification

Skills Used: Python (Pandas, Scikit-learn), Classification Modeling (Random Forest), Data Imputation (Median), Feature Scaling, Precision-Recall Analysis.

## I. Project Goal and Clinical Challenge

### The Challenge: Diagnostic Lag

Diagnosis for chronic conditions is often delayed until symptoms are severe, increasing treatment cost and risk. Doctors require non-invasive, early warning tools to augment their judgment and screen patients proactively.

### The Solution: High-Recall Risk Prediction

This project develops a Clinical Decision Support System (CDSS) MVP using Random Forest Classification to predict a patient's risk of Type 2 Diabetes based on routine non-invasive clinical features (BMI, Glucose, Age, etc.). The design prioritizes patient safety over operational efficiency.

## II. Methodology and Technical Execution

### Data Strategy and Cleaning

The Pima Indians Diabetes dataset was used. A critical initial step was data preparation: impossible zero values in features like Glucose, BMI, and Insulin were identified as missing data and imputed using the median—a robust technique used to prevent skewing the distribution with outliers.

### Modeling Pipeline

A standard Train (70%) and Test (30%) split was implemented to evaluate performance on unseen data.

Training: The Random Forest model was trained on the training set.

Evaluation: The model's performance metrics were generated solely on the unseen Test Set.

## III. Key Results and Ethical Trade-Off

The final evaluation confirmed the strategic design choice:

### Recall (Sensitivity)

Result : Approximately 89%

Interpretation : The model successfully identifies almost 9 out of 10 actual high-risk patients (minimizing dangerous False Negatives).

### Precision

Result : Approximately 53%

Interpretation : The model is highly cautious, accepting more False Positives (unnecessary follow-ups) to ensure high safety.

### Accuracy

Result : Approximately 68%

Interpretation : Overall score is secondary to Recall in diagnostic systems.


### Feature Importance

The model's logic is transparent and clinically sound, with Glucose ($\mathbf{31\%}$), Age ($\mathbf{16\%}$), and BMI ($\mathbf{15\%}$) being identified as the primary drivers of risk. This validates the model's reliability for use as a clinical aid.


## IV. Conclusion

This project demonstrates the ability to build and ethically deploy Supervised Learning systems for high-stakes health applications. By optimizing for Recall, the CDSS MVP acts as an invaluable triage tool, reducing the clinical burden and enabling the early intervention necessary for better patient outcomes.
