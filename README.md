# Credit Risk Analysis With Machine Learning
Looking at data from Fast Lending, a peer to peer lending company, credit risk of customers was evaluated using six different types of Machine learning methods in hopes achieving lower default rates. The data contained information on roughly 69,000 customers. This data is considered unbalnced due to the fact that good loans heavily outweigh bad loans. The data underwent different machine learning methods. Imblearn and scikit libraries were used to oversample (RandomOverSampler, SMOTE) and undersample (ClusterCentroids) the data. A combination of over/under sampling was used with SMOTEENN algorithm. Finally two ensemble classifiers were used being the RandomForestClassifier and the EasyEnsembleClassifier. The results of each model are compared below.

## Results
- The Naive Random Oversampling (RandomOverSampler) had a balanced accuracy score of 67%, precison for high_risk was only 1%, recall was 74% and the F1 score was .02.
 ** insert naive pic
- The SMOTE oversampling had a balanced accuracy score of 66%, precison for high_risk was only 1%, recall was 63% and the F1 score was .02.
** smote pic
- The ClusterCentroids undersampling had a balanced accuracy score of 54%, precison for high_risk was only 1%, recall was 67% and the F1 score was .01.
** cluster pic
- The SMOTEENN over/ undersampling had a balanced accuracy score of 64%, precison for high_risk was only 1%, recall was 70% and the F1 score was .02.
** SMOTEENN pic
- The ensemble classifier RandomForestClassifier had a balanced accuracy score of 68%, precison for high_risk was 88%, recall was 37% and the F1 score was .52.
** random forest
- The EasyEnsembleClassifier had a balanced accuracy score of 93%, precison for high_risk was only 9%, recall was 92% and the F1 score was .16.


## Summary
All models using over/under sampling were had very low F1 scores indicating thre is a large imbalance between precision and sensitivity. This shows the models were heavily leaning towards either being mostly highly sensitive or mosly highly precise. None of the first 4 models would help in determining credit risk and lowering the default rate. 

The ensemble classfifer RandomForestClassifier had the highest F1 score of all models used. This indicates there is a decent balance between sensitivity and precision. The sensitivy was 37% while the precision was 88%. In the scenario this model would be used in which is predicting credit risk, a model with higher precision would help reduce default rates as true positives are more likely to be more accurate rather than high sensitivity.