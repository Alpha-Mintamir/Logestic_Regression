# Model Folder

This folder contains the implementation of a **Logistic Regression** model, used for binary classification, as shown in the `logistic regression model.ipynb` notebook. The model predicts whether a given sample belongs to class **M** (Malignant) or class **B** (Benign) based on various features from a dataset.

## File Structure
- **logistic_regression.ipynb**: This Jupyter notebook contains the complete implementation of a logistic regression model, including data preprocessing, model training, prediction, and performance evaluation.

## Data Used
The data used for training the model is stored in a file named `data_cleaned.csv`, which contains features relevant to cancer diagnosis. The **`diagnosis`** column is the target variable, which is converted into binary labels:
- **1**: Malignant (M)
- **0**: Benign (B)

## Steps Involved

1. **Data Loading**  
   The cleaned dataset (`data_cleaned.csv`) is loaded using `pandas`.

2. **Data Preprocessing**  
   - Dropping unnecessary columns (like the `id` column).
   - Mapping the target variable (`diagnosis`) to binary values (1 for malignant, 0 for benign).
   - Standardizing the feature data using `StandardScaler` for better model performance.

3. **Model Training**  
   - Splitting the data into training and testing sets with a 70-30 ratio using `train_test_split`.
   - Training the logistic regression model with the training data.

4. **Prediction**  
   The trained model is used to predict the classes of the test set.

5. **Evaluation**  
   - A **classification report** is generated showing the precision, recall, F1-score, and accuracy of the model.
   - A **confusion matrix** is plotted using `seaborn` to visually represent the performance of the model.

## Dependencies
This notebook uses the following Python libraries:
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `matplotlib` and `seaborn`: For data visualization.
- `sklearn`: For model training, scaling, and evaluation (Logistic Regression, train-test split, scaling, confusion matrix, etc.).

You can install the dependencies via pip:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

Model Performance
The model is evaluated using several metrics:

Precision
Recall
F1-Score
Accuracy
A confusion matrix is also plotted to give a better visual understanding of how well the model is performing in predicting positive (malignant) and negative (benign) cases.

How to Use
Clone the repository and navigate to the Model folder.
Run the logistic_regression.ipynb notebook using Jupyter Notebook or Jupyter Lab.
Ensure that the data_cleaned.csv file is located in the appropriate directory (../Data/), or update the path in the notebook accordingly.


This is the `README.md` file with proper markdown syntax. You can copy and paste this into your `readme.md` file in the **Model** folder.
