# Life Expectancy Analysis and Linear Regression Model

## Project Overview  
This project explores the factors affecting life expectancy using a dataset of global health indicators. The analysis includes exploratory data analysis (EDA), feature preprocessing, and the development of a linear regression model to predict life expectancy based on selected features.

---

## Dataset Description  
The dataset contains information on 22 columns related to health, economy, and demographics from 193 countries between 2000 and 2015. Below are some key columns used in this analysis:  

- **Life expectancy**: Target variable representing the average lifespan in years.  
- **Schooling**: Average number of years of schooling.  
- **Income composition of resources**: A measure of income level (scaled between 0 and 1).  
- **Adult Mortality**: Probability of dying between the ages of 15 and 60 per 1,000 population.  
- **Status**: Development status of the country (Developed or Developing).  

---

## Steps and Methodology

1. **Data Loading and Initial Inspection**  
   - Loaded the data and provided an overview of columns and missing values.
   - Summary statistics were generated for a better understanding of data distribution.

2. **Data Preprocessing**  
   - Missing values were filled using the median for numerical columns.  
   - Converted the categorical column `Status` to binary (1 for Developed, 0 for Developing).  
   - Scaled features using `StandardScaler` for better performance in the linear regression model.

3. **Exploratory Data Analysis (EDA)**  
   - Histograms and scatter plots were used to visualize the distribution and relationships between key variables.  
   - Correlation analysis was performed using a heatmap to identify potential multicollinearity.  

4. **Model Development**  
   - A linear regression model was built using `sklearn`.  
   - The dataset was split into training (80%) and testing (20%) sets.  
   - Model coefficients, intercept, mean squared error (MSE), and R-squared (R²) score were evaluated.

5. **Model Evaluation**  
   - Residuals were analyzed using histograms, Q-Q plots, and scatter plots to ensure they followed a normal distribution and met linear regression assumptions.

---

## Results and Performance  

- **Model Coefficients**:  
   ```
   Schooling: 3.07  
   Income composition of resources: 2.26  
   Status: 0  
   Adult Mortality: -4.37  
   ```
- **Intercept**: `69.25`  
- **Mean Squared Error (MSE)**: `25.87`  
- **R-squared (R²)**: `0.70`

### Visualizations
- **Distribution of Life Expectancy**  
  Histogram showing the distribution of life expectancy values.
  
- **Scatter Plots**  
  Visualized relationships between life expectancy and key features (Schooling, Income Composition, and Adult Mortality).  
- **Correlation Matrix**  
  Heatmap showing correlations between input features.

---

## Usage Instructions  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/life-expectancy-analysis.git
   ```
2. Install required packages:  
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn statsmodels
   ```
3. Run the analysis script:  
   ```bash
   python analysis.py
   ```
4. Review results and visualizations.

---

## Dependencies  

- Python 3.x  
- pandas  
- numpy  
- seaborn  
- matplotlib  
- scikit-learn  
- statsmodels  

---

## Future Improvements  

- Use advanced regression models such as Ridge or Lasso to improve accuracy.  
- Explore feature selection techniques to reduce multicollinearity.  
- Perform time-series analysis to capture trends over time.  

---

## Author  
**Sayantika**  
