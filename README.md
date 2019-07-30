# Problem Statement

Left ventricular dilation, also known as dilated cardiomyopathy, simply put is the enlargement of the left ventricle as determined by the volume of blood in the left ventricle during the heart's diastolic phase.  It is serious because the muscle wall thins and its ability to pump blood out of the heart is reduced: the condition can contribute to serious caridac conditions such as clots, arrythmias, valvular disease, and congestive heart failure.  Prediction of this condition would give a physician warning that a subject needs close monitoring. 

The goal of this project is to classify who is at-risk of and who has left ventricular dilation based off of cardiac MRI and patient biometric measurements.  (I'm not entirely sure what model(s) I'm going to be using yet, I'm going to try to get office hours with Matt on Friday or Sunday.)

Because the data is unbalanced, I will use multiple metrics that are suited for unbalanced data:

* Sensitivity
* Specificity
* ROC-AUC Score
* [Balanced Accuracy](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html#sklearn.metrics.balanced_accuracy_score)
* [F1 Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html#sklearn.metrics.f1_score)
* [Fowlkes-Mallow Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.fowlkes_mallows_score.html)
* [Jaccard Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.jaccard_score.html)