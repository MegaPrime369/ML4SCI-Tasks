### Estimating the mass of the particle using Vision Transformers

#### 1. Constructing the vision transformer
- Instead of regular vision transformer i have used deepViT as mentioned in https://arxiv.org/abs/2103.11886
-  It is because unlike that of CNNs that can be improved by stacking more convlutional layers, the performance of ViTs saturate fast when scaled to be deeper.
- So I have mixed the attention of each head post-softmax 

#### 2. Model Architecture
![enter image description here](https://raw.githubusercontent.com/MegaPrime369/ML4SCI-Tasks/master/Task%203/model%20architecture.png)

#### 3 Notes on the implemented model:
- We have taken the patch size as 25
- The depth is 12 
- There are 16 attention heads
- Dropout is set to 0.1
- `AdamW` optimizer is used as it is better suited for for Vision Transformers.
- `learning rate:1e-3` and `batch_size:32` is used.

####  4 Future Works
- [ ] Implementing other vision transformers like CaiT(https://arxiv.org/abs/2103.17239) which tries to solve the same problem
- [ ] Merging a Convolutional network with a Vision Transformer where the conv. network will be the teacher and the transformer will be the student
- [ ] Finding the best depth value for our vision transformer
