## cs231 lecture 3

- Q. Hidden layer를 활성화 시키는 함수로 sigmoid를 사용하지 않고 ReLU라는 활성화 함수를 사용하는데 그 이유가 뭘까요?
- A1. ReLu 함수는 0보다 작은 값이 나온 경우 0을 반환하고, 0보다 큰 값이 나온 경우 그 값을 그대로 반환하는 함수입니다.

    0보다 큰 값일 경우 1을 반환하는 sigmoid와 다릅니다. 내부 hidden layer에는 ReLU를 적용하고 마지막 output layer에서만 sigmoid 함수를 적용하면 이전에 비해 정확도가 훨씬 올라가게 됩니다.
- A2. Sigmoid function 특성상 오른쪽과 왼쪽 끝으로 갈수록 기울기가 낮아지는(경사 소멸 vanishing gradient problem) 단점이 있는데, layer가 더 깊어질수록 이 단점이 계속 누적돼 오차율 계산이 어려워집니다.

  이 말은 x의 절대값이 커질수록 backpropagation 과정에서 미분 값이 소실될 가능성이 커지는 것을 의미합니다.

    이 경사 소멸을 해결하기 위해 나온 함수가 ReLU 함수이며, x값이 0보다 작은 값이면 뉴런이 죽을 수 있는 단점이 있지만 sigmoid, tanh 함수보다 학습이  빠르고, 연산 비용이 적고, 구현이 매우 간단한 커다란 장점이 있어서 자주 쓰입니다.