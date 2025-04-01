
![image1-23](https://github.com/user-attachments/assets/5919965a-4ecc-4e74-976a-73a0a980a667)


# Fraud Detection Using Machine Learning

## Overview
This project focuses on detecting fraudulent transactions using machine learning techniques. Given the highly imbalanced nature of fraud detection problems, various preprocessing techniques and classification models were explored to improve performance.

## Dataset
The dataset consists of transaction records with the following key features:
- `transaction_id`: Unique identifier for each transaction.
- `amount`: Transaction amount.
- `customer_id`: Unique customer identifier.
- `transaction_type`: Type of transaction (e.g., transfer, cash-out, etc.).
- `time_step`: Time elapsed since the first transaction in the dataset.
- `is_fraud`: Target variable (1 for fraudulent transactions, 0 for non-fraudulent transactions).

## Data Preprocessing
To improve model performance, the following preprocessing steps were applied:
- **Handling Missing Values**: Checked and imputed where necessary.
- **Feature Engineering**: Created new features such as transaction frequency per customer.
- **Encoding Categorical Variables**: Used label encoding for categorical features.
- **Scaling**: Applied normalization/standardization where needed.
- **Class Imbalance Handling**: Tried both SMOTE (Synthetic Minority Over-sampling) and undersampling techniques.

## Models Trained
The following machine learning models were trained and evaluated:
1. **Logistic Regression** - Baseline model, struggled due to class imbalance.
2. **Decision Tree Classifier** - Captured patterns but prone to overfitting.
3. **Random Forest Classifier** - Improved generalization by reducing overfitting.
4. **XGBoost Classifier** - Achieved the best recall and F1-score.

## Evaluation Metrics
Given the imbalanced nature of the dataset, the models were evaluated using:
- **Precision**: Proportion of correctly predicted frauds out of all predicted frauds.
- **Recall (Sensitivity)**: Ability to correctly identify actual fraud cases.
- **F1-Score**: Balance between precision and recall.
- **ROC-AUC Score**: Measures overall model performance.

## Results
| Model                 | Precision | Recall | F1-Score | AUC-ROC |
|----------------------|----------|--------|----------|---------|
| Logistic Regression  | Low      | Very Low  | Low      | Low     |
| Decision Tree       | Moderate | Good   | Moderate | Good    |
| Random Forest      | High     | Better | High     | Very High |
| XGBoost             | Best     | Best   | Best     | Best    |

## Future Improvements
- **Further Hyperparameter Tuning**: Fine-tune models using GridSearchCV.
- **Anomaly Detection Methods**: Explore unsupervised techniques like Isolation Forest.
- **Deploy the Model**: Create an API for real-time fraud detection.

## Installation & Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/fraud-detection.git
   cd fraud-detection
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the model training script:
   ```sh
   python train_model.py
   ```
4. Make predictions:
   ```sh
   python predict.py --input sample_transaction.csv
   ```

## Contributing
Feel free to fork this repository and contribute improvements! Open a pull request with your changes.


