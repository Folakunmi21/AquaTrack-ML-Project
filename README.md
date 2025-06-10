# AquaTrack-ML-Project
AquaTrack is a data science and machine learning project designed to help identify the risk of water shortages across different locations using rainfall data. This project was built using real precipitation data from Lagos, Nigeria, sourced from Kaggle.

![rainfall](weather-effects-composition.jpg)

---

## **What Does AquaTrack Do?**

The core goal of AquaTrack is to build a predictive model that classifies whether a particular area is at risk of water shortage based on rainfall trends. The tool uses historical weather data to learn patterns that might signal low water availability.

It does this through:

- **Temporal analysis** – understanding how rainfall varies over time  
- **Spatial analysis** – analyzing how precipitation differs across different parts of Lagos  
- **Machine learning modeling** – predicting water shortage risk using engineered features from the data

---

## 🛠 **Tools and Technologies Used**

- **Python** for programming  
- **Pandas** & **NumPy** for data wrangling  
- **Matplotlib** & **Seaborn** for data visualization  
- **Scikit-learn** for machine learning (Random Forest Classifier)  
- **Jupyter Notebook** as the development environment

---

## **Key Steps in the Pipeline**

- **Data Cleaning**  
  - Handled missing values  
  - Removed irrelevant data columns  

- **Exploratory Analysis**  
  - **Temporal patterns** – how rainfall changes over days and months  
  - **Spatial patterns** – rainfall intensity across different coordinates  

- **Feature Engineering**  
  - Recent rainfall trends (7-day and 30-day rolling averages)  
  - Rainfall deficit (how far current rain is from expected monthly average)  
  - Consecutive dry days (measuring ongoing dryness)  
  - Seasonal patterns (categorizing months into seasons)  

- **Model Training**  
  - Trained a Random Forest classifier to predict risk of water shortage as a binary label  
  - Evaluated using accuracy, confusion matrix, and feature importance  

---

## **Outcome**

The model identifies which features most strongly influence the risk of water shortage.

- The most important feature was **rainfall_vs_location_avg**, which compares current rainfall levels to the long-term average for each location.  
- Other high-impact features included:  
  - **consecutive_dry_days** – measures the number of days without rainfall  
  - **rainfall_30day** – captures total rainfall over the past month  
- These features help the model detect patterns of prolonged dryness that may signal drought conditions.  
- Additional variables like **rainfall_deficit** and **rainfall_7day** provided short-term deviations from normal precipitation.  
- While features such as **month**, **day_of_year**, and **season** were included, they had lower influence compared to the rainfall-based metrics.

Together, these engineered features allowed the model to effectively assess water shortage risks based on both temporal and location-specific rainfall trends.
