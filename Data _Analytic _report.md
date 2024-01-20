
**Data Analysis Report: Student Performance Analysis**
Introduction:
This report presents the results of an analysis of student performance data. The objective of the analysis is to understand the factors influencing student grades and provide insights for educational improvement.

Data was uploaded to the postgres fileand new  record was added to that.

**Data Description:**
Dataset Size: 316 records

**Data Cleaning and Preprocessing:**

There were no missing values or duplicate values.

**Exploratory Data Analysis (EDA):**

Categorical variables were encoded get dummies from pandas.
2 Correaltion matrix were formed.One between the numeraical values and another between the whole data set after encoding.
![Correlation Matrix and Histograms](extracted_graphical_image.png)

A positive correlation was observed between final grades,study time,Mother's education and father's education.
Family size does not appear to significantly impact final grades.
Top 10 best column were used for feature Engineering.


**Feature Selection and Engineering:**

Selected features for modeling: failures, freetime, Walc, absences, G1, G2', Medu,
      , reason_reputation, 'schoolsup_no, absences,goout,age_M, sex_M.
3 Features were Engineered  and combined with other features to see the output for different Models.
/Users/yorkmacbook023/kanwalpreet-kaur-aml-student-regression/image.png



**Model Building and Evaluation:**
3 Models were selected to evaluate the performance.RandomForest,SVR and Gradient boost
All had R2 scores between.80 and.92 for all the 5 sets of Feature Engineering and for all the 3 Models. 

Applied a RandomForestRegression model to predict final grades (G3) hypertuned the model using GridSearch method and get the final results.
Model evaluation metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2).
RandomForestRegressor Results:
Mean Squared Error: 1.7621874999999998
Mean Absolute Error: 0.896875
R-squared: 0.9008731717365928
Root Mean Squared  Error: 0.9008731717365928

**Results and Interpretation:**

The most influential factors on student performance are previous Grades
Students who receive school support tend to have higher final grades.
Other Factors  which contribute much to student grades are failures and absences 
The model can be used to predict final grades based on the selected features.
Limitations and Assumptions:

Limited dataset size may not capture all factors influencing student performance.
Assumptions about data distribution and linearity were made for regression modeling.
Conclusion:
This analysis provides valuable insights into student performance factors. Addressing factors like study time and family support could potentially improve students' grades.

**Predicting G3 grades without previous semester results** 
For predicting the results without the previous grades used models XGBoost , KNN regressor and Ridge. these models didn't perform very well with any of teh fature sets. Features influencing the G3 without the previos grades are Abcesves, failures, Mother's job and daily alchol and weekend alchol.Overall performance was declined.When hypertuned KNN model , it performed a little better and got the final reuls as below:-
KNN Results:
Mean Squared Error: 15.41863036577915
Mean Absolute Error: 3.0380787051807685
R-squared: 0.13266895587129857
Root Mean Squared  Error: 0.13266895587129857


**Recommendations:**

Encourage students to allocate more time for studying.
Provide additional support to students with lower family support.
Collect more data to refine the analysis and modeling.

