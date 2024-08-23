# online-gaming-behavior-eda
Phase 3 project

This project looks at online gaming behavior, in terms of levels of engagement. A descriptive analysis and inferential analysis are included together in one notebook. A technical modeling notebook makes up the other file. 

## Descriptive Analysis Questions
### 1. Do Males or Females have a higher Engagement Level?
### 2. How does engagement level break up vs. Play Time Hours?
### 3. Do Males or Females have a higher average played time?
### 4. What are the most played game genres based off this dataset?
### 5. What are the typical game genres played, and which is played the most?
### 6. How are the age brackets (15-24, 25-34, 35-44, 45+) represented across Male and Females?
### 7. What are the typical difficulty levels for games played, and which is played the most?
### 8. Which of those difficulty levels are played the most (Play Time Hours)?

## Inferential Analysis Questions
### 1. Is there any significant difference in the types of difficulty games Males play vs. Women?
### 2. Is there a link between Game Genre and Engagement Level?
### 3. Does Time Played significantly impact enagement level?
### 4. Does age impact time played?

For this technical modeling, I wanted to take a widespread approach and then narrow down my focus. I ran a quick cleaning of the data as I did in the previous notebook with a few alterations. I also created dummy columns for the categorical features to be able to scale them better. Once the data was cleaned it was time to run through a smörgåsbord of models. 

Since our target is categorical "EngagementLevel" the focus would be on classification models. To get as best of a spread of models we employed 7 models: Logistic Regression, Random Forest, SVM, KNN, Naive Bayes, Decision Tree, and Gradient Boosting. After the first round, Gradient Boosting, Random Forest, and SVM came out on top as the most accurate.

I made sure to rerun them all using a Pipeline and invoking StandardScaler. Doing this helped to work around data leakage. I got close the same results on the main 3 noted above. I decided that I would just go with the highest accuracy score and that was Gradient Boosting.

Once locked in, I employed a longer model run using a large parameter grid, for GridSearchCV and a decent number of cross evaluations. I was able to go from 87.86% to 88.14% accuracy rating.

This would be the area to continuing find tuning, and will do so in the future. 