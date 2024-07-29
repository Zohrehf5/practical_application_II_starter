<<<<<<< HEAD
=======

>>>>>>> 212e983 (Readme file)

[Report](CarPriceReport.docx)

# What drives the price of a car?

The main objective of this application is to analyze and identify the factors that impact car prices. By conducting this analysis, we will provide valuable recommendations to our client, a used car dealership, regarding the features and qualities that consumers value in a used car. This will help the dealership make more informed decisions and improve their understanding of customer preferences.
The application uses Vehicle Dataset from Kaggle, which contains around 426K samples of used cars. In this application, we have explored various aspects of the dataset, such as the car's manufacturer, model, year, mileage, condition, and other relevant attributes. It is important to keep in mind the specific needs and objectives of the client to ensure that the final recommendations are relevant, practical, and aligned with their goals.

We used industry standard process, named CRISP-DM framework, to work through a data problem.


**Data Understanding:**
- Exploratory Data Analysis (EDA)
- Load and Read DataSet
- Understand Features and Datatype
- Analyse Data and Statistics

***About Dataset***
The vehicles dataset contains total 18 features/variables including target variable named price. Here's brief about each feature:
- id: Unique identifier of each sample
- region: Region where vehicle belongs to
- price: Price of a Vehicle
- year: Year of a vehicle
- manufacturer: Manufactures of a vehicle i.e. Ford, Toyota etc.
- model: Model of the vehicle i.e. Elantra, Camry etc.
- condition : Condition of a Vehicle
- cylinders : No. of Cylinders in a vehicle
- fuel : Fuel type of a vehicle i.e. Gas, Electric etc.
- odometer : No. of Kms/Miles vehicle has driven
- title_status : Title of a vehicle
- transmission : Transmission type of a vehicle i.e. manual/auto etc.
- VIN : Unique Identifier of a vehicle
- drive : Drive type of a vehicle i.e front wheel drive etc.
- size : Size of a car i.e. full-size, compact etc.
- type : Vehicle type
- paint_color : Color of a Vehicle i.e. white/black etc.
- state : State of a vehicle

**Data Preparation:**  
Following steps are done for Data Preparation:

 - Break down the data to cat_col(categorical columns) and num_col (numerical columns)
 - Handle Missing Values and Feature Encoding
 - Handle Outliers, correct data types
 - Handling inconsistent data
 - Visualize cleaned Data
 - Drop unnecessary features that don't have impact on the price

 **Modeling:**
We have analysed the data against various regression models through different hyperparameters and perform cross validation to determine the best suited model for a vehicle dataset. The models used in current applications are:

1- Linear Regression Model with Polynomial Degree
2- Lasso Regression Model with Feature Selection =3
3- Linear regression model using feature selection using GridSearchCV
4- Ridge Regression Model using best alpha

**Evaluation:**
Above models are evaluated based on RMSE and R2. Best model is Linear Regression Model with Polynomial Degree =2
On all models permutation_importance is run and plotted feature importance. Also it is diagrammed the actual vs prediction.  


## Overall Conclusion:  
***Top Features Influencing Car Price:***
- Year: The model suggests that the year of the car is the most significant factor influencing its price. This is expected as newer cars tend to be more expensive.
- Drive: This feature also plays a significant role in determining the price. Different drive types (e.g., 2WD, 4WD) can affect the price.
- Odometer: The mileage of the car is another crucial factor. Cars with lower mileage typically have higher prices.
- Fuel: The type of fuel the car uses is an important factor. Cars that use cheaper or more efficient fuel types may have different pricing.
- Cylinders and Transmission: These features also contribute to the price. The number of cylinders and the type of transmission (manual or automatic) can affect the vehicle's price.


***Next steps and Recommendations:***
- Year and Odometer plays significant role in Vehicle price. Keep vehicles of recent year and less Odometer value vehicles
- Continue to gather new samples for recent years data, evaluate & tune model to improve price prediction and determines the factors that drives Vehicle Price.
- Analyze the residuals (differences between actual and predicted prices) to identify any patterns that might indicate areas where the model is underperforming.
