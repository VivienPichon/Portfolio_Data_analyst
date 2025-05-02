# Portfolio3_ML_Algorithm_Optimization_and_Comparison

Here I test and optimize several machine learning algorithm to predict continuous and categorical values. You can check the full code in the [notebook 1](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/clean/Project3_Machine_Learning_Optimization/Notebook_1_analysis_and_model_choice.ipynb) and [notebook 2](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/clean/Project3_Machine_Learning_Optimization/Notebook_2_note_validity_prediction.ipynb). The slides I used for my defense are available [here](https://github.com/VivienPichon/Portfolio_Data_analyst/blob/clean/Project3_Machine_Learning_Optimization/Results_presentation_slides.pdf).

In this portfolio I use several supervised blackbox ML models, a supervised glassbox model and an unsupervised blackbox model. 
Hyperparameter optimization is made with a 2-step Bayeseian search. 

## Roleplay context

In this exercise, I am asked by the French Bureau of Counterfeight Control to set up a machine learning tool to detect couterfeight notes based on geometric data. 
To do so I am given a table containing the measurements (diagonal, height_left, height_right, margin_low, margin_height and length) of 1500 notes in millimeters as well as an annotation to know if each is genuine or counterfeight.

My first task was to fill the margin_low column as it had missing values.
The second task was to test several classifier ML algorithm to find which one is the best at separating genuine from couterfeight notes.
Following this, I am asked to create another notebook, which contains an app that uses the best algorithm I found to predict the validity of a new dataset.

## Information on the exercise

### Fill missing values

I was asked to use a multiple linear regression to predict the missing values. The data was not adapted (none of the assumptions was met) so the algorithm performed poorly.
I decided to use instead a Random Forest regressor, which performed much better (although not greatly) after optimization.

### Note validity prediction

I tested the following calssification algorithms:

- K-Nearest-Neighbors
- Random Forest
- Extreme Gradient Boosting
- Logistic regression
- Explainable boosting (glassbox model)
- Gaussian Mixture Model (unsupervised learning)

When optimization was relevant, it was made to maximize the f1 metric, which finds a balance between the number of False Negative and False Positive detected in the validation set.

After optimization, all the algorithm performed strongly with a very low number of errors (1 error for the GMM, 3 errors for the Explainable boosting, 2 errors for the rest).
The algorithms which were fitted the most quickly were the KNN and the GMM. We then used the GMM for the prediction on new data.
