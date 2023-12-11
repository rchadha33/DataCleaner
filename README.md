## Advancing Data Cleaning Methods for Automated Visualization Tools: A Focus on Speed, Depth, and Engagement

### DataCleaner
A Python Class for Data Cleaning &amp; Interestingness based Pruning for Always On Visualization Tools (Such as Python's Lux)

#### Overview
The **'DataCleaner'** class is a Python tool designed to streamline the data cleaning process, particularly for use with automatic data visualization and recommendation systems like Lux. It addresses the gap in current state-of-the-art data cleaning methods, making them more suitable for real-world datasets such as the US Census and EEG data.

Below is the Structure of the DataCleaner Class:
```python
class DataCleaner:
   def __init__(self, df):
       # Initialize the class with a DataFrame and detect issues
       self._df = df
       self.issues = self._detect_issues()
       self._print_issues()
       self.methods = [
           "Median + Most Frequent","KNN Imputation",
           "Outlier Removal with Median Imputation",
           "Outlier Removal Ignoring Missing",
           "Outlier Removal",
       ]
   @property
   def df(self):
       # Property to get the DataFrame
       return self._df

   @df.setter
   def df(self, new_df):
       # Setter to update the DataFrame and re-detect issues
       self._df = new_df
       self.issues = self._detect_issues()
       self._print_issues()

   def _print_issues(self):
       # Print detected data issues

   def _detect_issues(self):
       # Detect various data issues like missing values, duplicates, etc.

   def apply_cleaning_method(self, df, method):
       # Apply specified data cleaning methods to the DataFrame

   def _calculate_interestingness(self, df, col1, col2):
       # Calculate the interestingness score for a pair of columns

   def visualize_effect_of_methods(self):
       # Visualize the effect of cleaning methods, pruning less interesting visualizations

   def visualize_all_methods(self):
       # Visualize the effect of all cleaning methods, showing interestingness scores
```

#### Purpose
The primary goal of the **'DataCleaner'** class is to enhance the user's experience in data exploration and visualization. By integrating data cleaning with automatic visualization tools, it provides a user-centric, intuitive, and efficient approach to data cleaning, ensuring that the final visualizations are accurate, insightful, and tailored to the dataset's unique characteristics.

#### Key Features
- Integration with Lux for enhanced data visualization.
- A range of data cleaning methods including outlier handling and missing value imputation.
- Calculation of 'interestingness' scores to guide users towards more meaningful visualizations.
- User-friendly interface to facilitate ease of use, especially for users new to data cleaning or Lux.

#### Installation

To use the DataCleaner class, you need to have Python installed on your system along with the necessary libraries. Here's how you can install it:

- ```git clone https://github.com/rchadha33/DataCleaner.git```
- ```cd DataCleaner```
- Open the CleaningClassMDS.ipynb notebook:
    - If you have Jupyter Notebook or JupyterLab installed, you can open it directly in your browser.
    - Alternatively, you can use an IDE that supports Jupyter notebooks, such as Visual Studio Code or PyCharm.

The **'CleaningClassMDS.ipynb'** notebook contains the DataCleaner class implementation along with example usage, allowing you to understand how to apply the class to your data cleaning tasks.

#### Usage
Here's a simple example of how to use the **'DataCleaner'** class:

```python
import pandas as pd
from data_cleaner import DataCleaner

# Load your dataset
df = pd.read_csv('path_to_your_dataset.csv')

# Create an instance of the DataCleaner class
cleaner = DataCleaner(df)

# Apply a cleaning method
cleaned_df = cleaner.apply_cleaning_method(df, 'Median + Most Frequent')

# Visualize the effect of cleaning methods pruned by Interestingness
cleaner.visualize_effect_of_methods()

# Visualize the effect of all cleaning methods sorted by interestingness
cleaner.visualize_all_methods()
```

Below is an Example Usage on the *US CENSUS* Dataset. 
- Step 1: Data cleaning issue identification on US Census Data
![Step 1](images/Step1.jpg)

- Step 2: Cleaning Method Visualizations after pruning based on Interestingness
![Step 2](images/Step2.jpg)

- Step 3 (Optional): Visualizing all Cleaning Method sorted based on Interestingness (descending)
![Step 3](images/Step3.jpg)

#### Contributions
*Rachit Chadha* (MS Computer Science) & *Brian Sang* (PhD Electrical and Computer Engineering) @ Georgia Institute of Technology.





