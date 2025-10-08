🛠️ NASA Engine Health ML — Predicting Remaining Useful Life
🌟 Project Overview

This project focuses on predicting the Remaining Useful Life (RUL) of jet engines using machine learning techniques on the NASA C-MAPSS dataset.
By analyzing engine sensor data over time, we estimate how many operational cycles remain before an engine fails. This is a crucial step toward predictive maintenance, which helps reduce unexpected breakdowns, lower costs, and improve safety.

📊 Dataset Information

Source: NASA C-MAPSS Dataset

File Used: test_FD002.txt

Description:
Each row in the dataset represents sensor readings from an aircraft engine at a specific cycle.

engine_id: Unique ID for each engine

cycle: Time step (like engine age)

setting_1 to setting_3: Operational settings

sensor_1 to sensor_21: Sensor measurements collected over time

👉 For each engine, the RUL is calculated by subtracting the current cycle number from its maximum cycle.

🧪 Feature Engineering

To improve model performance, we generated several new features:

Rolling Statistics (5 cycles):

Rolling Mean

Rolling Standard Deviation

Lag Features:

Lag of 1 cycle

Lag of 2 cycles

Feature Scaling:

All features were standardized using StandardScaler to ensure uniform scale for model training.

🤖 Machine Learning Model

We trained and evaluated a Random Forest Regressor, chosen for its robustness and ability to handle non-linear relationships effectively.

📈 Model Performance
Model	MSE	RMSE	R² Score
Random Forest	2935.32	54.18	0.11

(These values are based on the validation dataset for FD002. Update them if you retrain the model.)

🚀 How to Run the Project
1️⃣ Clone the Repository
git clone https://github.com/your-username/nasa-engine-health-ml.git
cd nasa-engine-health-ml

2️⃣ Install Dependencies
pip install -r requirements.txt

3️⃣ Launch the Notebook
jupyter notebook nasa.ipynb


or open it directly in VS Code / JupyterLab.

📁 Project Structure
nasa-engine-health-ml/
│
├── nasa.ipynb              # Main analysis notebook
├── data/                   # Dataset files (place NASA data here)
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
