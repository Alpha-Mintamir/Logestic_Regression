# Notebook Folder
This folder contains the **Exploratory Data Analysis (EDA)** notebook, which performs detailed exploratory analysis on a dataset, helping to uncover patterns, relationships, and insights in the data. The code is implemented in the `Exploratory Data Analysis.ipynb` file.

## File Structure
- **Exploratory Data Analysis.ipynb**: This Jupyter notebook contains the steps for loading the data, cleaning it, and performing various univariate, bivariate, and correlation analyses.

## Steps Involved

1. **Importing Libraries**  
    - Essential libraries like `pandas`, `numpy`, `seaborn`, and `matplotlib` are imported for data manipulation and visualization.
    - Custom utility functions for plotting and data summarization are imported from the `../scripts` folder.

2. **Loading Data**  
    The dataset is loaded from `../Data/data.csv` using `pandas`. Basic data exploration is performed using methods like `head()`, `tail()`, and `describe()`.

3. **Checking for Missing Values**  
    A custom function `missing_values_table()` is used to check for missing values, and the column `"Unnamed: 32"` is dropped from the DataFrame as part of data cleaning.

4. **Univariate Analysis**  
    The function `plot_univariate_analysis()` is used to plot the distribution of individual columns to understand their spread and distribution.

5. **Bivariate Analysis**  
    For bivariate analysis, the function `plot_bivariate_analysis()` is used to visualize relationships between pairs of features in the dataset, excluding the `id` column.

6. **Correlation Matrix**  
    The correlation matrix is calculated using the numeric columns of the DataFrame to identify the strength of relationships between features. A heatmap is plotted using `seaborn` to visualize the correlations.

7. **Saving Cleaned Data**  
    The cleaned and processed data is saved as `data_cleaned.csv` in the `../Data/` directory for further analysis or model training.

## Dependencies
The following libraries are used in the notebook:
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `seaborn` and `matplotlib`: For visualizations.
- Custom scripts (`plottings.py` and `utils.py`) located in the `../scripts` folder are imported to assist with plotting and data summarization.

You can install the dependencies via pip:
```bash
pip install pandas numpy seaborn matplotlib
```

## How to Use
1. Clone the repository and navigate to the Notebook folder.
2. Ensure the data file `data.csv` is placed in the `../Data/` folder.
3. Run the `Exploratory Data Analysis.ipynb` notebook using Jupyter Notebook or Jupyter Lab.
4. The cleaned data will be saved as `data_cleaned.csv` in the `../Data/` folder after the analysis.

## Output
- **Cleaned Dataset**: The processed and cleaned data is saved as `data_cleaned.csv`.
- **Visualizations**: Various plots and a correlation heatmap are generated to provide insights into the data distribution and relationships between features.

This notebook helps in preparing the data for further steps such as feature selection, model training, or additional statistical analysis.
