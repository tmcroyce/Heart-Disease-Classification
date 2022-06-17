## Project Overview:
The purpose of this project is to use categorical multiple machine learning models to solve a business problem.

My chosen problem is to see if I can predict heart disease from a variety of general factors. The business problem in this case is for a web application where, with just a few questions, an individual or their doctor could screen for the possibility that they have heart disease. 

## The Data

This project utilizes a dataset from kaggle: https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease

This dataset come from the CDC and is a major part of the Behavioral Risk Factor Surveillance System (BRFSS), which conducts annual telephone surveys to gather data on the health status of U.S. residents.

According to the CDC:
'Established in 1984 with 15 states, BRFSS now collects data in all 50 states as well as the District of Columbia and three U.S. territories. BRFSS completes more than 400,000 adult interviews each year, making it the largest continuously conducted health survey system in the world.'

## Describe Data

The data contains 18 variables and approximately 320,000 observations. 

The variables in the dataset include:
- 1. HeartDisease - Respondents that have ever reported having coronary heart disease (CHD) or myocardial infarction (MI)
- 2. Smoking (Question: Have you smoked at least 100 cigarettes in your entire life? [Note: 5 packs = 100 cigarettes])
- 3. AlcoholDrinking (Heavy drinkers (adult men having more than 14 drinks per week and adult women having more than 7 drinks per week)
- 4. Stroke - Has the individual had a stroke?
- 5. PhysicalHealth -ORDINAL Categorical Variable - (Now thinking about your physical health, which includes physical illness and injury, for how many days during the past 30 days was your physical health not good? (0-30 days)
- 6. MentalHealth - ORDINAL Categorical Variable - (Thinking about your mental health, for how many days during the past 30 days was your mental health not good? (0-30 days))
- 7. DiffWalking (Do you have serious difficulty walking or climbing stairs?)
- 8. Sex - Male or Female
- 9. AgeCategory - ORDINAL Categorical Variable (Fourteen-level age category)
- 10. Race
- 11. Diabetic - Yes/No/Borderline
- 12. PhysicalActivity - Adults who reported doing physical activity or exercise during the past 30 days other than their regular job
- 13. GenHealth - Is the individuals general health good / fair/ poor / very good / great?
- 14. Asthma - Yes/No
- 15. KidneyDisease - Yes/No
- 16. SkinCancer - Yes/No
- 17. SleepTime - How many hours per night do you sleep (Continuous Variable)
- 18. BMI - What is your body mass index

## Models Ran

Models ran included Random Forest, Extra Trees, Logistic Regression, XGBoost, Bagged Trees, KNN, and Decision Tree. 

## Conclusion

The Final Model is a Random Forest model, optimized by RandomizedSearchCV. 

The model's most important features, by far, were Age Category and General Health. 

These two features accounted for .45 of the total feature importance, between the two of them. 

The downsides of this model is it is one of the so-called "black box" models, which we can not read like we could a single decision tree model. This is still a better model, as the performance improvements are worth giving up some understanding of the specifics. 

In the future, I would like a larger set of variables, with more specific questions. While I know that the point of this dataset is to find what general questions can lead to specific results, it would be helpful to have more than 17 variables. It would also be interesting to see this same project done with more specific data, possibly medical data, to see what variables we need to achieve higher scores all around. 