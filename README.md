# AI-and-ML-Internship---Task-1
Data cleaning and preprocessing on Titanic dataset

This is basic task to learn about and familiarize with using Datasets and on how to handle it. 
To clean and prepare the Titanic dataset for machine learning tasks by handling missing data, encoding categorical features, scaling numeric values, and removing outliers.

# Dataset Description :
We used the Titanic dataset which was based on the famous Titanic shipwreck. Due to insufficient lifeboats, many were dead including the passengers and crew members. The dataset is created to work on with models to find out the more likely reasons for survival using the available passenger's personal information like age, gender, socio-economic class,etc.

# 🛠 Tools Used
- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

# Steps Performed

# 1. Importing and Exploring the Dataset

 For the 1st subsection, we initially loaded the CSV Dataset using pandas comment `pd.read_csv`. It will read over all the information present in the dataset. Then we explored the structure and datatypes using `.info()` and `.head()`. Also to ensure that the dataset doesnt have any empty values, because it might lead to wrong decisions, we identified missing values using `.isnull().sum()`.

# 2. Handling Missing Values
To ensure the dataset is clean we handled missing values in which, for the `Age` column, which is numerical, we filled in the missing entries using the median value. For the `Embarked` column, which is categorical, we filled the missing values with the most frequent category (mode). Since the Cabin column had too many missing values, we dropped it from the dataset. 

# 3. Converting Categorical Features to Numerical
ML models work best with numbers, so we needed to convert categorical (text-based) data into numeric form. We converted the `Sex` column by using label encoding, where 'male' was represented as 0 and 'female' as 1. For the `Embarked` column, which had multiple categories, we used one-hot encoding. 

# 4. Normalizing Numerical Features
Since features like `Age` and `Fare` had different range of values, we applied standardization to bring all numeric values to a similar range. Using `StandardScaler`, we scaled features like Age, Fare, SibSp, and Parch to have a mean of 0 and standard deviation of 1. 

### 5. Outlier Detection and Removal
Outliers are extreme values that can affect the performance negatively of ML model. To detect them, we used boxplots to visually identify any unusually high or low values in columns like `Age` and `Fare`. We then used the IQR (Interquartile Range) method to mathematically filter out these outliers. Any values lying outside 1.5 times the IQR from the first and third quartiles were considered outliers and removed. 

# Output
A cleaned and preprocessed version of the Titanic dataset.


# Notes
This task was part of an internship learning module for machine learning.

