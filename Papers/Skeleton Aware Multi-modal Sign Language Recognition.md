20221130
Topics: #ComputerVision , #NLP 

---
# Datasets

# Problem
| Problems | Suggested solution |
|------------ | ------------|
| Performing with fast speed, complex postures, facial expression |  |
| Lack of annotation on hand keypoints | |
| Sign language is affected by the language and culture| |
| Required both hand gestures and body motion. The facial express emotion| |
| | |


# Methodology
## Pipeline
| Step | Benefits and needs |
| --- | --- |
| Construct novel skeleton graph designed for [[SLR]] using whole-body keypoints and graph reduction| Utilizes pretrained whole-body pose estimator + requires no extra annotation effort|
| Propose [[SL-GCN]] to extract information from the whole-body skeleton graph| to model the [[dynamics embedded]]|
| Propose a novel [[SSTCN]] to further exploit whole body skeleton features| fully exploid data to improve the accuracy on whole-body keypoints comparing with the traditional 3D convolution|
| Propose a [[SAM-SLR]] framework for RGB and RGB-D based [[SLR]]| ensemble the proposed [[skeleton-based]] method with other modalities in both RGB and RGB-D scenarios|
## Evaluation

# Result


---

# References


