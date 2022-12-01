20221201
Topics: #Model 

---
Useful:
- Recognize the sign language from whole-body features

# Pipeline
![[Pasted image 20221201144242.png]]

## Prepocessing data
| Step | Doing|
| --- | --- |
| Step 1: Extract features | Take **33 keypoints** (landmarks: 4 on mouth, 2 on shoulder, 2 on wrists, 22 on hands, 1 on nose, 2 on elbow) from 60 frames of each video |
| Step 2: down-sample | All features down-sample to 24 x 24 using [[max pooling]] with [[2D convolution]] layer seperably (easily to converge, reduce parameters)

## Pipeline explain
| Stage| Purpose | Doing|
| --- | --- | --- |
| 1 | Resize, process temporal information| Reshape features from 60 x 33 x 24 to 60 x 792 x 24, **feed 1 x 1 [[convolution]] layers**|
| 2 | Extract temporal and spatial information among same key points features | shuffle and divided to 60 groups, utilize grouped 3 x 3 [[convolution]] |
| 3 | Extract spatial information | Shuffle again and divided into 33 groups, utilize grouped 3 x 3 [[convolution]]| 
| 4 | Generate predict features| implement all 3 x 3 fully connected layers|
Note:
- 3 first stage, ouptut is added by a residual
- All stages (module) have dropout layer to avoid overfitting
### Problems in pipeline
| Problems| Soluted |
| --- | --- |
| one-hot with cross entropy results overfitting in some case| adapt [[label smoothing]] technique|



---
# References
