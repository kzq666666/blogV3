---
title: "DeepLearning"
description: the note of deepLearning
date: 2020-11-13T15:47:57+08:00
draft: false
tags: ["Study"]
categories: ["Study"]
image:
---
How could I not study deep learning?
## Neural NetWord and Deep Learning
[传送门](http://www.ai-start.com/dl2017/html/lesson1-week1.html)
<br>
（1）
- Structured Data: database of data like a table or column that has a lot information
   Name | Age  |  Sex
--------|------|-------
    Bob | 27   |  male
  Alice | 23   |  female
- Unstructured Data:things like audio or image or text,the features might be the pixel values in and image. It is more difficult for computer to deal with unstructured data than strutured data

<br>（2）If you want to hit a high performance, you need train a big enough NN and a lot of data. `Scale has been driving deep learning progress.The scale means not only the nums of hidden layers of NN or nodes but only the scale of data`. We change the algorithm because it allows the code to run much faster and this allows us to train bigger neural network or complete the computation within reasonable amount of time. 

## Chapter Two

Cost Function:measure how well you are doing an entire training set.We need a cost function to get the parameters w by training the cost function and parameters b. It is used to measure the performance of the algorithm on all training samples. 
<br>

Loss Function:defined in a single training example, which is used to measure the performance of the algorithm in a single training sample

### Confront high Bias
- Bigger network like more hidden layers or more hidden nodes
- Train it longer
- train more advanced optimization algorithm
- decrease regularization parameter lambda
- add polynomial degress

### Confront high variance
- Regularization(L2 Regularization use lambda)
- Use more data or data augmentation
- Drop out
- Early Stop
- use simpler hypothesis
- add regularization item
- use validation set

### Normalizing inputs
(1) Process
- zero mean
- normalizion variance
(2) Why do that
- make the cost function faster to optimize

### Activation Fun
- sigmod：output (0,1) Vanishing gradients
- tanh: output (-1,1) zero mean, better to learn for the next layer, also have probleam of vanishing gradients compared with sigmod
- relu: if x < 0, output 0. If x > 0, output x. Commonly use it.
- leaky relu: if x < 0, output ax. If x > 0, output x.

### vectorization
- speed up the computing
tips: whenever possible, aviod explicit for loops
- in the layer computation, we can't aviod to use for-loops


### Others
(1) The layers is counted by the nums of hidden layers + 1. The input layers is not counted.
<br>
(2) If the data is not very large, the proportion of train,validation(dev),test is 6:2:2.But if the data is very big ten thousand even bigger 100W, the proportion is 98:2:2
<br>
(3) The validation set and test set should be come from the same distribution.
<br>
(4) DropOut is used in the training time, randomly delete the units of hidden layer.
<br>
(5) Classification，CE + sigmod or CE + softmax



# MATLAB Deep Learning
## Chapter 4 Neural NetWork And Classification
(1) The sigmod activation function accounts for the weighted sum of inputs. But the softmax activation function accounts not only for the weighted sum of inputs,but also for the inputs to the other output nodes
<br>

## Chapter 5 Deep Learning
## History
(1) It took 30 years to sovle the problems of the single-layer neural which lacks of the learning rule.The solution is the BP algorithm
<br>
(2) It took 20 years to solve the problems of the poor performance of the BP  -> the deep learing provided a solution.
<br>
(3) The problems of BP are as follows.
- Vanishing gradient
Solution: use the ReLU function as the activation function
- overfitting

- computational load

