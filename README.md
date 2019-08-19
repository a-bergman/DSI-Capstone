# Problem Statement

Left ventricular dilation, also known as dilated cardiomyopathy, simply put is the enlargement of the left ventricle as determined by the volume of blood in the left ventricle during the heart's diastolic phase.  It is serious because the muscle wall thins and its ability to pump blood out of the heart is reduced: the condition is a warning that an individual is severely at risk of developing congestive heart failure.  Being able to predict the end diastolic volume will aid cardiologists in deciding who needs further test; a patient would never be given therapy without having an image taken.  Thus a model could increase the efficiency of medical teams and reduce hospital costs.

To approach this problem we will use a regression model to predict the end diastolic volume.  To judge our model's performance, we will use the root mean squared error (MRSE) and the r<sup>2</sup> score.  Within the data itself there are three classes: normal, at-risk, and high.  In addition to using the two metrics I mentioned, I will compare my regression model's predictions against the actual classifications in my data set.  Doing that extra step allows for an additional measure of performance.

-------

# Executive Summary

The cost of healthcare has been in the news for the past couple of years because of how expensive medical testing and treatment is in the United States and cardiac imaging is no exception.  The median price of a cardiac MRI in the New York area is $1,507, but that's not all: MRI scans are very claustrophobic and can take a long time to complete.

[Source](https://www.newchoicehealth.com/places/new-york/new-york/mri/cardiac-mri]) for the median price.

-------

# Concerns

While the data overall is good data, there were concerns that cropped up.  Firstly, we were limited by HIPPA: _any_ potentially indentifying information was removed from the data.  Identifying information includes any kind of ID number and most demographic information, but also other diseases or conditions that a subject might have; such information may be co-morbid with increased heart size and could actually increase the performance of the model.  While the data had a full 48 features, it did not have as much information as we expected it to: height, weight, BMI/BSA, and numbers for cholesterol and blood pressure were absent.  Finally, our primary concern were errors in the data: the data was based off of MRI measurements, but they were recorded by humans.  Having an individual record measurements opens the window to data entry errors: we actually observed that in our ejection fraction feature that there are measurements of >100%, which is impossible especially given that the measurement is machine generated.  We are concerned that other data may be incorrect, but we have not found evidence to say that any other columns are incorrect.

-------

# Conclusions And 

-------

# Next Steps