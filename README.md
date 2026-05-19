                               Credit Card Customer Churn Prediction

📌 Project Overview
This project predicts whether a credit card customer is likely to churn (exit) using an Artificial Neural Network (ANN).
The model was trained on customer data and deployed with Streamlit for interactive use via a local web app.

📊 Dataset
The dataset contains the following columns:

RowNumber – Row index

CustomerId – Unique customer identifier

Surname – Customer surname

CreditScore – Credit score of the customer

Geography – Country (France, Germany, Spain, etc.)

Gender – Male/Female

Age – Customer age

Tenure – Number of years with the bank

Balance – Account balance

NumOfProducts – Number of bank products used

HasCrCard – Whether the customer has a credit card (1/0)

IsActiveMember – Whether the customer is active (1/0)

EstimatedSalary – Estimated salary

Exited – Target variable (1 = churned, 0 = retained)

⚙️ Preprocessing
Label Encoding: Gender column encoded using LabelEncoder → saved as le_gender.pkl.

One-Hot Encoding: Geography column encoded using OneHotEncoder → saved as ohe.pkl.

Feature Scaling: StandardScaler applied to numerical features → saved as scaler.pkl.

Encoders and scaler are saved as .pkl files for consistent preprocessing during inference.

🧠 Model
Built with TensorFlow/Keras.

Architecture:

Dense layer (64 units, ReLU)

Dense layer (32 units, ReLU)

Dense layer (1 unit, Sigmoid)

Loss: Binary Crossentropy

Optimizer: Adam

Metrics: Accuracy

The trained model is saved as model.h5.

🚀 Streamlit App
The app (app.py) allows users to input customer details and get churn predictions.

Run locally:

    streamlit run app.py
    
This will start a local server (default: http://localhost:8501) where you can interact with the model.

📈 Output
Displays Churn Probability (0–1).

If probability > 0.5 → “The customer is likely to churn.”

Else → “The customer is not likely to churn.”

<img width="1207" height="720" alt="image" src="https://github.com/user-attachments/assets/ad044f9f-901f-4e85-86c1-9e7b061534c4" />
<img width="731" height="519" alt="image" src="https://github.com/user-attachments/assets/5c7bc4a4-2b7c-43b9-a562-96ae6a5883ce" />

📂 Project Structure
Code
├── app.py                # Streamlit app
├── model.h5              # Trained ANN model
├── le_gender.pkl         # LabelEncoder for Gender
├── ohe.pkl               # OneHotEncoder for Geography
├── scaler.pkl            # StandardScaler for features
├── data.csv              # Source dataset
└── README.md             # Project documentation

✅ How to Use

Clone the repo and install dependencies:

Run in terminal : 
    pip install -r requirements.txt
Run the Streamlit app:
    streamlit run app.py

Enter customer details in the UI.

View churn probability and prediction result.
