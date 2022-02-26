# Agriculture-Recommender-System
Random Forest Classifier used to recommend ideal crops to grow based on WeatherAPI data.

Libraries Used:
  - Sci-kit learn
  - Seaborn
  - Matplotlib

Implementation:
  - Dataset:
    - Dataset imported from Kaggle: https://www.kaggle.com/atharvaingle/crop-recommendation-dataset
    - Dataset contains the following information (8 Columns):
      - N - the ratio of Nitrogen content in the soil
      - P - the ratio of Phosphorous content in the soil
      - K - the ratio of Potassium content in the soil
      - temperature - the temperature in degrees Celsius
      - humidity - relative humidity in %
      - pH - pH value of the soil
      - rainfall - rainfall in mm
      - label - the name of the ideal crop to be produced
    - The first 7 columns will be used as the input features of the Random Forest Classifies model.
    - The label column will be used as the output of the model.
    - The dataset is split 80/20 as training and testing subsets respectively.
  - Data Preprocessing:
    - Missing data will be fixed using data imputation.
    - Datapoints are normalized. (Note: This step is optional since Random Forest is a tree-based model and feature scaling is not a requirement).
      - Training the model with or without normalizing the data yeilded no significant change in the final accuracy of the model.
  - Data Analysis and Visualization:
    - Matplotlib and Seaborn figures are used to visualize the data and extract any correlations between features and make inferences.
  - Hyperparameter Tuning:
    - Hyperparameters are optimized using the GridSearchCV algorithm.
  - Model Training:
    - The model is training using the optimal hyperparamters obtained from the GridSearchCV algorithm.
    - The model will be trained to predict the ideal crop to grow given the following parameters: (N, P, K, temperature, humidity, pH, rainfall).
  - WeatherAPI:
    - Historical location based weather data can be obtained from the WeatherAPI from weatherapi.com.
  - Example Application: 
    - A farmer will input their region and soil composition into the model, the WeatherAPI will pull historical weather data and feed it into the Random Tree Forest Classifier. The classifier will suggest the ideal crop to grow in the region.   
