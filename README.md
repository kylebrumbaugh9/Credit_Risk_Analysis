# Credit_Risk_Analysis

## Overview

### Purpose
The purpose of this analysis was to apply machine learning to evaluate credit card risk with a multitude of algorithms and machine learning models. In this analysis, I looked at RandomOverSampler, SMOTE, ClusterCentroids and SMOTEENN algorithms to look at oversampling, undersampling, and a combination. I also looked at BalancedRandomForestClassifier and EasyEnsembleClassifer machine learning models to predict credit risk. Then, I evaluated the results and have determined my recommendations in the summary section below

### Technology used

I used Jupyter notebook, the scikitlearn and imbalanced-learn libraries, as well as numpy, pandas, Path, and Counter. Most of the code itself is written in Python.


## Results

- RandomOverSampler
  - Balanced Accuracy Score - 0.6645
  - Precision Score - 0.01
  - Recall Score - 0.73
  - Explanation - RandomOverSampler was not very accurate, or precise, when determining whether or not a patient was high_risk. Furthermore, the F1 score was 0.02 which means that this was a poor attempt at assessing risk. The average precision score is 0.99 but it's only 0.01 when looking at predicting high risk, so that's why the 0.01 score is more accurate than the "average" of 0.99. I extend this logic through each other machine learning model. 
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222313129-315559fa-2b57-4976-ac2c-b375f2b2b0b9.png)

- SMOTE
  - Balanced Accuracy Score - 0.6487
  - Precision Score - 0.01 
  - Recall Score - 0.64
  - Explanation - the SMOTE oversampling algorithm was also not very accurate, or precise. Even more so, the recall or sensitivity was worse than the randomOverSampler as well. SMOTE. Overall, SMOTE did a poor job.
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222516387-b882f72e-5fc5-4a01-9fe0-be27142f9d5b.png)

- ClusterCentroids
  - Balanced Accuracy Score - 0.5364
  - Precision Score - 0.01
  - Recall Score - 0.66
  - Explanation - The ClusterCentroids undersampling algorithm also did a poor job and actually performed the worst of all the models. With an accuracy score around 50%, you'd be just as good off if you flipped a coin.
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222517024-48076b3a-a2a4-4647-8e46-8963eb0cbd4a.png)

- SMOTEENN
  - Balanced Accuracy Score - 0.6625
  - Precision Score - 0.01
  - Recall Score - 0.74
  - Explanation -  SMOTEENN's oversampling/undersampling method was very similar to the RandomOverSampler method. It performed tied for the best of the sampling algorithms. 
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222516794-efae546b-8094-4eec-9307-347db4a0d97c.png)

- BalancedRandomForestClassifier
  - Balanced Accuracy Score - 0.7665
  - Precision Score - 0.03
  - Recall Score - 0.64
  - Explanation - The BalancedRandomForestClassifier did notedly better than the sampling algorithms done prior. This was 3 times better at the Precision score and 10 percentage points better at Accuracy, but had a similar recall score. Overall, BalancedRandomForestClassifier was not entirely useless.
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222517412-c5585de4-f821-4e59-8b74-eb5c1b1a25e0.png)

- EasyEnsembleClassifier
  - Balanced Accuracy Score - 0.9317
  - Precision Score - 0.09
  - Recall Score - 0.94
  - Explanation - The EasyEnsembleClassifier performed the best of the models; accuracy of 0.93, precision 9 times better than the sampling algorithms and 3 times better than the BalancedRandomForestClassifier, and the best recall score as well, by far. 
  - Screenshot - ![image](https://user-images.githubusercontent.com/114685724/222517452-4be3ea71-831f-4bf2-ae26-41dd4228575a.png)


## Summary

Overall, the EasyEnsembleClassifier performed the best out of all of the machine models. I would recommend using the EasyEnsembleClassifier if you had to choose one, but understand that it'll still be "wrong" 7% of the time, and someone who shouldn't have been approved will be. Also, 9 out of every 10 "positives", or "high_risks will be a false positive. That's also not _great_ so if anything, I'd recommend we keep searching for a better algorithm. 
