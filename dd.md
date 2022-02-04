## | 0. 강의 자료
### CS231n: Convolutional Neural Networks for Visual Recognition

* CS231n 전체 강의자료: [강의 자료 링크](http://cs231n.stanford.edu/2016/syllabus)
* CS231n 2강: [Youtube 링크](https://youtu.be/OoUX-nOEjG0)
* CS231n_2강 강의자료: [slide.pdf](http://cs231n.stanford.edu/slides/2017/cs231n_2017_lecture2.pdf)


## | 1. 강의 목표

1. K-Nearest Neighbor
2. Linear classifiers: SVM, Softmax
3. Two-layer neural network
4. Image features


## | 2. Image Classification

**The Problem**: Semantic Gap

An image is just a big grid of numbers between [0, 245]:

컴퓨터는 이미지를 0부터 245까지 픽셀로 본다. 따라서, 컴퓨터가 이미지 분류하기 위해서 몇 가지의 장애가 있다.

1. Viewpoint variation
2. Illumination
3. Deformation (변형)
4. Occulsion (가려짐)
5. Background Clutter (배경과 유사)
6. Intraclass variation (클래스 내부 분산)

<br>

### 이미지 접근 방법

1. Collect a dataset of images and labels
2. Use Machine Learning to train a classifier
3. Evaluate the classifier on new images

<br>

### First classifier: Nearest Neighbor

* Memorize all data and labels
```
def train(images, labels):
	# Machine learning
    return model
```

* Predic the label of the most similar training image
```
def predict(model, test_images):
	# Use model to predict labels
    return test_labels
```

<br>


## | 3. K-Nearest Neighbors

### Parameter of K-Nearest Neighbors

1. K
2. Distance Metric


### | K closest points

Instead of copying label from nearest neighbor, take **majority vote** from K closest points

![](https://images.velog.io/images/cha-suyeon/post/9eaede40-0fef-4718-abba-198160e0e3e9/image.png)



### | Distance Metric(L1, L2)


![](https://images.velog.io/images/cha-suyeon/post/5d799b42-ff9b-4d2d-9680-bc6a59d29a81/image.png)

![](https://images.velog.io/images/cha-suyeon/post/decb8802-bad5-4fba-937e-38476ef02dcf/image.png)


## | 4. Hyperparameter(Machine Learning)

In machine learning, a **hyperparameter** is a **parameter whose value is used to control the learning process**. By contrast, the values of other parameters (typically node weights) are derived via training.

These are hyperparameters: **choices about the algorithm that we set rather than learn.
**


### 이미지 분류에선 잘 사용하지 않는 이유

1. very slow at test time
2. Distance metrics on pixels are not informative
3. Curse of dimensionality


## | 5. Linear Classification

In the field of machine learning, the goal of statistical classification is to use an object's characteristics to identify which class (or group) it belongs to. A **linear classifier ** achieves this by making a classification decision based on the value of a linear combination of the characteristics. An object's characteristics are also known as feature values and are typically presented to the machine in a vector called a feature vector.

![](https://images.velog.io/images/cha-suyeon/post/20c538e4-946a-4b45-a59e-999de5e0f687/image.png)

![](https://images.velog.io/images/cha-suyeon/post/49a6ea6f-4784-4e89-b025-ce8f9ed1d98e/image.png)

![](https://images.velog.io/images/cha-suyeon/post/f91a13d1-f978-40a9-b52f-10ddf144ddfd/image.png)

* Hard cases for a linear classifier

![](https://images.velog.io/images/cha-suyeon/post/f41049a2-0dac-4de5-8f2c-e50acb964316/image.png)

