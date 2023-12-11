# Advancing Data Cleaning Methods for Automated Visualization Tools: A Focus on Speed, Depth, and Engagement

## DataCleaner
A Python Class for Data Cleaning &amp; Interestingness based Pruning for Always On Visualization Tools (Such as Python's Lux)

### Overview
The **'DataCleaner'** class is a Python tool designed to streamline the data cleaning process, particularly for use with automatic data visualization and recommendation systems like Lux. It addresses the gap in current state-of-the-art data cleaning methods, making them more suitable for real-world datasets such as the US Census and EEG data.

### Purpose
The primary goal of the **'DataCleaner'** class is to enhance the user's experience in data exploration and visualization. By integrating data cleaning with automatic visualization tools, it provides a user-centric, intuitive, and efficient approach to data cleaning, ensuring that the final visualizations are accurate, insightful, and tailored to the dataset's unique characteristics.

### Key Features
- Integration with Lux for enhanced data visualization.
- A range of data cleaning methods including outlier handling and missing value imputation.
- Calculation of 'interestingness' scores to guide users towards more meaningful visualizations.
- User-friendly interface to facilitate ease of use, especially for users new to data cleaning or Lux.

### Installation

To use the DataCleaner class, you need to have Python installed on your system along with the necessary libraries. Here's how you can install it:

- '''git clone https://github.com/rchadha33/DataCleaner.git'''
- '''cd DataCleaner'''
- Open the CleaningClassMDS.ipynb notebook:
    - If you have Jupyter Notebook or JupyterLab installed, you can open it directly in your browser.
    - Alternatively, you can use an IDE that supports Jupyter notebooks, such as Visual Studio Code or PyCharm.

The **'CleaningClassMDS.ipynb'** notebook contains the DataCleaner class implementation along with example usage, allowing you to understand how to apply the class to your data cleaning tasks.

### Usage
Here's a simple example of how to use the **'DataCleaner'** class:
'''python
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
data_cleaner.visualize_all_methods()
'''

### Contributions
Rachit Chadha (MS Computer Science) & Brian Sang (PhD Electrical and Computer Engineering) @ Georgia Institute of Technology.





