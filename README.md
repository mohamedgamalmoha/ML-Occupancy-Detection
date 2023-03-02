# Occupancy Detection

## Project Description:
Using environmental variable data and machine learning methods, we seek to identify room occupancy. 
We are using the UCI ML Repository's Occupancy Detection Dataset for this. Here, the time-stamped images of environmental
factors including temperature, humidity, light, and CO2 are taken every minute to determine the ground truth occupancy. 
The use of an ML algorithm as opposed to a real-world PIR sensor will be cheaper and require no upkeep. This could be 
helpful in the HVAC industry (Heating, Ventilation, and Air Conditioning).

## Data Source
Three data sets are submitted, for training and testing. Ground-truth occupancy was obtained from time stamped pictures that were taken every minute.
For the journal publication, the processing R scripts can be found in:. [Data Link](https://archive.ics.uci.edu/ml/datasets/Occupancy+Detection+)

## Data Info

Dataset has the following columns:
- **date**: the datetime of collection, format as year-month-day hour:minute:second
- **Temperature**: room temperature in celsius
- **Humidity**: the percentage of humidity of the air
- **Light**: Intensity of illumination measured in lux
- **CO2**: co2 parts per million - ppm
- **HumidityRatio**:  Derived quantity from temperature and relative humidity, in kgwater-vapor/kg-air
- **Occupancy**: Categorical value 0 or 1, 0 for not occupied, 1 for occupied status


Here is a snapshot of the data

|         date         | Temperature | Humidity | Light  |   CO2   | HumidityRatio | Occupancy |
|:--------------------:|:-----------:|:--------:|:------:|:-------:|:-------------:|:---------:|
| 2015-02-04 17:51:00  |    23.18    | 27.2720  | 426.0  | 721.25  |   0.004793    |     1     |
| 2015-02-04 17:51:59  |    23.15    | 27.2675  | 429.5  | 714.00  |   0.004783    |     1     | 
| 2015-02-04 17:53:00  |    23.15    | 27.2450  | 426.0  | 713.50  |   0.004779    |     1     |
| 2015-02-04 17:54:00  |    23.15    | 27.2000  | 426.0  | 708.25  |   0.004772    |     1     |
| 2015-02-04 17:55:00  |    23.10    | 27.2000  | 426.0  | 704.50  |   0.004757    |     1     |

The date is **not important** columns, so it is dropped.

## Data Exploration
To explore more about data, the following questions need to be answered:
  - What is the distribution of Temperature column?
  - What is the distribution of Humidity column?
  - What is the distribution of Light column?
  - What is the distribution of CO2 column?
  - What is the distribution of HumidityRatio column?
  - What is the distribution of Occupancy column?
  - What is the correlation & distribution between all features together? 

## Data Preprocessing
  - Set up the data with required columns
  - Split data into train set & test set
  - Scaling using standard scaler

## Applying ML Methods  
### Logistic Regression 
   1. Fitting Logistic Regression Model
   2. Predict test data 1 & 2
   3. Accuracy score
   4. Classification report (precision, recall, f1-score)
   5. Confusion matrix & Heatmap
   6. ROC curve for 3 sets
### Linear Support Vector Classifier
   1. Fitting Linear Support Vector Classifier Model
   2. Predict test data 1 & 2
   3. Accuracy score
   4. Classification report (precision, recall, f1-score)
   5. Confusion matrix & Heatmap
   6. ROC curve for 3 sets
### Naive Bayes Classifier
   1. Fitting DecisionTreeClassifier Model
   2. Predict test data 1 & 2
   3. Accuracy score
   4. Classification report (precision, recall, f1-score)
   5. Confusion matrix & Heatmap
   6. ROC curve for 3 sets

## References
  - [link 1](https://www.kaggle.com/datasets/robmarkcole/occupancy-detection-data-set-uci)
  - [link 2](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_curve.html)

