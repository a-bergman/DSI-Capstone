# Problem Statement

Left ventricular dilation, also known as dilated cardiomyopathy, is the enlargement of the left ventricle as indicated by the volume of blood during the diastolic phase (when the ventricle fills with blood).  It is serious because the muscle wall thins and its ability to pump blood is reduced: the condition is a warning that a patient is at serious risk of developing congestive heart failure.  Being able to predict the end diastolic volume will aid cardiologists in deciding who needs further testing. A model could increase the efficiency by indicating which patients need to be send to MRI rather than having to send everyone to MRI.

To approach this problem we will use a regression model to predict the end diastolic volume.  To judge our model's performance, we will use the root mean squared error (RMSE) and the r<sup>2</sup> score.

-------

# Executive Summary

The cost of healthcare has been in the news because of how expensive it is in the United States and cardiac imaging is no exception.  The median price of a cardiac MRI in the New York area is $1,507, but that's not all: MRI scans are very claustrophobic and can take a long time to complete.  Given both the cost and unpleasantness of MRIs, we are hoping to have a model than can be extended to non-MRI based data: we want to be able to make a prediction from patient chart information that would allow a doctor to determine if a confirmational MRI is needed.

We began to search for cardiac data online, but we had difficulty getting the data we need because of how specific the data is.  We then began reaching out to cardiologists as a last resort to see if we would be able to get good data.  Luckily we were given a cardiac MRI data set by two doctors at New York Presbyterian Hospital.  The data we received was remarkably clean: only six columns had missing data and none had a huge amount of it.  Upon closer examination, the data was not entirely in the format we had initially expected: there were a total of four numeric columns and the other 44 were ordinal or nominal.

Most of the cleaning we had to do was reformating column headers (shortening the names, removing spaces, and making them lowercase), making sure that all ordinal data is numeric, i.e. on a numeric scale, and creating dummy columns.  During the process of cleaning, we noticed that some values in our ejection fraction did not make any sense and so we had to filter them out.  After filtering them out, we noticed that some of our misising data was removed which left us with only four columns with missing data.  Due to the pitfalls of imputation, we opted to use the pattern sub-model approach.  This divided our data set into a series of smaller sub-sets that we will use to model and make predictions.

Because we have so many columns in the data set, we felt it was necessary to engineer our features in a way that reduced the total number of them.  Because the vast majority of our values are `0`, we could not make interaction columns since that relies on multiplication.  Instead, we opted to used a cardiac segmentation diagram as a way to sum the individual segments; when modeling we use either the summed columns or the originals, never both.  We also had a column with a lognormal distribution, so we created a column containing the log values.

We will begin with a simple linear regression model,  evaluate it's performance on all possible combinations of features, and add complexity to the simple model to see what effect that has on our predictions.  Additionally, we will be make use of two non-linear models to see how they compare to the linear ones; we will also compare the effects of the possible combinations of features.


[Source](https://www.newchoicehealth.com/places/new-york/new-york/mri/cardiac-mri]) for the median price.

-------

# Concerns

While the data overall is good data, there were concerns that cropped up.  Firstly, we were limited by HIPPA: _any_ potentially indentifying information was removed from the data.  Identifying information includes any kind of ID number and most demographic information, but also other diseases or conditions that a subject might have; such information may be co-morbid with increased heart size and could actually increase the performance of the model.  While the data had a full 48 features, it did not have as much information as we expected it to: height, weight, BMI/BSA, and numbers for cholesterol and blood pressure were absent.  Finally, our primary concern were errors in the data: the data was based off of MRI measurements, but they were recorded by humans.  Having an individual record measurements opens the window to data entry errors: we actually observed that in our ejection fraction feature that there are measurements of >100%, which is impossible especially given that the measurement is machine generated.  There was nothing that we could do about it, but we did bring it to the attention of the cardiologists.  We have concerns that other parts of the data might be incorrect, but we have not found anything else glaringly incorrect.

-------

# Conclusions

We chose two models because based off of our metrics, residual plots, and prediction plots because of the types of models we used.  Our best performing model was a random forest regressor, but because that is a black box method we felt the need to also select a model that we could interpret.  For that reason, we chose a second model that we could interpret.  We ended up choosing:


- A random forest model with our engineered columns for performance


- An XGBoost model also with our engineered columns for interpretability.

The models were not overfit at all: the models had metric scores for the train and test data that were virtually identical and both had very high R<sup>2</sup> scores.  However to assure that the R<sup>2</sup> score was not inflated by the number of columns, we also calculated and adjusted R<sup>2</sup> score and found that both scores were also virtually identical.


-----

# Next Steps


Knowing that we can predict the end diastolic volume with a good degree of accuracy, we want to try to get data from actual patient records: it's all well and good to predict the end diastolic volume from an existing MRI, but we are aiming to help reduce the cost to the health care system.  We are anticipating that it will be difficult to do so because of HIPPA, but we feel that using data from charts is the most sensible step forward.

In terms of modeling, we would like to continue optimizing the random forest and XGBoosting models to make them even more accurate; doing so entails simply further experimentation with the hyperparameters.  We also would like to implement other boosting models as well as an extra-trees model  to get a broader sense of what does and does not work with this type of data.  Another area we would like to work further on is the interpretability of the random forest model: there is a library call PDPbox that would allow for us to interpret the relationships between feature importance and the generated predictions.

Feature engineering also is an area where we would like to spend more time in.  While we were able to develop a new way of grouping the columns, we feel that further developing ways of representing the columns could improve performance as well: now that we know which features have high coefficients, we want to try emphasizing those columns as well.

-----

# Acknowledgments

We want to thank Drs. Jonathan Weinsaft and Jonathan Kochav from New York Presbyterian Hospital-Weill Cornell Medical Center for allowing me to use their clinical data for this project.