# Disease Prediction Model
This project aims to predict the likelihood of a disease based on medical data, including symptoms and patient history. The model uses classification algorithms to analyze the relationship between various features such as symptoms and precautions to classify diseases.

### Features:
- Disease symptoms dataset
- Disease precautions dataset
- RandomForestClassifier model

## Files:
- `disease_prediction_model.ipynb`: Google Colab notebook containing the disease prediction model implementation.
- `Disease precaution.csv`: Data about disease precautions.
- `DiseaseAndSymptoms.csv`: Data about disease symptoms.
- `README.md`: Documentation for the project.

## Dependencies:
- Python 3.x
- `pandas`: For data manipulation
- `sklearn`: For machine learning algorithms and metrics
- `imblearn`: For handling class imbalance using SMOTE

## Installation and Setup:
1. Open the `disease_prediction_model.ipynb` notebook in [Google Colab](https://colab.research.google.com/).
2. To upload the dataset files, either drag and drop the files into the Colab environment 
3. Run the cells in the notebook to train the model and evaluate its performance.

## How the Model Works:
1. **Data Preprocessing**: The datasets are loaded and checked for missing values. Any missing values are filled with "Unknown."
2. **Data Merging**: The two datasets (`Disease precaution.csv` and `DiseaseAndSymptoms.csv`) are merged on the 'Disease' column.
3. **Feature Encoding**: Categorical variables are encoded using one-hot encoding.
4. **Train-Test Split**: The data is split into training and test sets using a stratified split.
5. **Class Imbalance Handling**: SMOTE (Synthetic Minority Over-sampling Technique) is used to handle class imbalance in the training set.
6. **Model Training**: A RandomForestClassifier is trained on the processed data.
7. **Model Evaluation**: Accuracy, precision, recall, F1 score, and a classification report are calculated and displayed.
8. **Cross-validation**: The model is cross-validated using 5-fold cross-validation to ensure stable performance.

## Evaluation Metrics:
- **Accuracy**: Percentage of correctly predicted diseases.
- **Precision**: Ratio of correctly predicted positive observations to total predicted positives.
- **Recall**: Ratio of correctly predicted positive observations to all observations in actual class.
- **F1 Score**: Weighted average of precision and recall.
- **Classification Report**: Detailed metrics for each class.

## Example Output:

Accuracy: 0.95
Precision: 0.94
Recall: 0.93
F1 Score: 0.93

Classification Report:
              precision    recall  f1-score   support

      Disease1       0.92      0.95      0.94       100
      Disease2       0.96      0.92      0.94        80
      ...


## Contributing:
Feel free to fork the repository, submit issues, or contribute by making pull requests.

## License:
This project is open-source and available under the MIT License.
