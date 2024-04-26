# User Analytics in the Telecommunication Industry

This project focuses on analyzing user engagement and experience in the telecommunication industry, aiming to understand customer satisfaction deeply. The analysis involves various tasks, including clustering, scoring user engagement and experience, predicting satisfaction scores, and deploying a regression model.

## Task 1 - Streamlit Source Code Overview

### Overview
The Streamlit source code is structured in a modular and organized manner, following best practices for Python development. It utilizes advanced Python programming techniques such as decorators, docstrings, logging, and error handling. Unit and integration tests are written using the pytest framework. The codebase also relies on additional packages listed in the requirements.txt file.

### Observations
- The codebase uses @property and other custom decorators for managing properties and behaviors.
- Docstrings are extensively used to document functions, classes, and modules, providing clear explanations of their purpose and usage.
- Error handling is implemented using try-except blocks, ensuring graceful handling of exceptions and providing informative error messages.

## Task 2 to 4 - Engagement, Experience, and Satisfaction Analysis

### Engagement and Experience Analysis
- User engagement and experience are analyzed using clustering techniques (e.g., KMeans).
- Engagement and experience scores are calculated for each user based on their data points and cluster centroids.
- Satisfaction scores are derived as the average of engagement and experience scores.

### Regression Model
- A regression model is built to predict satisfaction scores based on user data.
- Various regression techniques can be applied, such as Linear Regression or Random Forest Regression.

### K-Means Clustering
- K-Means clustering is performed on engagement and experience scores to identify user segments.
- The number of clusters (k) is chosen based on the desired segmentation.

## Task 5.6 - Model Deployment Tracking

### Model Deployment
- The regression model can be deployed using MLflow or similar ML Ops tools.
- Model versions, parameters, metrics, and artifacts are tracked for monitoring and reproducibility.

### Example MLflow Usage
```python
import mlflow

# Start MLflow run
with mlflow.start_run():
    # Log model parameters
    mlflow.log_param("model_type", "Linear Regression")
    
    # Train the regression model
    regression_model = LinearRegression()
    regression_model.fit(X_train, y_train)
    
    # Log model metrics
    mlflow.log_metric("mean_squared_error", mean_squared_error(y_test, y_pred))
    
    # Log model artifact (trained model)
    mlflow.sklearn.log_model(regression_model, "regression_model")
