# Music genre prediction
The goal of this project is developing a machine learning model that can **accurately classify the musical genre of a song** among the 15 possible genres. The dataset used is a public *Spotify* dataset, 
including song features, such as tempo, mode, key, energy etc. The focus of the project was on a thorough and rigorous approach, especially regarding the preprocessing steps. In the end,
12 models were tested.
This project was done as a semester-long project for the Machine Learning master's course in a team of three.
The project can be separated into following sections:
1. Exploratory data analysis - target class distribution, undertanding the meaning of each feature and their statistical behavior in the dataset, **PCA** and **clustering**
2. Data preprocessing
3. Model selection
4. Final results and conclusion - the report *Machine Learning Project Report.docx* includes all the project details, including the final result analysis and conclusion.

For the data preprocessing, a set of steps was taken to ensure highest possible data quality:
1. Missing values handling
2. Deduplication
3. Outlier detection
4. Feature extraction - e.g. *vocal density* and *vocal expression* from speechines, valence and instrumentalness
5. Feature Selection - based on **correlation** and **feature importance** gained from **Mutual Information** and **Random Forest**
6. Feature transformations - including normalization and type conversion
7. Imbalance - including **undersampling**, **oversampling**, and spliting a large target class in two based on duration

Model selection was done using **grid search with 5-fold cross-validation** and rating the models by the **F1** score, and accuracy.
The candidate models were: **Naive Bayes** as a baseline model, **Logistic Regression**, **LDA**, **QDA**, **KNN**, **Decision Trees**, **Random Forest**, **Extra Trees**, **SVM**, **MLP**, **Stacking** and **Voting**
with decision trees, MLP, random forest and MLP. The voting model came up with the highest F1 score of **66.50%** onthe test set. The highest scoring singular model was the Multi-layer Perceptron with an F1 score of **65.90%**.
