## Common Task 2.  Deep Learning based Quark-Gluon Classification

For this task we trained a Resnet 50 Model and VGG-12 Model

### VGG Model
#### 1. Training:
- Sampled Random 1500 rows from the entire dataset
- I divided the sampled data into train and test set with the ratio `80%:20%`
- Early stopping patience is `3` for monotonic increase in validation loss.
- In the model `optimizer : Adam`, `learning rate : 1e-3`, `batch size : 32`
#### 2. Performance
- `0.79` on `train_set`
- `0.77` on `test_set`

### Resnet Model
#### 1. Training:
- Sampled Random 1500 rows from the entire dataset
- I divided the sampled data into train and test set with the ratio `80%:20%`
- Early stopping patience is `3` for monotonic increase in validation loss.
- In the model `optimizer : Adam`, `learning rate : 1e-3`, `batch size : 32`

#### 2. Performance:
`0.75` on train_set
`0.70` on test_set

As we can see that the VGG model performs better than the resnet-50 model.
