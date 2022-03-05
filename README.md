# AIFFEL DeepML Flipped School
Facilitator: 차수연
- Date: 2022.01.10-2022.02.23
- Members: 김현지, 박흥선, 신은정, 안정희, 이다정, 이예영, 장병용, 조송희, 함태식

</br>

## Introduction

This `Flipped School` study is for people like this

```
1) Beginners who are new to Deep Learning
2) Intermediate level knowledge of Deep Learning but want to learn in-depth
3) Seniors who want to look at the trends of Deep Learning
```

> Effective facilitation of a discussion involves the employment of different perspectives and different skills to create an inclusive environment.
I tried to consider the features of effective discussions, amd conditions that promote small group interaction and engagement.


</br>

## Uploaded

> - Textbook [Posting Series](https://velog.io/@cha-suyeon/series/%ED%98%BC%EC%9E%90%EA%B3%B5%EB%B6%80%ED%95%98%EB%8A%94%EB%A8%B8%EC%8B%A0%EB%9F%AC%EB%8B%9D)
> - cs231 [Posting Series](https://velog.io/@cha-suyeon/series/CS231n)
> - [Review](https://velog.io/@cha-suyeon/%ED%8D%BC%EC%8B%A4facilitator%EB%A1%9C%EC%84%9C%EC%9D%98-DeepML-%ED%92%80%EC%9E%8E%EC%8A%A4%EC%BF%A8-%ED%9B%84%EA%B8%B0)


</br>

## Questions & Answers

> I provided questions to the discussion and summarize the results in a visible way using Notion tools.

1. 1x1 Convolution layer를 사용하는 이유는 무엇일까요? [Answer](https://github.com/cha-suyeon/MLDL-study/blob/main/answers/1x1_Convolution_layer.md)
2. Non-Linearity(비선형)의 의미와 필요한 이유 / tanh가 sigmoid보다 더 좋은 성능을 갖는 이유 / ReLU의 문제점 [Answer](https://github.com/cha-suyeon/MLDL-study/blob/main/answers/Activation_Function.md)
3. Batch Normalization가 왜 필요할까요? /Batch Normalization의 효과는 무엇인가요? [Answer](https://github.com/cha-suyeon/MLDL-study/blob/main/answers/Batch_Normalization.md)
4. 왜 layer가 Conv layer와 Pooling Layer가 반복되며 나올까요?/마지막에는 Fully Connected Layer를 사용하는 이유는 뭘까요? [Answer](https://github.com/cha-suyeon/MLDL-study/blob/main/answers/CNN_Architecture.md)
5. CNN과 RNN의 주요 차이점은 무엇일까요?
6. 수렴(`convergence`)을 빨리 할 수 있다는 것은 무슨 의미인가요?
7. Downsampling을 하는 이유는 무엇인가요? size가 작아지는 것을 막기 위해 padding을 하는데, 왜 pooling을 통해 또 줄이는 걸까요?
8. Dropout의  효과 / BN(Batch Normalization)이 나오고 나서 Dropout은 실제로 잘 안 쓰이나요? / Dropout은 주로 어디에 위치하는 것이 권장될까요?
9. Dropout을 사용하게 되면 전체 학 습시간이 늘어나는 이유로 각 스텝마다 업데이트되는 파라미터의 수가 줄어들기 때문이라고 하였는데요. 파라미터의 수가 줄어들면 학습시간이 줄어드는 게 아닌지요?
10. searching space에 3~4개 이상의 차원이 포함된 경우 그리드 검색을 사용하면 안 됩니다. high spaces에서는 아주 나쁜 성능을 보여주는데요. 그 이유는 무엇일까요?
11. Hidden layer를 활성화 시키는 함수로 sigmoid를 사용하지 않고 ReLU라는 활성화 함수를 사용하는데 그 이유가 뭘까요?
12. `learning rate` α가 너무 크거나 α가 너무 작으면 어떤 일이 발생하나요?
13. LSTM이 RNN의 어떤 문제를 해결하였습니까? 
14. LSTM에는 cell state와 hidden state가 모두 있습니다. cell로 long-term dependency를 다룰 수 있다고 하는데요. cell state의 역할은 무엇인가요?
15. LSTM에 도입된 세 가지 gate의 역할은 무엇인가요?
16. feedback RNN과 LSTM/GRU의 차이점
17. many-to-one RNN architecture를 적용하기 더 좋은 task 2개는?
18. 미니 배치 크기를 작게 할 때의 장단점은 무엇인가요?
19. CNN과 단순 feed-forward neural network를 비교하면 어느 쪽이 parameter 개수가 더 많을까요?
20. Pooling은 overlap 하지 않는 것이 일반적이라고 합니다. Pooling을 적용할 때 overlap하여 더 촘촘히 feature를 뽑으면 좋을 것 같은데, 그렇게 하지 않는 이유는 무엇일까요?
21. RNN에서 activation function으로 tanh를 사용하는 이유는?
22. `robust`하다는 것은 무슨 의미인가요?
23. Safety margin의 개념. 본 강의에서는 safety margin을 1로 사용하였지만 사실 이 값은 별 상관이 없다 라고 하였는데 그 이유가 무엇일까요?
24. SGD, RMSprop, Adam에 대해 차이점을 두고 설명할 수 있나요?
25. SGD에서 Stochastic의 의미는 무엇일까요?
26. 해당 슬라이드에서 Car score가 cat score보다 높아서 loss가 0이 됩니다. 그것은 무엇을 의미하는 것인가요? / SVM loss function을 아래와 같이 제곱항으로 바꾸면 어떻게 될까요?
27. Transfer Learning & Fine Tuning의 차이가 무엇일까요?
28. 가중치 초기화 필요성 / 0으로 초기화 할 경우 / 무작위로 초기화된 가중치가 아주 크거나 작을 때
29. padding에서 zero-padding을 많이 사용하는 이유는 무엇일까요?

</br>

## Curriculum

|No.|Date|Topic|Textbook|Lecture|
|:--:|--|:--:|--|:--:|
|00|January 07, 2022|Introduction to Machine and Deep Learning/Data Handling|chapter 1, 2|✖|
|01|January 10, 2022|Image Classification|✖|[Lec 2.](https://velog.io/@cha-suyeon/CS231n-2%EA%B0%95-%EC%9A%94%EC%95%BD)|
|02|January 12, 20222|Regression Algorithm and Regularization|[chapter 3 -1](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-K-Nearest-Neighbors-R), [chapter 3 -2](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-feature-engineering-%EB%8B%A4%EC%A4%91-%ED%9A%8C%EA%B7%80)|✖|
|03|January 17, 2022|Loss Functions and Optimization|✖|[Lec 3.](https://velog.io/@cha-suyeon/cs231-Lecture-3-Loss-Functions-and-Optimization-%EC%9A%94%EC%95%BD)|
|04|January 19, 2022|Classification Algorithm|[chapter 4 -1](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-Logistic-Regression%EB%A1%9C%EC%A7%80%EC%8A%A4%ED%8B%B1-%ED%9A%8C%EA%B7%80), [chapter 4 -2](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-%EB%B0%B0%EC%B9%98%EC%99%80-%EB%AF%B8%EB%8B%88-%EB%B0%B0%EC%B9%98-%ED%99%95%EB%A5%A0%EC%A0%81-%EA%B2%BD%EC%82%AC%ED%95%98%EA%B0%95%EB%B2%95)|✖|
|05|January 24, 2022|Introduction to Neural Networks|✖|[Lec 4.](https://velog.io/@cha-suyeon/CS231n-4%EA%B0%95-%EC%A0%95%EB%A6%AC-Introduction-to-Neural-Networks)|
|06|January 26, 2022|Deep Learning|[chapter 7](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8)|✖|
|07|February 7, 2022|Artificial Neural Networks for Image|[chapter 8](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-%ED%95%A9%EC%84%B1%EA%B3%B1-%EC%8B%A0%EA%B2%BD%EB%A7%9D-Convolution-Neural-Network)|✖|
|08|February 9, 2022|Convolutional Neural Networks|✖|[Lec 5.](https://velog.io/@cha-suyeon/cs231n-5%EA%B0%95-%EC%A0%95%EB%A6%AC-Convolutional-Neural-Networks)|
|09|February 14, 2022|Training Neural Networks I|✖|[Lec 6.](https://velog.io/@cha-suyeon/cs231n-6%EA%B0%95-%EC%A0%95%EB%A6%AC-Training-Neural-Networks-I)|
|10|February 16, 2022|Training Neural Networks II|✖|[Lec 7.](https://velog.io/@cha-suyeon/cs231n-7%EA%B0%95-%EC%A0%95%EB%A6%AC-Training-Neural-Networks-II)|
|11|February 21, 2022|Artificial Neural Networks for Text|[chapter 9](https://velog.io/@cha-suyeon/%ED%98%BC%EA%B3%B5%EB%A8%B8-%EC%88%9C%EC%B0%A8-%EB%8D%B0%EC%9D%B4%ED%84%B0%EC%99%80-%EC%88%9C%ED%99%98-%EC%8B%A0%EA%B2%BD%EB%A7%9D)|✖|
|12|February 23, 2022|Recurrent Neural Networks|✖| [Lec 10.](https://velog.io/@cha-suyeon/cs231n-10%EA%B0%95-%EC%A0%95%EB%A6%AC-Recurrent-Neural-Networks)|

</br>

## Reference

> - Material: 
>   - Textbook: `혼자 공부하는 머신러닝+딥러닝`
>     - 📙 Github: [Colab(Jupyter Notebook)](https://github.com/rickiepark/hg-mldl)
>     - 💻 Youtube Link: [hg-mldl](http://bit.ly/hg-mldl-youtube)
>   - Video(youtube): `cs231n`
>     - Title: `cs231n`(Convolutional Neural Networks for Visual Recognition)
>     - 📒 Course Notes: [CS231n(Spring 2017)](http://cs231n.stanford.edu/)    
