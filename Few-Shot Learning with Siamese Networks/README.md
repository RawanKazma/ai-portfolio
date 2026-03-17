
# Few-shot Learning with Siamese Networks

**Course Project at VUB – Vrije Universiteit Brussel**  
This project was completed as part of a course assignment and done collaboratively by a team of 3 students. 

---

## Contributions 
Update the table below to indicate who did what:

| Student | Contribution |
|---------|-------------|
| Rawan Kazma | TBD |
| Elly Delaplace | TBD |
| Nicolas Xanthakis | TBD |

---

## Project Overview
Few-shot learning aims to detect and recognize **novel, unseen images** using only a few annotated examples, after training on a larger dataset. This project implements a **Siamese network**, a deep learning architecture with two identical sub-networks that share parameters. The network learns a **similarity function** rather than a classification function, distinguishing whether images are from the same class or different classes.  

The network is trained end-to-end using a **contrastive loss** and a **triplet loss**, encouraging embeddings of similar images to be close and dissimilar images to be far apart. During inference, a query image is compared with a support set to find the most similar image.

---

## Dataset
- **Mini-ImageNet**: Subset of ImageNet with 60,000 images (50K train, 10K test) across 100 classes.  
- Images are 224x224 pixels.  
- Predefined train/test splits are used.  

---

## Architecture
- **Custom Siamese Network**:
  - Single CNN network processes image pairs/triplets.
  - Produces feature embeddings per image.
  - Distance metrics (cosine similarity or Euclidean) are used to compute similarity.
  - Both **contrastive loss** and **triplet loss** are implemented from scratch.  

- **Inference**:
  - Input a novel query image + support set.
  - Output: the most similar image in the support set.

- **Visualization**:
  - PCA or t-SNE used to show that embeddings of similar classes are closer.
  - Explainable AI tools (e.g., GradCAM) to understand model decisions.

---

## Evaluation & Analysis
- Evaluate on **n-way k-shot** scenarios:
  - Example: 5-way 1-shot, 5-way 4-shot, 5-way 8-shot, 5-way 16-shot.
- Metrics:
  - **Top-1 / Top-5 accuracy**
  - **Mean Average Precision (mAP)** using similarity scores
- 20 random query images sampled from test set for evaluation.
- Visualize embeddings and model behavior using GradCAM or similar tools.

---

## Baselines
- **Custom Siamese Networks**: contrastive loss & triplet loss  
- **Pretrained ResNet18 Siamese Networks**:
  - Finetuned on mini-ImageNet
  - Compared with a ResNet18 trained on Places365
- Evaluation done on mini-ImageNet test set to avoid data leakage.

---

## References
1. Koch, G., Zemel, R., Salakhutdinov, R. (2015). *Siamese neural networks for one-shot image recognition.* ICML.  
2. Snell, J., Swersky, K., Zemel, R. S. (2017). *Prototypical networks for few-shot learning.* arXiv.  
3. Vinyals, O., et al. (2016). *Matching networks for one-shot learning.* arXiv.  
4. Zhou, B. et al. (2018). *Places: A 10 Million Image Database for Scene Recognition.* IEEE TPAMI.  
5. Deng, J., et al. (2009). *ImageNet: A large-scale hierarchical image database.* CVPR.
