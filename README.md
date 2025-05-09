# Montevideo Housing Price Prediction

This project explores the spatial dynamics of housing prices in Montevideo, Uruguay, using a multiple linear regression model with **longitude** and **latitude** as predictors.

## Objective
To model and visualize how geographic location influences housing prices, and to evaluate the predictive power of spatial features using a simple, interpretable regression approach.

---

## Dataset
The dataset consists of real estate listings scraped from [Properati](https://www.kaggle.com/datasets/jluza92/argentina-properati-listings-dataset-20202021) via Kaggle, containing real estate listings from Argentina, Uruguay, Brazil, and the United States.

For this analysis, we focused on:
- Properties located in **Montevideo**
- Listings priced under **$500,000**
- Records with valid **latitude** and **longitude**

---

## Steps

### 1. Data Cleaning
- Filtered out outliers above $500,000
- Removed columns with over 50% missing values
- Focused on properties in Montevideo for regional consistency
- Dropped rows with missing geographic coordinates

### 2. Visualization
- Created a **3D scatter plot** to show how price varies across location:
  - X-axis: Longitude  
  - Y-axis: Latitude  
  - Z-axis: Price

- Color-coded plots were used to encode price gradients across the city.

### 3. Baseline Model
To evaluate model performance:
- Calculated the **mean price**: \$113,822.5
- Predicted this mean for all records as a baseline
- **Baseline MAE**: 93,016.9

### 4. Linear Regression Model
Using `latitude` and `longitude` as predictors:
- **Intercept**: 3,207,000  
- **Longitude coefficient**: –44,831  
- **Latitude coefficient**: –23,961  

These values suggest that prices decrease as we move east or north within Montevideo.

- **Model MAE**: 92,655.09 — an improvement over the baseline

---

## Takeaways
Even with just two spatial features, we captured a geographic pricing gradient.
- Areas farther east or north tend to have lower prices.
- Although the model is basic, it sets a strong foundation for more complex spatial or machine learning models.

---

## Next Steps
- Incorporate non-spatial features (e.g. number of rooms, amenities)
- Apply advanced models (e.g. decision trees, random forests, or geospatial clustering)
- Build an interactive dashboard using Plotly Dash or Streamlit

---

## Author

**Harris Tekenah**  
[LinkedIn](https://www.linkedin.com/in/harris-tekenah-981223307/)  
[GitHub](https://github.com/HarrisTekenah)
