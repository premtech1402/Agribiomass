# 🌾 Agribiomass Yield Predictor

A Machine Learning-powered application that predicts biomass yield from agricultural waste inputs and recommends the most suitable processing method along with the resulting product.

---

## 📌 Overview

The Agribiomass Yield Predictor aims to transform agricultural waste into a valuable resource. By inputting the crop type, waste type, and waste amount, the system:
- Predicts the biomass yield (in kg)
- Recommends the optimal processing method (e.g., composting, briquetting)
- Displays the resulting product (e.g., organic compost, biomass briquettes)

This tool is built using **Python**, **Scikit-learn**, and **Gradio** for an intuitive user interface.

---

## 🔍 Features

- 🌱 Label Encoding for categorical inputs
- 🧠 Random Forest Regressor model for high-accuracy predictions
- 📊 Model evaluation with MAE, MSE, and R² Score
- 📦 Joblib serialization for model and encoder persistence
- 🖥️ Gradio web interface for easy access and usage
- 📈 Actual vs Predicted visualization to assess model performance

---

## 🧰 Technologies Used

- Python
- Pandas
- NumPy (implicitly via Scikit-learn)
- Scikit-learn
- Joblib
- Matplotlib
- Gradio

---

## 📁 Project Structure

agribiomass_project/
│
├── agribiomass.csv                  # Dataset with crop, waste, and biomass info
├── model_training.py               # Python script to train and save the model
├── predict_biomass.py              # Contains prediction logic with encoders
├── interface.py                    # Gradio-based user interface
├── label_encoders.pkl              # Encoded label mappings
├── agribiomass_model.pkl           # Trained RandomForest model
├── processing_methods.pkl          # Mapping of processing methods
├── method_product_info.pkl         # Mapping of methods & products
├── plot.png                        # Visualization: Actual vs Predicted
└── README.md                       # Project documentation

---

## 🚀 Getting Started

### 1. Clone the Repository

git clone https://github.com/yourusername/agribiomass-predictor.git
cd agribiomass-predictor

### 2. Install Dependencies

pip install -r requirements.txt

If you don't have a requirements.txt, install manually:

pip install pandas scikit-learn joblib matplotlib gradio

### 3. Run the Application

python interface.py

A browser window will launch with the input form.

---

## 📊 Sample Output

🌾 Predicted Biomass Amount: 112.45 kg  
🔧 Recommended Processing Method: Composting  
📦 Resulting Product: Organic Compost

---

## 📈 Model Performance

- Mean Absolute Error (MAE): 15.18 kg
- Mean Squared Error (MSE): 462.92
- R² Score: 0.95

> The model exhibits excellent performance, indicating high reliability for practical use.

---

## 📝 Future Improvements

- Add dropdown inputs instead of free text for better UX.
- Integrate real-time agricultural databases.
- Enable cloud deployment using Streamlit or FastAPI.
- Add support for seasonal and regional features.

---

## 👨‍💻 Author

**Atmakuri Leela Naga Premchand**  
Minor Project 2 | Machine Learning & AI |CSE Student.
