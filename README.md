# Data Science Module 4 Project - Applying Classification Modeling
* Tara Rosen(nyc-mhtn-ds-0422019)
* Flatiron School
* For this module's project, you will answer a classification data science question using multiple models and present the results   of your project. In doing so, we want you to utilize all of the different tools we have learned over the course: data cleaning,   EDA, feature engineering/transformation, feature selection, hyperparameter tuning, and model evaluation.

## Process/Expectations

1. Clean up your data set so that you can perform an EDA.
2. Perform EDA to identify opportunities to create new features. 
3. Engineer new features.   
4. Perform some feature selection.
5. You must fit **four** models to your data and tune **at least two hyperparameters** per model. (**work in progress**)
6. Decide on which evaluation metric you think is most appropriate for your project, evaluate how well your models perform, and identify your best model.
7. Use the outputs of your different models, along with your EDA work, to provide insight to your original question.


## Project Background

![title](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_1.png)

I used the Austin Animal Dataset to evaluate animal intakes and outcomes in order to see if I could predict feline outcomes (live vs. euthanasia) and determine what features would be critical in reducing feline euthanasia rates in animal shelters. We were giving the option of using one of seven, relatively clean, provided datasets or finding our own dataset. As animal welfare is a passion of mine, I opted to focus on adoption rates in animal shelters and find my own dataset.

![dataset](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_2.png)

I needed to look at the number of intakes vs. the number of outakes via euthanasia or live. There were 37,650 feline intakes, 18,880 felines were transfered out to adoption partners and 18,770 felines were either adopted or euthanized.

![adop_euth](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_4.png)

The feature engineering process involved:

* Merging the intake and outcome databases
* Converting the age and time in shelter to specific buckets
* Converting intake and outcome dates to seasons
* Separating out coat and breed types 
* Dummying or making all features binary

The feature selection process included:

* F-test (filter method)
* Recursive Feature Elimination (wrapper method)
* Correlation Coefficient

Handling Class Imbalance:

* Oversampling: SMOTE
* Undersampling: Tomek's Links


Modeling included:

* Logistic Regression
* Decision Tree
* Bagged Trees
* Random Forest
* KNN

The modeling is still a work in progress but using Random Forest with upsampling - SMOTE, I achieved an accuracy of 95.29%. I also used forest.feature_importances_ to perform feature selection to find the most important features:

![for_feat](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_9.png)

It appears that significant predictors for whether a feline will be adopted or euthanized is whether or not a feline is spayed or neutured, whether they have a name and their intake condition.

 
![named](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_10.png)

![sp_ne](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_11.png)

Recommendations for moving forward to reduce euthanasia and increase adoptions in animal shelters:

![reccs](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_13.png)

![thanks_you](https://github.com/TaraRosen/mod4project_austin_animal_center_dataset/blob/master/images/aa_14.png)