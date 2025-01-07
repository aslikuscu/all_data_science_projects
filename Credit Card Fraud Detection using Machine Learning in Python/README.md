

# **Credit Card Fraud Detection using Logistic Regression**

## 🚀 **Overview**

In this project, we focus on building a **fraud detection system** using **Logistic Regression** to identify fraudulent transactions from a credit card transaction dataset. The dataset is highly imbalanced, with normal transactions greatly outnumbering fraudulent ones. Through preprocessing techniques like under-sampling and the use of machine learning algorithms, we aim to achieve a high-accuracy classification model.

---

## 📊 **Dataset**

This dataset contains information about **credit card transactions**. The dataset includes:

- **Time**: Time elapsed since the first transaction in seconds
- **V1 to V28**: 28 anonymized features resulting from PCA transformations
- **Amount**: The transaction amount
- **Class**: Target variable indicating whether the transaction is fraudulent (`1`) or legitimate (`0`)

The dataset is highly imbalanced, with **284,315 normal transactions** and only **492 fraudulent transactions**.

---

## 🧠 **Modeling Process**

### 1. **Data Preprocessing**
   - **Handling Missing Values**: The dataset contains no missing values.
   - **Data Balancing**: Since the dataset is highly imbalanced, we used an **under-sampling technique** to balance the distribution of fraudulent and normal transactions.
   - **Feature Engineering**: The original features were used for training the model, including anonymized variables and the transaction amount.

### 2. **Model Selection**
   - The model chosen for this task is **Logistic Regression** due to its efficiency and interpretability in binary classification tasks.

### 3. **Model Evaluation**
   - The dataset was split into training and testing sets using an **80-20 split**.
   - The model’s performance was evaluated using **accuracy score** on both the training and test datasets.

---

## 💡 **Results**

- **Training Data Accuracy**: **94.16%**
- **Test Data Accuracy**: **93.91%**

These high accuracy scores indicate that the model is performing well in classifying both normal and fraudulent transactions.

---

## ⚙️ **Technologies Used**

- **Programming Language**: Python
- **Libraries**:
  - `pandas`: Data manipulation and analysis
  - `numpy`: Mathematical operations
  - `sklearn`: Machine learning models and evaluation metrics
  - `matplotlib` (Optional for visualization)

---

## 👩‍💻 **How to Run the Project**

### 1. Clone the repository

```bash
git clone <repository-link>
```

### 2. Install required dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the Python script

```bash
python credit_card_fraud_detection.py
```

---

## 🎯 **Future Improvements**

- **Model Optimization**: Use hyperparameter tuning techniques (like GridSearchCV) to improve the model's performance.
- **Advanced Models**: Try using more advanced models like Random Forests or XGBoost to compare results and increase accuracy.
- **Anomaly Detection**: Implement an unsupervised anomaly detection method for a more robust fraud detection system.

---

## 📬 **Contact**

For any questions or feedback, feel free to reach out:

- **Email**: [aslii.ksc@gmail.com]
- **LinkedIn**: [[your LinkedIn profile](https://www.linkedin.com/in/asli-kuscu/)]

---

