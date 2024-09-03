# Driving Behaviour

Driving behaviour is a ML/data science project I did in order to learn and practice different machine learning tools, as well as practicing cleaning, reading, and training on data. Specifically, I aimed to predict a person's driving behaviour (aggressive, normal, or slow) based on given accelerometer and gyroscope data. 

## Data Collection

The data is from a public collection on Kaggle, and collection methodologies are outlined in the [team's paper](https://rochi.utcluj.ro/articole/10/RoCHI2022-Cojocaru-I-1.pdf). 

## Process

I first began by creating my own features from the data, being the magnitudes of acceleration and gyroscopic data. I did this since the data was missing information on the overall change in acceleration and gyroscope. After splitting up the classes (AGGRESSIVE, NORMAL, SLOW) into their own pandas dataframes, I plotted their accel/gyro data against time.

## KNN vs Random Forest Classifiers

The first classification method I chose was K-nearest neighbors as I had learned it in one of my university classes. Next, I decided to create and use a Random Forest as it seems to be a very popular classification method. 

According to the classification reports and confusion matrices, the random forest was able to classify accelerometer and gyro data as aggressive, normal, and slow slightly better than the KNN classifier. In particular, the KNN had a 37% accuracy, whereas the random forest had about 41% accuracy. 

## Future Improvements and Exploration

It is very possible that either classification method could be improved using different k-values or n-estimators. Improvement could also be made by calculating more features/columns of data. For example, it may be possible to look at the derivative/change in acceleration and gyroscope relative to the values of neighboring timestamps. This way, we may see a correlation between frequent accel/gyro changes and aggressive/slow driving. 
