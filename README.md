# Netflix Movies and TV Shows Classification Project

## Overview
This project aims to classify Netflix content as either a movie or a TV show using machine learning techniques. The dataset used contains detailed information about various titles available on Netflix, including their attributes such as director, cast, country of production, and more.

## Table of Contents
- [Objective](#objective)
- [Dataset](#dataset)
- [Data Understanding](#data-understanding)
- [Data Preprocessing](#data-preprocessing)
- [Feature Engineering](#feature-engineering)
- [Visualization](#visualization)
- [Machine Learning Model](#machine-learning-model)
- [Results](#results)
- [Conclusion](#conclusion)
- [Installation](#installation)
- [Usage](#usage)

## Objective
The primary goal of this project is to classify Netflix content into two categories: Movies and TV Shows. This classification will help in understanding the distribution and characteristics of content available on the platform.

## Dataset
The dataset used in this project is the "Netflix Movies and TV Shows" dataset, which contains 8,807 entries and 12 columns. Key columns include:
- **Type**: Indicates whether the entry is a Movie or TV Show (target variable).
- **Title**: Title of the content.
- **Director**: Director of the content.
- **Cast**: Actors involved.
- **Country**: Production country.
- **Date_Added**: Date the content was added to Netflix.
- **Release_Year**: Year of release.
- **Rating**: TV rating.
- **Duration**: Total duration in minutes or number of seasons.
- **Listed_In**: Categories of the content.
- **Description**: Brief description of the content.

## Data Understanding
The dataset was loaded using Pandas, and initial exploration included checking for null values, data types, and basic statistics. The target label identified is the **Type** column.

## Data Preprocessing
1. **Handling Missing Values**: Missing values were filled or dropped based on their significance.
2. **Data Type Conversion**: Object data types were converted to categorical for better handling.
3. **Feature Engineering**: New features were created, such as `Years_On_netflix` and splitting the `Duration` column into `Duration_value` and `Duration_Type`.

## Feature Engineering
- Explored the `Rating`, `Date_Added`, and `Listed_In` columns to create meaningful features.
- Label encoding was applied to categorical columns to prepare for machine learning.

## Visualization
Various visualizations were created to understand the distribution of content types, ratings, durations, and the impact of directors on the dataset using libraries like Matplotlib and Plotly.

## Machine Learning Model
1. **Data Splitting**: The dataset was split into training and testing sets (70% training, 30% testing).
2. **Model Selection**: A Logistic Regression model was chosen for classification.
3. **Model Evaluation**: The model's performance was evaluated using accuracy, confusion matrix, and classification report, achieving an accuracy of 100%.

## Results
- The model demonstrated excellent performance with an accuracy of 100%.
- The ROC Curve and AUC score were calculated to assess the model's ability to distinguish between classes.
- A learning curve was plotted to evaluate potential overfitting or underfitting.

## Conclusion
The project successfully classified Netflix content into movies and TV shows using various features from the dataset. The preprocessing steps ensured data quality, while the Logistic Regression model demonstrated excellent performance. Future work could involve exploring more complex models or additional features to enhance classification accuracy further.

## Installation
To run this project, ensure you have the following libraries installed:
```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn imbalanced-learn xgboost
```

## Usage
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd <project-directory>
   ```
3. Run the Jupyter Notebook or Python script to execute the analysis.

Feel free to explore the code and modify it for your own analysis or improvements!
