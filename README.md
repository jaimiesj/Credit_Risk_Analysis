# Credit Risk Analysis

## Overview of the analysis: 
The purpose of this analysis was to oversample, undersample, over and undersample in combination then use different machine learning approaches to determine if these methods should be used to predict credit risk for individuals looking to get loans

## Results: Comparison of balanced accuracy scores, precision and recall scores of each learning model
- RandomOverSampler
<img width="514" alt="Random Oversampler" src="https://user-images.githubusercontent.com/88955412/149671471-8612ba4e-f625-41ea-8109-81d92fb869f7.png">
- SMOTE
<img width="493" alt="SMOTE oversampler" src="https://user-images.githubusercontent.com/88955412/149671475-1b76ee56-5ba0-4389-b4f9-8fdf7ef082b5.png">
- ClusterCentroids
<img width="499" alt="ClusterCentroid" src="https://user-images.githubusercontent.com/88955412/149671478-1c54ccc0-02da-4f6d-8aec-784a35e45b88.png">
- SMOTEENN
<img width="493" alt="SMOTEENN" src="https://user-images.githubusercontent.com/88955412/149671482-5b2ddd1c-5e89-4254-8677-e272c269010d.png">
- BalancedRandomForestClassifier
<img width="495" alt="Balanced Random Forest" src="https://user-images.githubusercontent.com/88955412/149671492-5cc59fca-1c4f-4b65-bda1-027896afc4cf.png">
- EasyEnsembleClassfier: I was unable to use EasyEnsembleClassifier due to an error I tried to resolve but was unable to: 'EasyEnsembleClassifier' object has no attribute 'n_features_in_'. The solution was to downgrade the version of scikit-learn to 1.0 because this attribute was not support in the most recent version but despite downgrading, I was still unable to run the code error free. Instead I ran AdaBoostClassifier
<img width="500" alt="AdaBoostClassifier" src="https://user-images.githubusercontent.com/88955412/149671715-b9099a76-0bb9-4af0-af00-2ad3cf7a1e64.png">

## Summary: 
It appears the undersampling, oversampling and combination resulted in the lowest accuracy scoresSummarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning. All models were able to accurately predict a significant amount of false values, which is supported by the precision value for low-risk being so high. The precision value for high-risk was very low, explaining the high value of false negatives compared to true positives. As this is a large dataset, additional under-sampling techiques might be better, such as NearMiss, which eqalizes the majority and minority class. If I was able to resolve the EasyEnsembleClassifier error, it would have been interesting to see the classification report it generated as the sample code suggested it had a high accuracy value but high accuracy doesn't explicity mean it is an ideal model.
