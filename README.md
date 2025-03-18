# Machine Learning-Based Process Scale-Up of Stirred Reactor From 1L to 7000L
![image](https://github.com/user-attachments/assets/7dfcce4a-194a-452f-a37c-f3c4c7f5a445)

## 📌 Project Overview
This project applies **machine learning (ML) techniques** to predict **turbulence characteristics** in a stirred reactor, facilitating **scaling from lab-scale (1L) to industrial-scale (7000L) reactors**.

By leveraging **Computational Fluid Dynamics (CFD) simulation data**, the model aims to predict key **fluid dynamics properties** such as:
- **Turbulent dissipation rate (ε)**
- **Turbulent kinetic energy (k)**
- **Strain rate**
- **Velocity magnitude**

This approach eliminates the need for expensive and time-consuming CFD simulations when scaling up stirred reactors.

---

## 🚀 Features
** Predict turbulence parameters from **impeller RPM**
** Scale-up insights for reactors of different sizes
** **Random Forest Regressor** for accurate predictions
** Data visualization for model evaluation
** Saves time & computational resources by reducing CFD simulations

---

## 📊 Dataset
The dataset contains fluid dynamics parameters for different **impeller speeds (RPM)**:
| **Column** | **Description** |
|------------|----------------|
| `rpm` | Impeller speed (Revolutions per minute) |
| `epsilon_p50` | Median turbulent dissipation rate |
| `k_p50` | Median turbulent kinetic energy |
| `strainRate_p50` | Median strain rate |
| `Umag_p50` | Median velocity magnitude |

📌 **Source**: Generated from CFD simulations

---

## 🔬 Methodology
1. **Data Preprocessing**
   - Load CSV dataset
   - Handle missing values
   - Scale/normalize features
2. **Feature Engineering**
   - Define `rpm` as the main input feature
   - Extract turbulence properties as target variables
   - Apply transformations (e.g., `log(epsilon_p50)`, `rpm^2`)
3. **Train-Test Split**
   - 70% training, 30% testing
   - Ensure reproducibility with `random_state=42`
4. **ML Model Training**
   - Implement **Random Forest Regressor**
   - Train separate models for each turbulence property
5. **Evaluation Metrics**
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)
   - Root Mean Squared Error (RMSE)
   - Explained Variance Score
6. **Visualization**
   - Scatter plots for true vs predicted values
   - Performance comparison using evaluation metrics

---

## 📌 Results & Insights
- The trained model accurately predicts turbulence properties across different RPM values.
- The **Random Forest Regressor** performs well with low MAE/MSE values.
- Visualization confirms a strong correlation between true and predicted values.

📌 **Key Benefit**: Reduces the dependency on CFD simulations, making scale-up more efficient.

---

## 🔧 Installation & Usage
### 1️⃣ Clone Repository
```bash
git clone https://github.com/yourusername/stirred-reactor-ml.git
cd stirred-reactor-ml
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Run the Model
```python
python train_model.py
```

### 4️⃣ Visualize Predictions
```python
python plot_results.py
```

---

## 📜 License
This project is licensed under the **MIT License**.

---

## 🤝 Contributions
Feel free to open issues or submit pull requests to improve this project.

🔗 **Author**: [NovaLabs](https://www.kaggle.com/novalabs)

💡 **Inspired by CFD-driven reactor design & scale-up**.

