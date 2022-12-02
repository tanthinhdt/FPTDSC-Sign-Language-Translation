20221130
Topics: #ComputerVision, #NLP

---

# Problems

# Datasets

# Methodology
![[Pasted image 20221202121619.png]]
Learn the conditional probability $p(y|x)$ of generating a spoken language sentence $y = (y_1, y_2,..., y_u)$ with $U$ number of words given a sign video $x = (x_1, x_2,..., x_T)$ with T number of frames.

## Spatial and Word Embeddings
### Spatial Embeddings
Use 2D CNNs ([[Convolution Neural Network]]) to extract non-linear frame level spatial representations as:

$$
f_t = SpatialEmbeddings(x_t)
$$
### Word Embeddings
Transform the sparse one-hot vector representations, where each word is equidistant from each other, into a denser form, where words with similar meanings are closer by a linear projection.
$$
g_u = WordEmbedding(y_u)
$$
## Tokenization Layer
* Low level (characters, words):
	* Pros: smaller vocabularies
	* Cons: increase complexity, require long term relationships to be maintained
* High level (N-grams or phrases):
	* Pros: a small number of neighboring tokens
	* Cons: vasly increase vocabularies
* Framework for tokenization in the paper is generic
$$
z_{1:N} = Tokenization(f_{1:T})
$$
## Attention-based Encoder-Decoder Networks
### 1. Encoding phase


## Evaluation
1. [[BLEU Score]] 
2. [[ROUGE Score]]

# Recommend reading
* [[CTC Loss]]
* [[Encoder-Decoder Network]]
* [[Attention Mechanism]]

---

# References
