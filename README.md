🩺 SugarSight – Diabetes Risk Assessment Tool

SugarSight is an interactive machine-learning–powered Streamlit application designed to estimate diabetes risk based on patient health metrics. The app uses a trained SVM model along with a preprocessing scaler to provide predictions, probability insights, and personalized health recommendations.

⭐ Features

🔍 Diabetes risk prediction using an ML classifier

📊 Probability breakdown (Diabetic vs. Non-Diabetic)

🎛️ Interactive patient input controls

🚦 Gauge chart visualization of risk level

⚠️ Risk factor analysis (BMI, glucose, blood pressure, etc.)

💡 Personalized recommendations

🛡️ Medical disclaimer included

📁 Project Structure
.
├── app.py                     # Streamlit application
├── diabetes.csv              # Dataset used for training
├── diabetes_model.pkl        # Trained SVM model
├── diabetes_model_rf.sav     # Random Forest model (unused)
├── scaler_svm.pkl            # StandardScaler used during training
├── prediction.ipynb          # Notebook for training/testing models

🚀 How to Run the Application
1️⃣ Install Dependencies

Make sure you have Python 3.8+ installed.

Run:

pip install -r requirements.txt


If you do not have a requirements file, use:

pip install streamlit pandas numpy joblib plotly scikit-learn

2️⃣ Ensure Model Files Are Present

The app relies on:

diabetes_model.pkl

scaler_svm.pkl

If missing, train and generate them using:

python diabetes_prediction.py


(or run the included prediction.ipynb to regenerate the model files.)

3️⃣ Launch the Web App
streamlit run app.py


Then visit:

http://localhost:8501

🧠 How It Works
Model

The app loads a trained Support Vector Machine (SVM) model.

Inputs are standardized using a saved StandardScaler.

It produces:

Binary prediction (Diabetic / Non-Diabetic)

Probability estimates (if supported by model)

Risk categorization (Low, Moderate, High)

Input Features
Feature	Description
Pregnancies	Number of pregnancies
Glucose	Plasma glucose concentration
Blood Pressure	Diastolic blood pressure
Skin Thickness	Triceps skinfold thickness
Insulin	Insulin concentration
BMI	Body Mass Index
Diabetes Pedigree Function	Genetic Diabetes risk indicator
Age	Age of patient
📊 Visualizations

SugarSight uses Plotly to generate a gauge meter showing diabetes probability:

🟢 0–30% → Low Risk

🟡 30–70% → Moderate Risk

🔴 70–100% → High Risk

🏥 Medical Disclaimer

This tool is not a substitute for professional diagnosis.
Always consult a certified healthcare provider for medical advice or treatment.

🙌 Contributors

Your Name — Krish Malhotra

Machine Learning Model based on the PIMA Diabetes Dataset

📜 License

This project is open-source. Use and modify as needed.
