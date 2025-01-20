# Dehli Indian Housing Part 3: Predicting Price with Location and Amenities Using Multiple Linear Regression

## Project Overview
This project explores how location features (latitude and longitude) and amenities (number of bathrooms and bedrooms) influence housing rental prices in Delhi. Building upon the foundations of Part 2, this analysis employs **Multiple Linear Regression** models to predict rental prices (`price_approx_usd`).

## Contact Details
- Email: dumisanimukuchura@gmail.com
- LinkedIn: https://www.linkedin.com/in/dumisani-maxwell-mukuchura-4859b7170/

## Objectives
- Evaluate the relationship between location and rental prices using visualizations and correlation analysis.
- Develop baseline and regression models for:\n
  - Location-based features (`latitude`, `longitude`).
  - Amenities-based features (`numBathrooms`, `numBedrooms`).
- Compare model performance using **Mean Absolute Error (MAE)**.
- Communicate results with equations and 3D visualizations.

---

## Dataset Description
The dataset contains housing rental details in Delhi, India. Below are the key columns used:

| Column              | Description                                |
|---------------------|--------------------------------------------|
| `latitude`          | Geographic latitude coordinates           |
| `longitude`         | Geographic longitude coordinates          |
| `numBathrooms`      | Number of bathrooms                       |
| `numBedrooms`       | Number of bedrooms                        |
| `price_approx_usd`  | Rental price in US Dollars                |

---

## Key Steps

### **1. Data Preparation**
- Imported and cleaned the dataset.
- Converted column data types (e.g., `numBedrooms` to float).
- Split data into training and test sets for model building and evaluation.

### **2. Exploratory Data Analysis (EDA)**
- **Heatmap Analysis**:\n
  - Evaluated correlations between features and price.
  - Observed that location features (`latitude`, `longitude`) had weak correlations with price.
  - Identified stronger correlations for amenities features (`numBathrooms`, `numBedrooms`).
- **Scatter Plots**:\n
  - Visualized location data on a 2D map and 3D scatter plot.
  - Identified concentration of high-priced properties in central Delhi.

### **3. Baseline Models**
- Established a baseline for both models by predicting the mean of the target variable (`price_approx_usd`).
- **Baseline MAE**:\n
  - Location Model: `$1651.68`
  - Amenities Model: `$1651.68`

### **4. Regression Models**
- **Location-Based Model**:\n
  - Features: `latitude`, `longitude`
  - Training MAE: `$1703.45`
  - Test MAE: `$1313.17`
- **Amenities-Based Model**:\n
  - Features: `numBathrooms`, `numBedrooms`
  - Training MAE: `$1525.08`
  - Test MAE: `$1271.72`

### **5. Communicating Results**
- **Equations**:\n
  - Location Model: `rental price = (21697 * longitude) + (-2116 * latitude) + (-451741)`
  - Amenities Model: `rental price = (-811 * numBathrooms) + (2466 * numBedrooms) + (-1322)`
- **3D Visualizations**:\n
  - Created scatter plots overlaying the regression plane for both models.

---

## Tools and Libraries Used
- **Python**
- **Pandas** and **NumPy**: Data manipulation and numerical operations.
- **Matplotlib**, **Seaborn**, and **Plotly**: Data visualization.
- **scikit-learn**: Machine learning algorithms and evaluation metrics.

---

## How to Run the Project
1. **Set Up the Environment**:
   - Install required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, `scikit-learn`.
   - Ensure the datasets (`housing_training_data.csv` and `housing_test_data.csv`) are in the `data` directory.
2. **Run the Jupyter Notebook**:\n
   - Execute cells sequentially to preprocess data, build models, and evaluate results.
3. **Analyze Results**:\n
   - Review metrics and visualizations to understand model performance.

---

## Folder Structure
Dehli-Indian-Housing-Analysis-Part3/ 
├── data/ 
│ ├── housing_training_data.csv # Training dataset 
│ ├── housing_test_data.csv # Test dataset 
├── notebook/ 
│ └── Dehli_Indian_Housing_MLR.ipynb # Jupyter Notebook for analysis 
├── visualizations/ 
│ └── plots/ # Saved plots (optional) 
├── README.md # Project documentation

---

## Project Outcome
- Demonstrated the limited predictive power of location features for rental prices.
- Highlighted the stronger predictive ability of amenities features.
- Communicated findings through model equations and visualizations.

---

## Future Work
- Incorporate additional features like `house_size_in_sqft` or `location` as categorical variables.
- Experiment with polynomial or interaction terms to capture non-linear relationships.
- Explore advanced models like decision trees or gradient boosting for better performance.

---

## References
- **Dataset**: [Kaggle](https://www.kaggle.com/datasets/bhavyadhingra00020/india-rental-house-price)
- **Contact**: Dumisani Maxwell Mukuchura | dumisanimukuchura@gmail.com | [LinkedIn](https://www.linkedin.com/in/dumisani-maxwell-mukuchura-4859b7170/)
"""