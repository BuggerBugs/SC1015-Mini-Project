# SC1015 Mini Project - Song Popularity Predictor :musical_score::musical_score:
## About
This is our Mini-Project for SC1015 ( Introduction to Data Science and Artificial Intelligence ) which focuses on songs from the [Song Popularity Dataset from Kaggle](https://www.kaggle.com/datasets/yasserh/song-popularity-dataset).
Here is an overview of the source code: 
1. [Data Preparation](https://github.com/BuggerBugs/SC1015-Mini-Project/blob/main/SC1015%20Mini-Project%20Files/1.%20Data_Preparation.ipynb)
2. [Data Visualization](https://github.com/BuggerBugs/SC1015-Mini-Project/blob/main/SC1015%20Mini-Project%20Files/2.%20Exploratory%20Analysis.ipynb)
3. [Regression Models](https://github.com/BuggerBugs/SC1015-Mini-Project/blob/main/SC1015%20Mini-Project%20Files/3.%20Numeric_Prediction.ipynb)
4. [Classification Models](https://github.com/BuggerBugs/SC1015-Mini-Project/blob/main/SC1015%20Mini-Project%20Files/4.%20Categorical_Prediction.ipynb)
5. [Results Comparision](https://github.com/BuggerBugs/SC1015-Mini-Project/blob/main/SC1015%20Mini-Project%20Files/5.%20Results_Comparison.ipynb)

## Contributors 
- @s-27-b (Bhargavi) - Data Visualisation, Regression Models
* @BuggerBugs (Qi Yang) - Data Preparation, Classification Models, Results Comparision

## Problem Definition 
- Musical Artists sometimes have a limit on the number of songs they can release in an album. Being able to predict which ones will do better can help them decide which songs to include in their album for a **HIT** !!!
* Our aim is to come up with the best model to predict how popular a song could be (popularity category) based on it's audio features - song duration, acousticness, danceability, energy, instrumentalness, key, liveness, loudness, audio mode, speechiness, tempo, time signature and audio valence.

## Models Used 
Originally, the song popularity scores are from 0-100. We identified 4 categories, and want to predict the song's popularity category. Here are the popularity scores and their corresponding popularity categories: {0-25 : CAT 0, 26-50 : CAT 1 , 51-75 : CAT 2, 76-100 : CAT 3}

We used 2 approaches to find the best model. 

Firstly, we used regression to predict the numerical value of the popularity score, then convert that predicted score into the popularity category of 0-3, and check against the actual song popularity category.

The models we used for **regression** are :
1. Multi-Variate Linear Regression 
2. Stepwise Linear Regression 
3. Support Vector Regression 
4. K-nearest Neighbours Regression 

Our second approach is to categorise all the song popularity scores into categories first, then train our classification models on these popularity categories to predict the song popularity category.

The models we used for **classification** are :
1. Decision Trees 
2. Random Forest 
3. Artificial Neural Networks

## Conclusions 
* The best model to predict song popularity for this dataset is Random Forest (50.6% Accuracy)
- Regression Models and Non-Oversampled Classification Models are not suitable in predicting song popularities from the lowest and highest categories in this dataset.
* It is difficult to get a model with high accuracy to predict what song people would like, or dislike.
* SMOTE Oversampling can reduce bias of models towards song popularity category 2 (the majority class), but reduces overall model accuracy for models trained on this dataset.
 
* A larger and less imbalanced dataset could be needed to reduce bias, as well as noise from oversampling, and ultimately train better performing models for artistes to utilise and decide which songs to include in their albums, or which ones to leave out!

## What did we learn from this project?
* One hot encoding and dummy variable trap
- Different models for regression - Stepwise, KNN, SVM.
* SMOTE Oversampling technique
- Different models for classification - Random Forest, Neural Networks
* Hyperparameter optimization with keras tuner
- Creating repositories and collaborating on Github

## References
* https://towardsdatascience.com/a-beginner-friendly-explanation-of-how-neural-networks-work-55064db60df4
* https://machinelearningmastery.com/multi-class-imbalanced-classification/
* https://www.youtube.com/watch?v=6Nf1x7qThR8
* https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
* https://stackoverflow.com/questions/45053238/how-to-get-all-confusion-matrix-terminologies-tpr-fpr-tnr-fnr-for-a-multi-c
* https://www.analyticsvidhya.com/blog/2021/10/implementing-artificial-neural-networkclassification-in-python-from-scratch/
* https://www.youtube.com/watch?v=9yl6-HEY7_s&t=376s

