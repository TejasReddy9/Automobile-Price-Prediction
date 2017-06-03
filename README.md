# Automobile-Price-Prediction

#### This project is done in Microsoft Azure Machine Learning Studio


## Usage

To use the Automobile Price Prediction:

1. Open `main.py` and edit the json `data` with the automobile characteristics for which price is to be predicted

2. For batch input, you can use `main_batch.py`


## How is it developed

1. The raw data contains a lot of missing data. So, those columns in which a lot of data is missing is skipped. Even if a single data element is missing, we remove that whole row.
2. The features are extracted whose impact on price is observable, and which are not are discarded.
3. Our labels are `price`, and on the extracted data we do a 70% split as training data, and other 30% as testing data. This splitting is done on randomly shuffled data.
4. I have modelled this predicitive experiment in `Microsoft Azure Machine Learning Studio` using `Linear Regression` as initialising model.
5. By feeding this Regression algorithm along with the training data into a model which will be trained according to the features and behaviour in training data.
6. Now using this newly trained model and the testing data available, we make predictions for the testing data and stored in `scored labels` column and store it in a csv file.
7. According to these predictions, we compute the coefficient of determination and mean error values.
