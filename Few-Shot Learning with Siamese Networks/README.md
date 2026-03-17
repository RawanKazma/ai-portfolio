# Few-shot Learning with Siamese Networks

**Course Project at VUB – Vrije Universiteit Brussel**  
Collaborative project completed by a team of three students.

---

## Contributions
| Student | Contribution |
|---------|-------------|
| Rawan Kazma | TBD |
| Elly Delaplace | TBD |
| Nicolas Xanthakis | TBD |

---

## Project Overview
Implemented a **Siamese network** for **few-shot learning** to recognize novel, unseen images using only a few examples. The network learns a **similarity function** to compare images and determine if they belong to the same class, using both **contrastive** and **triplet losses**.  

Key outcomes:  
- Successfully trained the network on **Mini-ImageNet** (100 classes, 224x224 images).  
- Designed a **custom CNN architecture** for embeddings.  
- Evaluated on multiple **n-way k-shot scenarios**, demonstrating accurate few-shot recognition.  
- Applied **visualization techniques** (PCA, t-SNE) and **GradCAM** for model interpretability.

---

## Architecture & Approach
- **Custom Siamese CNN**:
  - Processes image pairs/triplets to generate embeddings.
  - Distance metrics (cosine similarity / Euclidean) used to compute similarity.  
- **Inference**:
  - Input: novel query image + support set.  
  - Output: most similar image in support set.  
- **Model Analysis & Visualization**:
  - Embeddings visualized with PCA/t-SNE.  
  - GradCAM used to interpret model decisions.

---

## Evaluation
- Tested on **n-way k-shot tasks** (e.g., 5-way 1-shot, 5-way 4-shot, 5-way 8-shot, 5-way 16-shot).  
- Metrics computed:
  - **Top-1 / Top-5 accuracy**  
  - **Mean Average Precision (mAP)** based on similarity scores  
- Demonstrated that similar class embeddings cluster together and dissimilar ones are separated.

---

## Baselines
- Compared **custom Siamese networks** with **pretrained ResNet18-based Siamese networks**.  
- Finetuned ResNet18 models on Mini-ImageNet and Places365 for comparison.  
- Evaluated consistently on Mini-ImageNet test set to avoid data leakage.

---

## Skills & Techniques Demonstrated
- Few-shot learning & Siamese networks  
- CNN architecture design and embedding learning  
- Custom implementation of **contrastive** and **triplet losses**  
- Model evaluation in multiple n-way k-shot scenarios  
- Visualization & interpretability with PCA, t-SNE, GradCAM  
- Working with large datasets (Mini-ImageNet) and PyTorch/Colab  

---

## References
1. Koch, G., Zemel, R., Salakhutdinov, R. (2015). *Siamese neural networks for one-shot image recognition.* ICML.  
2. Snell, J., Swersky, K., Zemel, R. S. (2017). *Prototypical networks for few-shot learning.* arXiv.  
3. Vinyals, O., et al. (2016). *Matching networks for one-shot learning.* arXiv.  
4. Zhou, B. et al. (2018). *Places: A 10 Million Image Database for Scene Recognition.* IEEE TPAMI.  
5. Deng, J., et al. (2009). *ImageNet: A large-scale hierarchical image database.* CVPR.
