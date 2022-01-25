# Credit_Risk_Analysis

## PURPOSE 
The purpose of this analysis was to run different, supervised machine learning algorithms to evaluate their performance on predicting results from an imbalanced dataset that describes credit card risk.
The different algorithms used include: oversampling, undersampling, a combination of the former and latter, and ensemble algorithms. 

## RESULTS
  ### 1. RandomOverSampler
  ![image](https://user-images.githubusercontent.com/90593897/150884776-bd4ef7d7-b852-4cf4-93a3-a3b86fa75752.png)


  ![image](https://user-images.githubusercontent.com/90593897/150884730-56841693-1f57-434c-833c-b4c4ea57d6bb.png)

    - Avg. Balanced Accuracy Score: .60
    - Avg. Precision: .99
    - Avg. Recall: .60
    - Avg. F1 score: .74
    
  ### 2. Synthetic Minority Oversampling Technique (SMOTE)
  ![image](https://user-images.githubusercontent.com/90593897/150886425-bedc14b4-d936-46f0-9501-f1a1935216fe.png)


![image](https://user-images.githubusercontent.com/90593897/150886518-b4dca40f-09b9-4923-a7c8-a9a212a28819.png)

    - Avg. Balanced Accuracy Score: .69
    - Avg. Precision: .99
    - Avg. Recall: .69
    - Avg. F1 score: .81
    
  ### 3. ClusterCentroids (Undersampling Technique)
  ![image](https://user-images.githubusercontent.com/90593897/150886551-6fb6d2e8-5b34-4ddf-aa42-dc7e88d36d52.png)


![image](https://user-images.githubusercontent.com/90593897/150886596-c06a0eb0-d3af-4d49-98b0-275e9847bb58.png)

    - Avg. Balanced Accuracy Score: .40
    - Avg. Precision:  .99
    - Avg. Recall: .40
    - Avg. F1 score: .56
    
  ### 4. SMOTEENN (SMOTE and Edited Nearest Neighbors; Combo Technique) 
  ![image](https://user-images.githubusercontent.com/90593897/150886635-22ea5eac-782b-48e8-88eb-70043aa9fa1a.png)


![image](https://user-images.githubusercontent.com/90593897/150886656-8df61096-8630-4121-8677-9506941c7c3a.png)

    - Avg. Balanced Accuracy Score: .60
    - Avg. Precision: .99
    - Avg. Recall: .60
    - Avg. F1 score: .74
    
  ### 5. BalancedRandomForestClassifer 
  ![image](https://user-images.githubusercontent.com/90593897/150886700-bebd6e80-3156-421e-a3e3-5935fd7a1d24.png)


![image](https://user-images.githubusercontent.com/90593897/150886729-9059c069-ab29-4a59-8ee3-5433fd7fed7f.png)

    - Avg. Balanced Accuracy Score: .79
    - Avg. Precision: .99
    - Avg. Recall: .87
    - Avg. F1 score: .93
    
  ### 6. EasyEnsembler (Adaptive Boost Clasifier) 
  ![image](https://user-images.githubusercontent.com/90593897/150886764-4833829d-b21c-4025-a7a5-1006f53b8c28.png)


![image](https://user-images.githubusercontent.com/90593897/150886805-a3ab8e9b-ac1d-44d9-8321-009a9fb80386.png)

    - Avg. Balanced Accuracy Score: .93
    - Avg. Precision: .99
    - Avg. Recall: .94
    - Avg. F1 score: .97

## SUMMARY
If our goal is to miminize the approval of high-risk loans, we want high recall so that we don't accidentally approve a person for a loan who is high-risk, and might not pay us back. This may come at the expense of declining some low-risk people a loan, but it would help us not lose money in the long run. 

Based on this goal, the best model to use would be the EasyEnsembler model as it has the highest average recall rate of .94. The F1 score is also quite high at .97, which indicates there is good balance between both precision and recall. 

The model with the lowest average recall score is ClusterCentroids (Undersampling Technique), so this model should be avoided. 
