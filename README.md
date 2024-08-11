
# 311 Complaint Analysis and Prediction for NYC Department of Housing Preservation and Development

This project aims to analyze and predict 311 complaints related to housing and buildings in New York City, focusing on the 'HEAT/HOT WATER' complaint type. It leverages data analytics and machine learning techniques to provide actionable insights and predictive models to assist the Department of Housing Preservation and Development in addressing these issues effectively.

## Project Goals

1. Identify the most prevalent complaint type.
2. Determine and mark areas with severe complaint concentrations.
3. Analyze the relationship between the primary complaint type and building characteristics.
4. Build predictive models to forecast the possibility of future complaints.

## Data Sources

* PLUTO 311 Complaint Data (`fhrw-4uyv.csv`) 
* PLUTO Building Characteristics Data (`BX_18v1.csv`)

## Project Steps

### 1. Project Setup and Data Loading

* Set up a Python environment with necessary libraries (pandas, NumPy, matplotlib, seaborn, scikit-learn, folium).
* Load both datasets into pandas DataFrames.
* Inspect the data structure and types.

### 2. Data Cleaning and Preprocessing

* Convert the `created_date` to datetime format in the 311 complaint data.
* Filter the 311 data to focus on relevant years.
* Standardize complaint types (e.g., combine "HEAT/HOT WATER" and "HEATING").
* Select required columns and handle missing values in the PLUTO building data.

### 3. Exploratory Data Analysis (EDA)


1. **Complaint Type Analysis:**
   * Count the occurrences of each complaint type using `value_counts()`.
   * Visualize the distribution using bar plots or pie charts.
   * Identify the most frequent complaint type ("HEAT/HOT WATER").

2. **Spatial Analysis:**
   * Filter data for the identified complaint type.
   * Create an interactive map using folium to visualize complaint hotspots by borough, street, and ZIP code.
   * Aggregate and analyze complaints by these geographic attributes.

3. **Relationship with Building Characteristics:**
   * Merge the 311 complaint data with the PLUTO building data based on common identifiers (e.g., street name, ZIP code).
   * Calculate correlations or conduct statistical tests to identify relationships between the complaint type and building characteristics.
   * Visualize these relationships using scatter plots, heatmaps, or other appropriate charts.


### 4. Predictive Modeling

1. **Approach 1: Binary Classification**

   * Create a binary target variable for the presence or absence of the complaint type.
   * Split the data into training and testing sets.
   * Train and evaluate classification models (Logistic Regression, Decision Trees, Random Forests, Gradient Boosting).
   * Plot confusion matrices and analyze feature importance.

2. **Approach 2: Complaint Count Prediction**

   * Use the number of complaints as the target variable.
   * Apply regression models (e.g., K-Nearest Neighbors) to predict complaint counts.
   * Evaluate model performance and optimize parameters.

### 5. Reporting and Insights

* Answer the four questions posed by the Department.
* Provide actionable insights and recommendations.
* Present findings in a clear and concise manner using visualizations and non-technical language.

## Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Shreyash-Gaur/NYC_311_Complaints_Analysis.git
   ```
2. **Install Dependencies:**

3. **Run the Notebook:**
   ```bash
   NYC_Housing_Complaints.ipynb
   ```

## Key Findings and Insights

* **Most Prevalent Complaint:** HEAT/HOT WATER
* **Areas with Severe Complaints:**
    * Borough: Bronx
    * Street: Grand Concourse
    * ZIP Code: 11226
* **Relationship with Building Characteristics:**
    * Strong negative correlation with building age (older buildings have more complaints).
    * Some correlation with the number of floors, built floor area ratio, and year of last alteration.
* **Predictive Models:**
    * High accuracy achieved in both binary classification and complaint count prediction tasks.
    * Models can help identify buildings at risk and enable proactive interventions.

## Recommendations

* Prioritize addressing HEAT/HOT WATER complaints in the Bronx, specifically on Grand Concourse and in ZIP code 11226.
* Focus on older buildings with a higher number of floors and larger built floor area ratios.
* Utilize predictive models to identify buildings at risk and implement preventive measures.
* Regularly update and retrain models as new data becomes available.

## Disclaimer

This project is for educational and informational purposes only. The models and insights provided are based on the available data and may not capture all the complexities of real-world situations. 

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve the analysis, models, or documentation. 
