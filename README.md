# Handling Big-p, Little-n in Machine Learning

This is an article stating how to solve Machine Learning Problems with small number of samples and high number of features.

## Problems with p>>n problems

A major problem while dealing with such datasets is that the machine learning model tends to overfit the training dataset.
Given the lack of samples, most models are unable to generalize and instead learn the statistical noise in the training data. This makes the model perform well on the training dataset but perform poorly on new examples from the problem domain. 

This is also a hard problem to diagnose, as the lack of samples does not allow for a test or validation dataset by which model overfitting can be evaluated. Hence, we often use leave-one-out style cross-validation (LOOCV) when evaluating models on p >> n problems.
There are many ways to approach the problem. Let's discuss some of them:

## Feature Selection
Feature Selection is the method of removing irrelevant and redundant features of your model by using only relevant data and getting rid of noise in data, without affecting the learning performance.

Common techniques include filter methods that select features based on their statistical relationship to the target variable (e.g. correlation), and wrapper methods that select features based on their contribution to a model when predicting the target variable (e.g. RFE).

**Note**: Feature Selection is one of the most important steps for a classifier when p>>n.

## Projection Methods
Principle Component Analysis(PCA) is an adaptive data analysis technique used for reducing the dimensionality of large datasets, increasing interpretability while minimizing information and reconstruction losses. In machine learning terms, it is used to reduce the number of parameters based on how much they contribute to predicting the output so that they can be represented graphically in a 2D/3D plot.

Projection Perspective is a technique used in PCA that further minimizes the data reconstruction cost. Data reconstruction simply means reducing the data point in higher dimensions to lower dimensions where it is easily interpretable. 
They are often used for visualization, although the dimensionality reduction nature of the techniques may also make them useful as a data transform to reduce the number of predictors.
## Regularization
Standard machine learning algorithms may be adapted to use regularization during the training process.
Regularization is a technique to prevent the model from overfitting by adding extra information to it. In regularization, we reduce the magnitude of features by keeping the same number of features.
This can act as a type of automatic feature selection during training and may involve augmenting existing models (e.g regularized linear regression and regularized logistic regression) or the use of specialized methods such as LARS and LASSO.

## Conclusion
Different methods regarding Handling Big-p, Little-n problems have been discussed. None of them can be called a best method. We need to conduct different experiments in order to test a suite of different methods.
