# Game Data Analytics and Machine Learning Models

## Overview

This project involves analyzing a dataset of game apps to gain insights into game quality, ratings, pricing, and genres. It also applies machine learning models to predict **Average User Rating** based on various features of the games. The key objectives of the project are:

1. Perform **Exploratory Data Analysis (EDA)** on the game app data to gain valuable insights.
2. Extract meaningful insights related to **developers**, **genres**, **rating trends**, **pricing**, and **user engagement**.
3. Train and evaluate various **machine learning models** to predict **Average User Rating** based on game features.

---

## Data Overview

The dataset used in this project contains various features related to mobile game applications. The key columns in the dataset are:


- **URL:**** The URL associated with the game.
- **ID:** The unique identifier for the game.
- **Name:** The name of the game.
- **Subtitle:** A secondary title or subtitle for the game.
- **Icon URL:** The URL for the game's icon.
- **Average User Rating:** The average rating provided by users.
- **User Rating Count:** The total number of ratings received by the game.
- **Price:** The price of the game.
- **In-app Purchases:** Information about any in-app purchases.
- **Description:** The description of the game.
- **Developer:** The developer of the game.
- **Age Rating:** The age rating for the game.
- **Languages:** The languages the game supports.
- **Size:** The size of the game in MB.
- **Primary Genre:** The primary genre of the game.
- **Genres:** The genre(s) of the game.
- **Original Release Date:** The original release date of the game.
- **Current Version Release Date:** The release date of the current version of the game.


---

## Data Preprocessing

### 1. Missing Value Handling

- **Numeric Columns**: Missing values in numeric columns like `Size` and `Average User Rating` were filled with the **mean** value of the respective columns.
- **Categorical Columns**: Missing values in categorical columns like `Developer` and `Genres` were replaced with the **mode** (most frequent value).
- **Dropped Irrelevant Columns**: Columns that were deemed unnecessary for analysis were dropped to improve the dataset's quality.

---

### 2. Feature Engineering

- **Language Count**: A new column **Language_Count** was created by counting the number of languages listed for each game app. The **Languages** column was subsequently dropped.
- **One-Hot Encoding**: The **Primary_Genre** column was transformed using one-hot encoding to convert categorical data into numerical values for machine learning models.

---

### 3. Data Transformation

- **Log Transformation**: The `Size` column was log-transformed to reduce skewness and handle outliers. The new log-transformed column was named `Log_Size`.
- **Outlier Handling**: Outliers in columns like `Price` were detected using the **Interquartile Range (IQR)** method and were capped or removed based on certain thresholds.

---

## Exploratory Data Analysis (EDA)

### 1. Descriptive Statistics

The initial step in EDA involved calculating basic descriptive statistics of the numerical features, including:

- Mean, Median, and Mode
- Standard Deviation and Variance
- Range (Min-Max)
- Distribution shape

### 2. Data Visualizations

Several visualizations were created to understand the distribution and trends in the data:

- **Rating Counts by Genre**: A bar chart showing the total rating counts for each genre.
- **Price Distribution**: A histogram to visualize the distribution of game prices.
- **Average User Rating Trend**: A line plot showing the trend of average user ratings from 2010 to 2015.
- **Top 5 Games by User Rating Count**: A bar chart representing the games with the highest rating counts.

These visualizations provided valuable insights into the relationships between various features in the dataset.

---

## Machine Learning Model Development

### 1. Model Selection

Several machine learning models were used to predict the **Average User Rating** based on other game features. These models include:

- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Support Vector Machine (SVM) Regressor**
- **k-Nearest Neighbors (KNN) Regressor**

### 2. Model Training and Evaluation

The dataset was split into training and testing sets using a **70-30 split**. The models were then trained using the training data, and their performance was evaluated based on the **Root Mean Squared Error (RMSE)** metric.

**Model Performance:**
- **Linear Regression**: RMSE = 0.512
- **Decision Tree Regressor**: RMSE = 0.645
- **Random Forest Regressor**: RMSE = 0.480
- **Support Vector Machine (SVM) Regressor**: RMSE = 0.520
- **k-Nearest Neighbors (KNN) Regressor**: RMSE = 0.552

From the results, **Random Forest Regressor** performed the best with the lowest RMSE, suggesting it is the most effective model for predicting the **Average User Rating**.

---

## Key Insights and Recommendations

1. **Top Developers by App Count**: 
   - Tapps Technology and Vikash Patel are the top two developers with 121 and 94 apps, respectively.

2. **Genres with the Highest Rating Counts**: 
   - Strategy games have the highest rating counts (11M), followed by Action (5M) and Entertainment (4M) genres.

3. **Average User Rating Trend**: 
   - The average user rating has steadily increased from around 0.2 in 2010 to around 10.9 in 2015, indicating an overall improvement in game quality over time.

4. **Top 5 Games by Rating Count**:
   - Games like **Clash of Clans**, **Clash Royale**, **Plants vs Zombies 2**, **Pokémon GO**, and **PUBG MOBILE** have the highest rating counts.

5. **Age Rating**: 
   - The minimum age rating in the dataset is 4, while the maximum is 17, suggesting a wide range of game content suitable for different age groups.

6. **Most Expensive Games**:
   - Premium titles such as **African Cheetah Wild Animal Simulator 3D Full** and **Army Truck Offroad Simulator 3D Full Drive mini truck** are among the most expensive games in the dataset.

---
## Reports
 The reports folder contains the following files:

MobileGamesDataAnalysis.pdf: A detailed report of the game data analysis.
MobileGamesDataAnalysis.pbix: Power BI file containing the dashboard for the analysis.
MobileGamesDataAnalysis_dashboard.pdf: A PDF version of the dashboard.

## Data
The data folder contains the following files:

appstore_games.csv: The raw dataset containing information about mobile game apps.
newgamesclean.csv: The cleaned version of the dataset after preprocessing.

## Scripts
The scripts folder contains the following file:

MobileGamesDataAnalysis.ipynb: Jupyter Notebook containing the full code for data analysis, preprocessing, and machine learning model training.


## Conclusion

The project successfully identified key patterns in the game app dataset through EDA and built effective machine learning models to predict **Average User Rating**. The **Random Forest Regressor** was the top-performing model, making it the most suitable choice for rating prediction. The insights gathered provide valuable recommendations for game developers and businesses in the gaming industry, especially in terms of pricing, genre preferences, and strategies for improving user ratings.


---

## Acknowledgments

We would like to acknowledge the creators of the dataset for providing valuable data that enabled this analysis. Additionally, we appreciate the contributions of various open-source libraries like **Pandas**, **Matplotlib**, **Seaborn**, and **Scikit-learn** for making this project feasible.

---
