# Steel Industry Energy Consumption Prediction

**Current Date**: Wednesday, February 05, 2025

## Project Overview
The Steel Industry Energy Consumption Prediction project aims to develop a machine learning model that predicts energy consumption in steel manufacturing processes. 
By analyzing historical data, this project seeks to optimize energy usage, enhance operational efficiency, and contribute to sustainability efforts within the industry.

## Objectives
- To analyze the factors affecting energy consumption in steel production.
- To develop a predictive model that accurately forecasts energy usage based on various input features.
- To provide insights that can help reduce energy costs and improve operational efficiency.

## Dataset Description
The dataset used for this project includes the following features:

| Variable Name                           | Type       | Description                                      | Units |
|-----------------------------------------|------------|--------------------------------------------------|-------|
| `Usage_kWh`                             | Continuous | Industry Energy Consumption                       | kWh   |
| `Lagging_Current_Reactive.Power_kVarh` | Continuous | Lagging Reactive Power                           | kVarh |
| `Leading_Current_Reactive_Power_kVarh` | Continuous | Leading Reactive Power                           | kVarh |
| `CO2(tCO2)`                            | Continuous | CO2 Emissions                                   | ppm   |
| `Lagging_Current_Power_Factor`         | Continuous | Lagging Power Factor                             | %     |
| `Leading_Current_Power_Factor`         | Continuous | Leading Power Factor                             | %     |
| `NSM`                                   | Integer    | Not Specified                                   | s     |
| `WeekStatus`                            | Categorical| Weekend (0) or Weekday (1)                     |       |
| `Day_of_week`                          | Categorical| Sunday, Monday, ..., Saturday                   |       |
| `Load_Type`                            | Categorical| Light Load, Medium Load, Maximum Load           |       |

### Data Collection
The information gathered is from the DAEWOO Steel Co. Ltd in Gwangyang, South Korea. It produces several types of coils, steel plates, and iron plates.
The data was downloaded from UCI Machine Learning Repository using the **ucimlrepo** package. The dataset consists of 35040 observations covering.

## Methodology
### Data Preprocessing
- **Data Cleaning**: Missing values were handled appropriately, and outliers were addressed.
- **Feature Engineering**: New features were created based on existing variables to enhance model performance.
- **Encoding Categorical Variables**: Categorical variables were converted into numerical format using one-hot encoding.

### Exploratory Data Analysis (EDA)
EDA was conducted to understand relationships between variables and visualize trends in energy consumption. Key findings include:
- A correlation analysis indicated significant relationships between energy consumption and certain features such as reactive power and power factors.
- Visualizations revealed patterns in energy usage across different days of the week and load types.

### Model Development
The Machine Learning algorithm used is Random Forest Classifier.

After training and evaluating these models, the Random Forest Classifier achieved the highest accuracy of **91%** on the test dataset.

### Model Evaluation
The model was evaluated using metrics such as:
- Accuracy
- Precision
- Recall
- F1-score

A confusion matrix was generated to visualize prediction performance across different load types.

## Results
The model successfully predicted energy consumption with an accuracy of 91%. Key insights include:
- The most influential features affecting energy consumption were identified.
- The model can effectively differentiate between light, medium, and maximum load types based on input parameters.

### Example Visualization
![Correlation](https://github.com/user-attachments/assets/fee98220-6e4b-4b64-939f-4a0cb7b9b51a)
