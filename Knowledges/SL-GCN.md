20221201
Topics: #Model

---
**Full name**: Sign Language Graph Convolution Network
**Useful**:
- Construct a spatio-temporal graph to model the dynamics of human body skeleton for [[SLR]] 
- Plus with attention mechanism to extract motion dynamics from the graph

# Pipeline
![[Pasted image 20221201002306.png]]

## Graph Construction and Reduction
| Simple way | Difficult (Motivation) | Soluted |
| --- | --- | --- |
| Use ground-truth skeleton annotations by device capture input| Do not have annotation for the hands | Use a pretrained whole-body pose estimate network|

Find the maximum distance is 1, if longer than 1 than this is not exist, else add to adjacent matrix
Because the original is use 133 nodes of skeleton (Hard to learn interact between nodes) -> Use 27 nodes (10 nodes both hands, 7 nodes upper body)

## Graph Convolution
| Motivation| How? |
| --- | --- | 
| Model dynamic skeletons| Capture the pattern embedded in the whole-body skeleton graph -> Adopting the spatio-temporal [[GCN]]| |

$x_{out} = D^{-1/2}(A+I)D^{-1/2}x_{in}W$

# Learn more
the adjacent matrix A
Graph Convolution


---

# References
