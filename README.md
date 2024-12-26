# **Project Description**
## **Overview**:  
This project explores how various car features impact pricing and profitability. It aims to help car manufacturers optimize their pricing strategies and product development by identifying features that drive consumer demand and profitability.

## **Business Problem**:  
How can a car manufacturer optimize pricing and product development decisions to maximize profitability while meeting consumer demand?

## **Data Sources**:  
The dataset, titled "Dataset" contains 11,915 observations and 16 variables, including details on car make, model, year, fuel type, engine specifications, and MSRP. The data was sourced from Kaggle and represents trends up to 2017.

## **Data Cleaning and Preprocessing**:  
- Missing values were identified and handled appropriately.
- Cleaned text and removed extra spaces.
- Duplicated values were identified and removed.
- Blank rows were identified and removed.
- Columns like Year, which were stored as strings, were converted to integers for chronological analysis.
- Converted MSRP and Engine HP from strings to numerical data types (e.g., float) for calculations.
- Adjusted Number of Doors from float to integer for logical consistency.

---

# **Approach**
**Analytical Methods**:  
- Descriptive statistics to summarize data trends.
- Regression analysis to model the relationship between features and MSRP.
- Visualizations, including scatter plots, combo charts, and bar charts, to explore patterns.

## **Reasoning Behind Methods**:  
- Regression analysis identifies significant predictors of price, helping prioritize feature development.
- Visualizations simplify the communication of complex relationships for stakeholders.

## **Modeling Techniques**:  
- Multiple linear regression for price prediction.
- Correlation analysis to study relationships between variables like fuel efficiency and engine cylinders.

---

### **Tech-Stack Used**
**Tools and Software**:  
- **Excel**: Pivot tables, Regression Analysis, Power Query Editor, Charts, Slicers, VLOOKUP and HLOOKUP

**Reasoning**:  
- Excel was chosen for its ease of use in business contexts.

---

# **Insights**
1. **Market Category Popularity**:  
   - Luxury and performance categories show high average prices but varied popularity.
   - Crossovers dominate in terms of model count and consumer interest.

2. **Feature Importance for Pricing**:  
   - Engine HP and market category significantly influence MSRP.
   - Vehicle style and size also contribute but with less weight.

3. **Fuel Efficiency and Engine Cylinders**:  
   - Cars with fewer cylinders generally exhibit higher fuel efficiency.

## **Recommendations**:  
- Focus on optimizing features in the luxury and crossover segments.
- Develop pricing strategies that reflect consumer interest in performance and sustainability.

---

# **Results**
**Visualizations and Tables**:  
- **Combo Chart**: Relationship between market category popularity and model count.

  ![image](https://github.com/user-attachments/assets/8d584c12-f1b7-43c7-aa41-e4b6c13bdb86)    


- **Scatter Plot**: Engine HP vs. MSRP with a trendline.

  ![image](https://github.com/user-attachments/assets/57bcb4d5-c6c5-4fd5-a756-66abbc7e2803)    


- **Bar Chart**: Feature importance in predicting MSRP.

  ![image](https://github.com/user-attachments/assets/a2ca30c3-ef07-44e0-8e87-2cea3b87b484)

  ![image](https://github.com/user-attachments/assets/91bd8e80-15a2-4b80-856e-caf028dcd886)


- **Horizontal Stacked Bar Chart**: Relationship between manufacturer and average price.

  ![image](https://github.com/user-attachments/assets/e6e19e14-167d-45e8-b2f3-9dd32efb5ff6)



- **Scatter Plot**: No. of Cylinders vs highway MPG with regression line.

  ![image](https://github.com/user-attachments/assets/78f97a0d-3f86-4a7e-879e-8c278bf7dd71)

  ![image](https://github.com/user-attachments/assets/62620d31-4725-4486-b82d-ec0d717fba32)


- **Stacked Column Chart**: Distribution of Car Prices by Brand and Body Style

  ![image](https://github.com/user-attachments/assets/91137960-d27d-430b-bb65-c7f8fe016e61)


- **Table**: Min and Max MSRP by body style.

  ![image](https://github.com/user-attachments/assets/007002ea-79ce-43da-a43c-4cb2c5f363fd)


## **Discussion**:  
- The analysis highlights actionable insights for car manufacturers to refine their strategies.
- Limitations include the dataset's age and potential bias in imputation methods.

## **Future Directions**:  
- Incorporate recent data to capture emerging trends like EVs and autonomous vehicles.
- Extend analysis to include consumer demographics for targeted marketing.
