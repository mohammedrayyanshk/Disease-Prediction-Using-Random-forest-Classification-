**# Disease-Prediction-Using-Random-forest-Classification-**
This is a Python-based machine learning project that predicts possible diseases based on a list of symptoms provided by the user. The system uses a Random Forest Classifier model trained on a labeled dataset and returns the top 3 predicted diseases along with their descriptions and suggested precautions.
Technologies Used
Python

Pandas

Scikit-learn (RandomForestClassifier, LabelEncoder, train_test_split)

CSV-based datasets

**Dataset Files**
dataset.csv: Contains patient symptoms and their diagnosed disease.

Symptom-severity.csv: Maps each symptom to a numerical weight (severity).

symptom_Description.csv: Provides a short description for each disease.

symptom_precaution.csv: Lists up to 4 precautions for each disease.

Model Training Process
Data Cleaning:

Missing values in dataset.csv are filled with 'None'.

Symptoms are mapped to their respective severity weights using Symptom-severity.csv.

Label Encoding:

Disease names are label-encoded to be used as numeric targets for training.

Model:

A RandomForestClassifier is trained using 80% of the data (train_test_split).

Accuracy is evaluated using the remaining 20% of the data.

🔍 Prediction Logic
The user provides a list of symptoms (up to 17).

Each symptom is converted to a severity weight using the mapping dictionary.

The trained model predicts the disease probabilities.

The top 3 most probable diseases are selected.

For each predicted disease:

A description is fetched from symptom_Description.csv.

Up to 4 suggested precautions are retrieved from symptom_precaution.csv.

Features
Supports prediction based on multiple symptoms (up to 17).

Returns top 3 disease predictions with probability scores.

Provides description and precautions for each disease.

Offline-compatible (no internet/API dependency).

