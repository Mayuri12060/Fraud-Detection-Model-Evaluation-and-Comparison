# Fraud Detection Model Evaluation and Comparison

## Objective
The primary aim of this project is to develop a robust fraud detection model utilizing a dataset containing transactional information. The goal is to predict whether a transaction is fraudulent or not based on the given features.

## Dataset Description
The dataset consists of **555,719 rows and 13 columns**, initially including the following features:
- Transaction category
- Transaction amount
- Gender
- City, state, and zip code
- Latitude and longitude
- City population
- Occupation
- Merchant latitude and longitude
- Binary label indicating whether the transaction is fraudulent or not

### Preprocessing
To streamline the dataset for model training, the following columns were dropped:
- `city`
- `state`
- `zip`
- `latitude`
- `longitude`
- `city_pop`
- `job`

This resulted in a cleaner dataset focusing on the most relevant features.

## Model Development and Evaluation

### Random Forest Model
A **Random Forest** model was initially employed, achieving an impressive accuracy of **99.76%**. While the model demonstrated perfect precision for non-fraudulent transactions, there was room for improvement in detecting fraudulent ones.

### Model Comparison
To evaluate alternative approaches, the following models were implemented:
- **Gradient Boosting**
- **Logistic Regression**
- **XGBoost**

#### Key Observations:
- **Logistic Regression** achieved a competitive accuracy of **99.76%**, matching the Random Forest model.
- Logistic Regression demonstrated significantly faster execution times compared to Random Forest and Gradient Boosting models.

### Performance Metrics
For each model, the following performance metrics were computed:
- **Precision**
- **Recall**
- **F1-score**
- **Support**

### Visualizations
To aid in understanding model performance, the following visual aids were generated:
- Confusion matrix
- Precision-recall curve
- ROC curve
- Feature importance plots

## Conclusion
This project highlights the importance of exploring multiple models for fraud detection tasks. Key takeaways include:
- While Random Forest exhibited high accuracy, Logistic Regression proved to be both efficient and effective.
- Computational efficiency is as important as accuracy, particularly for deploying fraud detection systems in real-world scenarios.

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/fraud-detection
   ```
2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebook or script:
   ```bash
   python fraud_detection.py
   ```

## Results
The detailed results, including performance metrics and visualizations, are available in the output folder.

## Acknowledgements
Special thanks to the contributors and data providers for making this project possible.
