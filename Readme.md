# Electric Vehicle Data Analysis Project

## Overview
This project involves analyzing a dataset containing information about electric vehicles, including their model, make, electric range, and other attributes. The analysis focuses on exploratory data analysis (EDA), handling missing data, and performing univariate and bivariate analysis to derive insights.

## Dataset
The dataset contains 112,634 rows and 17 columns, representing various attributes of electric vehicles such as:
- **VIN (1-10)**: A truncated version of the Vehicle Identification Number
- **County, City, State, Postal Code**: Location details of the vehicle
- **Model Year, Make, Model**: Vehicle details
- **Electric Vehicle Type**: Battery Electric Vehicle (BEV) or Plug-in Hybrid Electric Vehicle (PHEV)
- **Clean Alternative Fuel Vehicle (CAFV) Eligibility**: Eligibility for clean energy benefits
- **Electric Range**: Electric driving range
- **Base MSRP**: Manufacturer's suggested retail price
- **Legislative District, DOL Vehicle ID, Vehicle Location, Electric Utility, 2020 Census Tract**

## Project Steps

### 1. Data Exploration
- **Shape of the Data**: 112,634 rows and 17 columns
- **Data Types and Memory Usage**: Checked data types to understand the structure.
- **Missing Values**: Identified missing values in several columns:
  - 20 missing values in the **Model** column.
  - 286 missing values in the **Legislative District**.
  - 443 missing values in the **Electric Utility**.

### 2. Exploratory Data Analysis (EDA)
#### Insights Derived:
- **Missing Data**: 
  - There were missing values in the columns **Model**, **Legislative District**, and **Electric Utility**.
- **Duplicated Data**: No duplicated values found in the dataset.
- **Outliers**: Boxplots were used to identify outliers in the columns **Electric Range**, **DOL Vehicle ID**, and **Base MSRP**.
- **Data Distribution**:
  - The electric range density is higher between 0 to 45 miles, while it decreases significantly above 350 miles.
  - **City Distribution**: Seattle has the most electric vehicles, followed by Bellevue and Redmond.
  - **Make Distribution**: Tesla dominates the electric vehicle market in this dataset with over 50,000 vehicles, followed by Nissan and Chevrolet.
  - **State Distribution**: Washington (WA) has the majority of electric vehicles in the dataset.

### 3. Handling Missing Data
- Used **SimpleImputer** to handle missing values:
  - Imputed missing values in the **Model** column using the most frequent value.
  - Used the **mean** strategy to impute missing values in the **2020 Census Tract**.
  - Used the **median** strategy to impute missing values in the **Legislative District**.

### 4. Univariate Analysis
- Performed analysis using individual columns such as **Electric Range**, **City**, and **Make** to understand their distribution.
- Created KDE plots and bar plots to visualize the distribution of the electric range, cities, and make of the vehicles.

### 5. Bivariate Analysis
- Performed analysis to understand relationships between two features, such as:
  - **State vs. Electric Vehicle Type**: 
    - Washington has the most battery electric vehicles.
    - Oklahoma and North Dakota have the fewest plug-in hybrid electric vehicles.

### 6. Visualizations
- **Boxplots** were created to check for outliers in numerical columns like **Electric Range**, **DOL Vehicle ID**, and **Base MSRP**.
- **Barplots** and **Pie Charts** were used for categorical analysis, such as the distribution of cities, states, and vehicle makes.
- **Cross-tabulation** was used to explore the relationship between states and electric vehicle types.

## Tools and Libraries Used
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Seaborn**: For creating statistical plots.
- **Matplotlib**: For basic plotting and visualizations.
- **Plotly Express**: For interactive visualizations.
- **SimpleImputer (from sklearn)**: For handling missing data.

## Insights
- **Electric Range**: The electric range of most vehicles is concentrated below 100 miles, with Tesla models contributing significantly to higher ranges.
- **City and State Distributions**: Seattle (WA) has the highest concentration of electric vehicles. The dataset is heavily skewed toward Washington state.
- **Vehicle Make**: Tesla leads the market in electric vehicles, followed by Nissan and Chevrolet.
  
### Future Scope
- **Additional Analysis**: Further analysis could explore the relationship between electric vehicle range and state-specific infrastructure, or conduct predictive modeling for electric vehicle growth.
- **Time-based Trends**: Incorporating model year to analyze trends over time could provide more insight into the evolution of electric vehicle usage.

