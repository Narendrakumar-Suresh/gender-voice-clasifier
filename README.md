# gender-voice-clasifier
This project implements a gender classification system based on voice analysis using a dataset in CSV format. The model achieves an accuracy score of 97%.

**Libraries Used:**
scikit-learn (https://scikit-learn.org/),
pandas (https://pandas.pydata.org/),
joblib (https://joblib.readthedocs.io/)

**Data Description:**
The project utilizes a CSV file containing voice data with the following attributes:
meanfreq: Mean frequency of the voice signal (kHz).
sd: Standard deviation of the frequency (kHz).
Q25: First quartile of the frequency distribution (kHz).
Q75: Third quartile of the frequency distribution (kHz).
IQR: Interquartile range (difference between Q75 and Q ۲۵) - characterizes the middle 50% of the data (kHz).
akew: Skewness of the frequency distribution.
kurt: Kurtosis of the frequency distribution.
sp.ent: Spectral entropy - a measure of the randomness of the frequency spectrum.
centroid: Frequency centroid of the voice signal (kHz).
meanfun: Mean of the fundamental frequency (pitch) across the signal (kHz).
minfun: Minimum fundamental frequency (pitch) measured (kHz).
maxfun: Maximum fundamental frequency (pitch) measured (kHz).
dfrange: Range of the fundamental frequency (kHz).
These attributes likely correspond to Mel-frequency cepstral coefficients (MFCCs) and pitch information extracted from the voice samples. They capture various statistical properties of the frequency domain, which can be informative for differentiating male and female voices.

_**Project Overview**_

**Data Preprocessing:**
Load the voice data from the CSV file using pandas.
Explore the data to understand its distribution and identify any missing values or outliers.
Preprocess the features for machine learning, potentially including scaling or normalization.

**Model Training:**
Split the data into training and testing sets.
Train a machine learning model, such as Support Vector Machine (SVM) or Random Forest, to classify voices as male or female based on the extracted features.

**Model Evaluation:**
Evaluate the trained model's performance on the testing set using metrics like accuracy score.
An accuracy score of 97% indicates the model correctly classifies 97% of voices in the testing set.

**Model Saving :**
Use joblib to save the trained model for future use.
This allows you to use the model for gender classification on new voice samples without retraining.
