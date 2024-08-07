# Titanic-Survival-Data-Analysis-Power-BI
This report presents a comprehensive analysis of the Titanic dataset, which contains information about passengers tragic deaths. The report aims to explore factors influencing passenger survival and gain insights into patterns and trends related to the tragedy. By analyzing this dataset, we can better understand the circumstances surrounding the Titanic disaster and identify key factors that contributed to survival rates.

The Titanic dataset provides a wealth of information about passengers on board, including their demographics, cabin class, ticket fare, family relationships, and survival status. This dataset offers a unique opportunity to analyze the factors that influenced passenger survival during the Titanic disaster.

## DATA EXPLORATION:

The Titanic dataset consists of several variables, including passenger demographics, sex, ticket details, age, survival status, embarkation, class of travelling,  etc. These variables allow us to examine different aspects of the passengers' profiles and survival outcomes.

## DATA QUALITY:

Before conducting the analysis, performed a thorough data quality check to ensure data integrity and consistency. This process involved handling missing values, removing duplicates, and addressing any inconsistencies in the dataset.

## Dashboard includes analysis on:

### Introduction 

### Insights

### Age Group

### Embarkation

### Gender

### Passenger Class

## Analysis done on:

Cards: Total Passengers, Survived, Died, Total Fare, Maximum Fare, Average Fare, Maximum Age, Total Male Passengers, Total Female Passengers.

Slicers: Sex, Age Group, Embarked, Passenger Class.

Table: Survived Passengers, Died Passengers.

Stacked Column Chart: Survived and Died by Age Group

Funnel: Survived by Age Group, Average of Fare by Embarked

Waterfall Chart: Average of Fare by Age Group, Family Size by Gender, Average of Fare by Class.

Stacked Area Chart: Total Passengers by Age Group

Clustered Column/bar Chart: Survived by Embarked, Survived by Passenger Class, Family Size by Class.

Donut Chart: Total Passengers by point of Embarkation, Total Passengers by Gender, Total Passengers b Class.

Pie Chart: Family Size by Embarked.

Ribbon Chart: Survived by Gender.

Line and Clustered Column Chart: Average of Fare by Gender and Survived.

## Data Analysis Expressions (DAX) Formulas used in Measures:

Total Passengers = COUNT(train[PassengerId])

Total Fare = SUM(train[Fare])

Average of Fare = AVERAGE(train[Fare])

Male Count = 
CALCULATE ( 
    COUNTROWS ( 'train' ),
    'train'[Sex] = "male"
)

Female Count = 
CALCULATE ( 
    COUNTROWS ( 'train' ),
    'train'[Sex] = "female"
)

Survived = 
CALCULATE ( COUNTROWS ( train ),train[Survived] = 1 )

Died = 
CALCULATE ( COUNTROWS ( train ), train[Survived] = 0 )
