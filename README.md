# Problem Statement

Left ventricular dilation, also known as dilated caridomyopathy, simply put is the enlargement of the left ventricle determined by the volume of blood in the left ventricle during the heart's diastolic phase.  The condition is serious because the muscle wall in the left ventricle thins and its ability to pump blood out of the heart is seriously impact: the condition contributes to serious caridac conditions such as clots, arrythmias, valvular disease, or congestive heart failure.  It is important for a physician to determine if a subject is at risk for or has ventricular dilation. 

The diagnosis is usually determined through MRI volume measurements, but not every physician has access to them.  The goal of this project is to predict who is at-risk of and who has left ventricular dilation as accurately possible but also in a way that minimizes false negatives.  I will approach this as a classification problem with three targets: normal, at-risk, and high.  By adding an at-risk category, I am hoping to identify subjects who need to closely monitored.

Because I want to be as accurate as I can and the data is very unbalanced, I will use multiple metrics that are suited for unbalanced data:

* [Balanced Accuracy] (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html#sklearn.metrics.balanced_accuracy_score)
* [F1 Score] (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html#sklearn.metrics.f1_score)
* [Fowlkes-Mallow Score] (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.fowlkes_mallows_score.html)
* [Jaccard Score] (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.jaccard_score.html)