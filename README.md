# DA-Internship-Task-5

# 1. Data Overview
   
•	Dataset loaded from train.csv.

•	Basic inspections like head() showed the dataset has typical Titanic features such as Survived, Pclass, Sex, Age, Fare, etc.

## 2. Data Information
            
•	train_df.info() revealed:

o	Total entries: 891 rows.

o	Some columns have missing values.

o	Mixture of data types: integer, float, and object (categorical).

## 3. Summary Statistics
            
•	train_df.describe() showed:

o	Age range: ~0.42 to 80 years.

o	Fare had a wide spread (min=0, max=512).

o	Mean Age was around 29.7 years.

o	Ticket prices were highly skewed, with most fares lower and few extremely high.

## 4. Missing Values Analysis
           
•	train_df.isnull().sum() revealed:

o	Age has 177 missing values.

o	Cabin has 687 missing values (high percentage, around 77% missing).

o	Embarked has 2 missing values.

•	Total Missing Values: 866 across the entire dataset.

## 5. Target Variable (Survived) Distribution
   
•	train_df.Survived.value_counts():

o	0: 549 passengers (did not survive).

o	1: 342 passengers (survived).

•	Conclusion: The dataset is imbalanced with more non-survivors than survivors.

## 6. Feature Distributions (Univariate Analysis)
   
•	Histograms for Age and Fare:

o	Age is approximately normally distributed but slightly skewed to the right (more young people).

o	Fare distribution is highly right-skewed (majority paid low fare, few paid very high fares).

•	Countplots for categorical variables (Survived, Pclass, Sex, Embarked):

o	Pclass:

	Class 3 had the highest number of passengers.

o	Sex:

	More males than females in the dataset.

o	Embarked:

	Most passengers embarked from port 'S' (Southampton).

## 7. Bivariate Analysis (Relationships with Survived)
   
•	Pclass vs Survived:

o	Survival rate decreases as the class number increases.

o	1st class passengers had the highest survival rate.

•	Sex vs Survived:

o	Females had a significantly higher survival rate than males.

•	Embarked vs Survived:

o	Passengers who embarked at 'C' (Cherbourg) had a higher survival rate compared to 'S' and 'Q'.

## 8. Multivariate Visualization
            
•	Heatmap of Correlations (not shown fully but implied):

o	Strong correlations noted:

	Fare positively correlated with Pclass.

	Survived correlated with Sex and Pclass.
