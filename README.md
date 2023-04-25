# Threat_Detection_YOLOV7

Build a model capable of detecting and classifying weapons

## Objective of this notebook
- The purpose of this notebook is to build model capable of detecting and classifying weapons
- The algorithm of choice here is YOLOV7 and we would be custom training YOLOV7 on a weapons datatset
- Details of the **Problem Statement**  , **Data Set** , **Data Pre-processing & Splits**,  **Architecture/Algorithm** , **Summary of the Code/Solution**  , **Sample Output/Prediction** from the program and **Final Result** of the project are listed in the sections to follow.

## Problem Statement 
Computer vision can be used to pro-actively detect threats 


## Data Description:
- Data Set: https://github.com/ari-dasci/OD-WeaponDetection
- Total No Of classes in the entire dataset = 6 
- Total No Of Image Files =4127(Train) +  857(Val)
 
## Domain:
   Surveillance

## Data Pre-processing & Splits:
- Data exists in te original dataset in splits of train(1427 files) and Test(857 files), we will keep/use the same split
- Label Data exists in the orignal datat set in the YOLOV7 specific label format( wherein there will be one label file for each image file and the format of the label file will be as follows class|xcenter|ycentre|width|height for each bounding box in that image and labels were generated in this format).We will re-use the data labels  as is 
 -There are 6 available classes namely 
 - The Train and Validation splits are done/exist  in a 80:20 split respectively and the details are as follows
![image](https://user-images.githubusercontent.com/68383273/232124614-ef6ee13e-3a07-49bd-8a6c-f3627608f753.png)
 
 
 ## Architecture/Algorithm:
 YOLOV7 by https://github.com/WongKinYiu/yolov7

## Summary of the Solution/Code:
The code aims at custom training YOLOV7 on the xView dataset
- In this notebook we first Explore/Sanity test on  YOLOV7  API as is and run some general inferences to validate setup
- We then Custom Train this YOLOV7 API on Weapon dataset for 55 epochs 
- We log the mAp score and F1 scores
- We establish a baseline score
- We do not tune the model further because baseline scores were satisfcatory
- Run inferences on some images from validation split

## Sample Ouput/Prediction :
Here are a couple of sample Ouput images from  the program/model .

![image](https://user-images.githubusercontent.com/68383273/232134906-343bf44e-cc94-40c8-860b-b5b3eb4261ad.png)

![image](https://user-images.githubusercontent.com/68383273/232135071-2907fd22-c33d-4af7-81e3-0a98ff7d09ec.png)



## Result
![image](https://user-images.githubusercontent.com/68383273/232135671-72c23cec-6bc8-45a0-9c78-17792736f0f3.png)
![image](https://user-images.githubusercontent.com/68383273/232135817-0f891d74-bd78-4afa-939b-39e347c0e2d1.png)

![image](https://user-images.githubusercontent.com/68383273/232136246-b435476b-258c-4892-b12e-4cbd551dc8d3.png)

## References & Guidance
- https://dasci.es/transferencia/open-data/24705/ 
- https://github.com/ari-dasci/OD-WeaponDetection/tree/master/Weapons%20and%20similar%20handled%20objects/Sohas_weapon-Detection-YOLOv5

