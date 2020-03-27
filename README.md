# EVA Assignment Submissions ( S8 Onwards )

This is an original submission of assignments from S8(session 8) onwards. The goal is to get hands on various state of art models and get to the target accuracy assigned.
The models that i have implemented here is resnet18 and will continously integrate later models onward. 

## Acknowledgements

I would like to thanks all the EVA4 telegram batch members who has helped me to implement the code whenever i am stuck.

I would also like to thank www.theschoolofai.in to give me this opporthunity to get hands on AI. 

## Prerequisites
- Python 3.6+
- PyTorch 1.0+

## Changes to the original file

1. Found the best LR using LRfinder https://github.com/davidtvs/pytorch-lr-finder.
2. GradCam for falsely predicted images.
3. Added Cutout to the albumentation transformations.
4. Uses momentum with SGD.
5. Changed the epoch number to 50.

## Approach

### Prepare the Albumentation transformation
The first step is to understand the dataset. The dataset is CIFAR10 https://www.cs.toronto.edu/~kriz/cifar.html, which has  60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.

My observation is that when i applied as much as albumentation(HorizontalFlip, RandomContrast, RandomGamma, RandomBrightness, GaussNoise, RGBShift, GaussianBlur, Blur, ElasticTransform, Cutout, Normalize, ToTensor) https://albumentations.readthedocs.io/en/latest/, then i am training very hard and it was getting very difficult to reach the target accuracy of 88% validation. Then i reduced the transformation to HorizontalFlip, RandomRotate90, ShiftScaleRotate, Cutout, Normalize, Normalize, ToTensor, which i consider as lighter transformation which helped me to reach the target accuracy, But i see the model is overfitting. 

### Find the best LR using LRFinder

Find the best Learning Rate using LRFinder module.

### Repeat the process of adding transformation, momentum

Add or remove albumentation transformation and best values of model hyperparameters and see on which combination it gives best accuracy.

### Results and some observations S8 submission
1. Highest test accuracy is 84.51% for only one iteration in total number of epochs.
2. The test accuracy keeps on oscillating in range of 83 - 84 % after a definite number of epoch.
3. The training accuracy is always 96-97 % during training.

### Results and some observations S9 submission
1. Highest test accuracy is 85.41% within 60 epochs. 
2. The test accuracy goes high in less number of epochs than the number of epochs in S8 submission.
3. Albumentation is used because of which the test accuracy goes high.
4. GradCam is implemented.

### Results and some observations S10 submission
1. Highest test accuracy is 88.41% within 50 epochs. 
3. Albumentation is used because of which the test accuracy goes high.
4. GradCam is implemented on misclassified images.

### Accuracy
| Model             | Acc.        |
| ----------------- | ----------- |
| [resnet18](https://arxiv.org/abs/1512.03385) S9         | 85.41%      |
| [resnet18](https://arxiv.org/abs/1512.03385) S10         | 88.41%      |



## About me
My name is Anup Gogoi and i am an computer vision and AI enthusiast. My dream is to develop products which actually augment the intelligence of mankind in specially medical domain. Human brain can do very complex things, But still it will take some time to figure out the best medicine for Coronavirus pandemic, whereas a combined effort of human and artificial intelligence can do that in very less time.

My github repo is public and collaborators, suggestions are always welcomed.




