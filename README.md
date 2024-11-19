### Bangalore Home Price Prediction
This project predicts property prices in Bangalore using various features like location, total area (in square feet), number of bedrooms, bathrooms, etc. The solution involves data preprocessing, feature engineering, and training machine learning models, with a Flask-based API for serving predictions.

### Table of Contents : 
Dataset
Installation
Usage
Project Structure
Key Features
Technologies Used
Results
Future Enhancements
Contact

### Dataset
The dataset contains information about various properties in Bangalore, including:
Location
Size (e.g., "2 BHK," "4 Bedroom")
Total Square Feet
Price (in Lakhs)
Number of Bathrooms
The raw dataset was preprocessed to handle missing values, outliers, and categorical encoding.


### Use the /predict_home_price endpoint by sending a POST request with the following fields:
total_sqft: Total area in square feet (float)
location: Location of the property (string)
bhk: Number of bedrooms (integer)
bath: Number of bathrooms (integer)

Example Request:

json
Copy code
{
    "total_sqft": 1200,
    "location": "Whitefield",
    "bhk": 3,
    "bath": 2
}

### Project Structure
data: Contains raw and preprocessed datasets.
notebooks: Jupyter notebooks for exploratory data analysis and model building.
artifacts: Saved models and column metadata for prediction.
app.py: Flask application for prediction.
utils.py: Utility functions for preprocessing and prediction logic.
Key Features
Data Cleaning: Handled missing values, converted non-standard formats for square footage, and removed outliers.
Feature Engineering: Engineered features like price_per_sqft and consolidated rare locations into a single category.
Machine Learning Models: Compared Linear Regression, Lasso, and Decision Tree models using GridSearchCV.
API Integration: A Flask API for predicting property prices based on user inputs.
Model Deployment: Serialized the trained model for use in a production environment.

### Technologies Used
Languages: Python
Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Flask
Tools: Jupyter Notebooks, Pickle for model serialization
Frameworks: Flask for API development

### Results
Achieved a score of 84.9% on training data using Linear Regression.
Cross-validation results indicate consistent performance across multiple folds.

### Future Enhancements
Improve model performance with advanced algorithms like XGBoost.
Include additional features like property age, nearby amenities, and distance from key locations.
Integrate a user-friendly front-end interface.

### Contact
If you have any questions or want to collaborate, feel free to contact me

