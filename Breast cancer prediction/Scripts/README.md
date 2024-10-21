# Scripts Folder
This folder contains Python utility scripts used for data analysis and visualization in conjunction with the **Exploratory Data Analysis** notebook. These scripts help in performing various plotting, data summarization, and missing value detection tasks.

## File Structure
- **plottings.py**: Contains functions for univariate and bivariate analysis visualizations.
- **utils.py**: Contains utility functions for summarizing DataFrame columns and handling missing values.

## plottings.py

This script provides plotting functions using `seaborn` and `matplotlib` for visual data analysis. It also includes logging functionality to record successful operations and errors.

### Functions:
1. **plot_univariate_analysis(df, columns)**  
    - Plots the distribution of individual columns in the DataFrame.
    - Categorical columns are visualized using count plots, while numerical columns use histograms with Kernel Density Estimates (KDE).
    - Logs information about successfully generated plots or errors if plotting fails.

    Example:
    ```python
    plot_univariate_analysis(df, df.columns)
    ```

2. **plot_bivariate_analysis(df, columns)**  
    - Plots pairwise relationships between columns in the DataFrame.
    - For categorical columns, a count plot is used; for numerical columns, a scatter plot is used.
    - Logs successful plots or errors encountered during execution.

    Example:
    ```python
    plot_bivariate_analysis(df, df.columns)
    ```

### Logging:
Log files are saved in the `../logs/` folder:
- `info.log`: Stores logs for successful operations.
- `error.log`: Stores logs for any errors encountered during execution.

## utils.py

This script provides utility functions for handling missing values, generating summary statistics, and logging these operations. It is designed to simplify data exploration and cleaning tasks.

### Functions:
1. **missing_values_table(df)**  
    - Identifies missing values in the DataFrame and calculates the percentage of missing values for each column.
    - Logs the number of columns with missing values and generates a table summarizing missing data.

    Example:
    ```python
    missing_values_table(df)
    ```

2. **column_summary(df)**  
    - Generates a summary for each column in the DataFrame, including data type, the number of missing and non-missing values, and the distinct values.
    - For columns with fewer than 10 distinct values, it shows the count of each distinct value. For columns with more than 10 distinct values, it shows the top 10 most frequent values.
    - Logs information about the column summary generation process.

    Example:
    ```python
    column_summary(df)
    ```

### Logging:
Log files are saved in the `../logs/` folder:
- `info.log`: Logs successful function calls and operations.
- `error.log`: Logs errors encountered during function execution.

## Dependencies

These scripts rely on the following libraries:
- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations.
- `seaborn` and `matplotlib`: For data visualization.
- `logging`: For logging successful operations and errors.

You can install the dependencies via pip:
```bash
pip install pandas numpy seaborn matplotlib
```

## How to Use

1. Ensure the scripts folder is located as expected relative to the project structure.
2. Import the necessary functions in your Jupyter notebooks or Python scripts by adding the following line to your code:
    ```python
    import sys, os
    sys.path.append(os.path.abspath(os.path.join(os.getcwd(), '../scripts')))
    from plottings import plot_univariate_analysis, plot_bivariate_analysis
    from utils import missing_values_table, column_summary
    ```
3. Use the functions provided by the scripts to streamline your data exploration and visualization tasks.

## Logs

The scripts are configured to log important events. Logs can be found in the `../logs/` folder:
- `info.log`: Records successful operations.
- `error.log`: Records any errors encountered during script execution.