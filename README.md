# Taxi Fare Prediction Regression

# Business Understanding

The stand-out objective of the project is to produce a predictive model that can accurately return the taxi fares for all possible journeys and new trips in the local Bournemouth and Dorset region. The requirement for the model is its accuracy in predicting a fare as close to the actual price as possible. The need for this precision is indisputable as it could deter possible customers if the algorithm overcharges customers for journeys. Currently, the data provided is raw and little correlation can be observed between the attributes, hence the need for a model with useable features to provide a level of intelligence to the predictive algorithm. 10,000 journeys were observed within two weeks, shown in the dataset, highlighting the necessity for an automated system; as it would be near impossible to predict new taxi journeys manually. This project will be completed in accordance with the CRISP-DM methodology.

# Data Understanding

Throughout this project, charts have been created and other data analysis tools used, to better visualise the correlation within the raw data, to help understand how the model can be trained to have a higher accuracy when predicting the label. The importance of finding these correlations in data mean that redundant data can be ignored, to a certain extent, while more specific helpful information can be picked up and used.

# Data Preparation and Modelling

In terms of preprocessing this project was started by cleaning the dataset before any changes could be made; in order to ensure the data being worked with is as accurate and viable as possible. To make certain that the datatypes of the attributes remain the same throughout, the conversion of all values to floats have be made. In addition, the dataset now also has no null values.

Here the creation of multiple features will be extrapolated from the raw data, trying to convert it to more meaningful information. The feature engineering will be geared towards the improvement of the models, to see what works best.

Error Analysis will also be performed to corroborate the validity of the data with no extreme outliers or performance reducing instances.

# Evaluation and Deployment

A final score of ~1.58841 RMSE was achieved as the lowest RMSE from the Kaggle submissions. This score meets the accuracy objective that the project was heavily reliant on. During the selection of the models, two of them stood out, these were Random Forest and MLP Regressor algorithms. To find out which model would be best to implement a number of Yellowbrick regressor visualisations were created. It was made apparent that the R-squared between the predicted values of the train and test data was closer, when ran through a MLP regressor whereas the Random Forest Regressor had larger variance. It was also observed that the CV score and Training Score was at its best with 9 features implemented.

In terms of deployability there was a minimal sacrifice of training speed to better the accuracy of the fare prediction. However, it is still quick enough to prevent any major disruptions to the companys customers. MLPRegressor kept the two main objectives of the company in mind, speed and accuracy.

A common pattern was found that prediction errors were more likely to occur in the model when the fare was over £30. This was believed to be because there are less fares at higher prices making it more difficult for the model to learn, then apply and predict.

It was observed that the best accuracy was achieved when 100% train data was used on the model. Although, an 80/20 ratio worked best when training and testing the model algorithms.

Overall, the boosting regressor models, neural network model and tree based models worked best, they seemed to follow the true trend of the learned data, these could be compared to the linear regression model that could not handle the complex nature of our data. The best way to evaluate was the models was the accuracy with the MAE and RMSE scores, which were printed alongside all our implemented models.

# Data Analysis and evaluation of our new features

During the data understanding a few question were left unanswered due to the vague nature of the raw data. Therefore, a data analysis was to be performed to better understand the correlation between the newly implemented features.

It is now seen that the correlation between fare and the features is greater than the raw features of the dataset. It was made apparent that the addition of night trips was important and well correlated while other features showed less correlation highlighting which attributes may affect the model for better or worse.

# Feature Engineering for the Hold out test
**Reassigning the attributes to hold out for the test.csv file**

It is important to make sure both the train dataset and test dataset match up, including all the same data types and attribute names, to prevent any mismatch when the predictive model tries to perform on the test data.
