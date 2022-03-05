## cs231 lecture 5
### About CNN

- Q. CNN과 단순 feed-forward neural network를 비교하면 어느 쪽이 parameter 개수가 더 많을까요?
- A. feed-forward의 parameter 수가 훨씬 많습니다. hidden layer를 더 깊게 만들 수록 Fully Connected Neural Network과 CNN과의 학습 파라미터의 차이는 더 급격하게 늘어납니다. CNN은 Fully Connected Neural Network과 비교하여 다음과 같은 특징을 갖습니다. 
    - CNN은 training parameter 수가 매우 작음
    - training parameter가 작고, 학습이 쉽고 network 처리 속도가 빠름