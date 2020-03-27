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
### Train CIFAR10 with PyTorch resnet18 model

This repo is subjected to submission of assignment from S8. It implements resnet18 model. 
1. S8 - The target is to acheive 85% accuracy in any number of epochs. 
2. S9 - The target is to acheive 87% accuracy in any number of epochs.
        ,Implement Albumentation, 
        Implement Gradcam 
### Results and some observations S8 submission
1. Highest test accuracy is 84.51% for only one iteration in total number of epochs.
2. The test accuracy keeps on oscillating in range of 83 - 84 % after a definite number of epoch.
3. The training accuracy is always 96-97 % during training.

### Results and some observations S9 submission
1. Highest test accuracy is 85.41% within 60 epochs. 
2. The test accuracy goes high in less number of epochs than the number of epochs in S8 submission.
3. Albumentation is used because of which the test accuracy goes high.
4. GradCam is implemented.

### Accuracy
| Model             | Acc.        |
| ----------------- | ----------- |
| [resnet18](https://arxiv.org/abs/1512.03385) S9         | 85.41%      |
| [resnet18](https://arxiv.org/abs/1512.03385) S10         | 88.41%      |

## File Structure
![Test Image](https://github.com/futartup/S8-assignment/blob/master/FS.png)


