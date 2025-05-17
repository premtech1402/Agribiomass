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

## 📂 Dataset Description

The dataset used in this project — **`agribiomass.csv`** — contains information on various types of agricultural waste and their corresponding biomass yields. It was compiled to support the prediction and classification of biomass potential based on waste attributes.

### 📄 Columns in the Dataset:

| Column Name              | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| `Crop Type`              | The name of the crop that generated the waste (e.g., Wheat, Rice, Maize).   |
| `Waste Type`             | The specific type of agricultural waste (e.g., Straw, Husk, Stalks).        |
| `Waste Amount (kg)`      | Quantity of waste generated in kilograms.                                   |
| `Biomass Yield (kg)`     | Actual amount of usable biomass obtained from the given waste.              |
| `Processing Method`      | The recommended method for processing the given crop-waste combination.     |
| `Resulting Product`      | The end product obtained after processing the waste (e.g., Briquettes, Compost). |

---

### 🧪 Sample Data (Example Rows):

| Crop Type | Waste Type | Waste Amount (kg) | Biomass Yield (kg) | Processing Method | Resulting Product     |
|-----------|------------|-------------------|---------------------|-------------------|------------------------|
| Rice      | Husk       | 50                | 40.5                | Briquetting       | Biomass Briquettes     |
| Wheat     | Straw      | 60                | 45.2                | Composting        | Organic Compost        |
| Sugarcane | Bagasse    | 100               | 88.0                | Pelletization     | Biomass Pellets        |

---

### ⚙️ Preprocessing Applied to Dataset

- **Label Encoding**: `Crop Type` and `Waste Type` are encoded to numerical values using `LabelEncoder` for model training.
- **Feature Selection**:
  - **Inputs**: Crop Type (encoded), Waste Type (encoded), Waste Amount (kg)
  - **Target**: Biomass Yield (kg)

---

### 🔍 Purpose of Dataset

This dataset enables the training of a machine learning model to:
- Predict how much biomass can be generated from specific crop waste.
- Recommend the most suitable processing technique and end product for practical use in rural/agro-industrial settings.


## 📁 Project Structure

agribiomass_project/
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
