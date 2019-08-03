# Problem Statement

Left ventricular dilation, also known as dilated cardiomyopathy, simply put is the enlargement of the left ventricle as determined by the volume of blood in the left ventricle during the heart's diastolic phase.  It is serious because the muscle wall thins and its ability to pump blood out of the heart is reduced: the condition can contribute to serious caridac conditions such as clots, arrythmias, valvular disease, and congestive heart failure.  Prediction of this condition would give a physician warning that a subject needs close monitoring. 

To approach this problem I will use a regression mode (not sure what type yet).

To judge my model's performance, I will use the root mean squared error (MRSE) and the $\r<\sup>2<\sup> score.  Within the data itself there are three classes: normal, at-risk, and high.  In addition to using the two metrics I mentioned, I will compare my regression model's predictions against the actual classifications in my data set.  Doing that extra step allows for an additional measure of performance.