# Titanic Data Analysis
## Table of Contents

 - [Project Overview](#project-overview)
 - [Data Sources](#data-sources)
 - [Recommendations](#recommendations) 

### Project Overview
In this project we will analyze the Titanic data and see if there is a correlation between the chances of survival and certain characteristics of each passenger (gender, cabin class, ticket price, etc).

### Data Sources
Titanic data: The primary dataset used for this analysis is the "titanic_train.csv" file, containing detailed information about passengers being on board at Titanic.

### Tools

- Python: pandas - Data Cleaning and Data Analysis [Download here](https://www.anaconda.com/)
- Python: matplotlib, seaborn- Data Visualization

### Data Cleaning/Preparation
In the initial data preparation phase, we performed the following tasks: 
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Exploratory Data Analysis
EDA involved exploring the data to answer key questions, such as:
 1. How age contributed to survival rates?
 2. Who has higher chances of surviving, male or female?
 3. Does the passenger class have an impact on survival rates?
 4. Does the fare have an impact on survival rates?


### Data Analysis
Include some interesting code/features worked with:
```python
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```
```python
df.groupby('Sex').size().plot.pie( title= " Gender distribution of passengers ",
                                  colors=('lightcoral','deepskyblue'),
                                  labels=('Female', 'Male'),
                                  autopct='%1.1f%%',
                                  pctdistance=0.7,
                                  shadow=True, 
                                  explode=(0.1, 0),
                                  figsize=(5,5)                               
                                 )
```
```python
sns.heatmap(corr_mtx, annot=True, cmap='Blues', fmt='.2f')
```
### Results/Findings
Results
The analysis results are summarized as follows:
1. The age of passengers that survived is more prevalent between 20-40 y.o.
   So, in case of men, younger passengers had a higher chance of survival, but for women, older passengers.
2. More women survived than men.
3. Passengers in Class I had higher chances of surviving compared to other classes.
4. The higher the ticket fare, the higher the survival chances, with no deaths reported for fares higher than $300.

### Recommendations
Based on the analysis we recpmmend the following actions:
1. Consider further analysis to understand why younger men and older women had higher chances of survival. This could involve investigating factors such as proximity to lifeboats, assistance received, or adherence to evacuation protocols.
2. Highlight the importance of prioritizing women and potentially vulnerable groups during evacuation procedures. Further investigation could explore the reasons behind this gender disparity.
3. Emphasize the correlation between higher-class tickets and survival rates. This information could be used for future safety and evacuation protocols, ensuring that passengers in lower classes also have increased chances of survival.
4. Consider the implications of fare class on passenger location, access to lifeboats, or other safety measures. This information could be used to refine safety protocols for passengers with lower fare tickets.

### Limitations
I had to fill in the missing values in the embarked column with the most commonly appearing value. Column Cabin contains too many null values, so it was deleted from the DataFrame. Column Age was completed with median age for women and men,corresponding. They would have affected the accuracy of my conclusions from the analysis.

### References
- [About Correlations](https://towardsdatascience.com/eveything-you-need-to-know-about-interpreting-correlations-2c485841c0b8)
