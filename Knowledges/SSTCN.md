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
| Step 1| Doing|

---
# References
