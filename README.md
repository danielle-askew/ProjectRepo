![COVID](Resources/COVID_19.jpg)

# Topic: COVID19 Analysis at the Colorado County Level

## Summary
Our project used machine learning to determine if a Colorado county was likely to have a higher Covid-19 infection rate than the state average. Using the Decision Tree and Random Forest Algorithms, our model included features such as vaccination rates and social vulnerability index scores. While our models both obtained an encouraging accuracy score of 69%, we believe additional data points would be necessary to make a more robust model.

## Communication Protocols
* The Team will coordinate using a combination of Slack, Zoom Meetings during Monday and Wednesday classes, and additional meetings as-needed. We will use a Google Document for tracking meeting notes.

**Preprocessing and Machine Learning**

* This data will be consolidated into a database and the variables will be applied to a Machine Learning model to predict whether a specific county is likely to have a COVID Outbreak that exceeds the State or National Average. 
**Analysis, Presentation, and Visualization**

## Technology 

* Data is collected and preprocessed in `Jupyter Notebook` using `Pandas` and `Python`.

* Preprocessed data is connected and imported into `Postgres` using `pgAdmin` and AWS.
* The database is then connected to the Machine Learning model that has been created using 'Python', 'Pandas', and `Jupyter Notebook`
* The presentation will be displayed via `Google Slides`, as well as, an interactive webpage hosted by `Tableau Public` using `HTML`, `CSS` and `Javascript`.

## Visualization & Dashboard

* Dashboard [Storyboard](https://docs.google.com/presentation/d/1dCde1OCeyl3IB1D-QORw7h_S3HN5e1TztJYZq71IYIo/edit?usp=sharing) & blueprint. 
* [Dashboard](https://public.tableau.com/shared/H3Q25244H?:display_count=n&:origin=viz_share_link).

## Presentation 
* [Presentation Link](https://docs.google.com/presentation/d/12rbSZus9Fq7tq2jcaFw_y1p1-sv5cmX0l--q5vLJ2IA/edit?usp=sharing).

## Database ##

Our collective database was created in PostgreSQL (PGadmin), and connected using AWS.
* Preprocessed data is connected and imported into `Postgres` using `pgAdmin`.
* The database is then connected to the Machine Learning model that has been created using `Jupyter Notebook`
* The presentation will be displayed via `Google Slides`, as well as, an interactive webpage hosted by `Tableau Public` using `HTML`, `CSS` and `Javascript`

Additionally, the database meets all of the criteria requested for this unit's deliverables. 


## Machine Learning Model ##

In this machine learning analysis, we look to explore the relationship of vaccination rate and poplulation density by County in Colorado.

**ML Goal:** Explore the relationship of COVID Vaccinations and Population Density’s Impact on Infection Rates.

**Implications:**  We hope that by finding key variables that contribute to whether an area is likely or unlikely to experience an elevated COVID 19 infection rate by comparing  demographics to geographic data such as average percentage of completed vacctions and two week outbreaks that we can define infection trends ahead of time.

### Preliminary Feature Engineering, Feature Selection, and Decision-Making Process

**Target:** Whether an area is likely to or unlikely to experience an elevated COVID infection rate. 

**Features:** Demographic Data such as vaccination and outbreaks. 

### *Training and Testing Sets*
The dataset is split into training and testing sets. The model uses the training dataset to learn from it. It then uses the testing dataset to assess its performance. If we were to use the entire dataset to train the model, we wouldn't know how well the model will perform when it encounters unseen data. We use the SciKit Learn Library to split, train, and test the data.

### *Model Choice: Limitations and Benefits*
Because we are relating many variables, we will utilize both a Supervised Decision Tree and Random Forest Machine Learning Model. Supervised Machine Learning deals with labeled datasets. This approach is appropriate for this project because we will use current infection data to run predictions on future unknown datasets.

- Decision Tree Benefits: One of the most interpretable models, as they provide a clear representation of how the model works. Easy to classify or label objects by asking a series of questions designed to zero in on the true answer.
Decision Tree Drawbacks: Can become very complex and very deep, depending on how many questions have to be answered. Deep and complex trees tend to overfit to the data and do not generalize well.

- Random Forest Benefits: Instead of having a single, complex tree like the ones created by decision trees, a random forest algorithm will sample the data and build several smaller, simpler decision trees. Each tree is simpler because it is built from a random subset of features. Random forest algorithms are beneficial because they are robust against overfitting as all of those weak learners are trained on different pieces of the data, can be used to rank the importance of input variables in a natural way, can handle thousands of input variables without variable deletion, are robust to outliers and nonlinear data and run efficiently on large datasets.
Random Forest Drawbacks: The main limitation of random forest is that a large number of trees can make the algorithm too slow and ineffective for real-time predictions. In general, these algorithms are fast to train, but quite slow to create predictions once they are trained.

### *Model Results* 
* Accuracy: Our models showed different levels of accuracy in our undersampling piece we recieved an accuracy of 78.5% and 81.25% in the Logistic Regression.  
Our Supervised Machine Learning dataset contained binary outcomes, the accuracy of the predictions can be further analyzed by viewing the Confusion Matrices for the two models.

* Precision: Precision, also known as positive predictive value (PPV), is a measure of how likely that a Predicted Positive is a True Positive. Precision is obtained by dividing the number of true positives (TP) by the number of all positives (i.e., the sum of true positives and false positives, or TP + FP). For our models below, both the Decision Tree and Random Forest achieved a Precision score of .67. This means that out of 100 predicted positives, 67 were True Positives.

* Sensitivty/Recall: We can assess a model's performance is with sensitivity/recall. Sensitivity is a measure of how many True Positives were correctly predicted. For our models, both the Decision Tree and Random Forest achieved a Recall Score of .67. 

* F1 Score - Tradeoff Between Precision and Sensitivity: The F1 score is a pronounced imbalance between sensitivity and precision. For our models below, both models achieved a high F1 Score of .67.

![Confusion Matrix](Resources/CM.jpg)


## Project Team Members
* Mike Tuckerson 
* Jordan Brickman
* Adam Magyar
* Danielle Askew 
