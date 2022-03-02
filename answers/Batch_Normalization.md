## cs231 lecture 6
### about Batch Normalization

### 개념

수십 개의 layer가 있는 심층 신경망을 훈련하는 것은 학습 알고리즘의 초기의무작위 가중치와 구성들에 민감할 수 있습니다.

그 이유는 가중치가 업데이트 될 때, 각 미니 배치 이후에 네트워크의 깊은 layer에 대한 입력 분포가 변할 수 있기 때문인데요. 이런 변화를 “*internal covariate shift”이라고도 합니다.*

배치 정규화는 각 미니 배치에 대한 계층에 대한 입력을 표준화하는 매우 깊은 신경망을 훈련하는 기술입니다. 이는 학습 프로세스를 안정화하고 심층 네트워크를 훈련하는 데 필요한 훈련 에포크 수를 획기적으로 줄이는 효과가 있습니다.

<br/>

- Q1. Batch Normalization가 왜 필요할까요?
- Q2. Batch Normalization의 효과는 무엇인가요?

<br/>

![img_3.png](img_3.png)

- A. input을 정규화하면 network가 첫 번째 layer에서 parameter를 더 효과적으로 학습합니다.

    network의 두 번째 layer가 첫 번째 layer의 activation values를 inputs으로 받아들이기 때문에, 이전 layer에서 설정한 정규화된 값을 network에서 더 효율적으로 학습하는데 도움이 된다고 봅니다.

    하지만 앞의 예시에서는 Deep Neural Network를 사용할 때, hidden layer에 대한 input distribution은 더 이상 정규화된 분포가 아니며, parameter update로 인해 변경됩니다.

    그래서 Batch Normalization의 개념은 모든 hidden layer에 대한 입력 분포가 정규화되도록 하는 아이디어입니다.

    모든 layer는 연결하는 weight에 대한 학습 향상을 위해 각 계층의 actiavations을 normalize함으로써 hidden layer에서 더 유용하게 작동하게 합니다.

    즉, 각 layer를 normalization하는 것입니다.

    이런 이론을 바탕으로 더 깊은 network를 빠르게 training 할 수 있게 되었습니다.

    이건 이전 layer의 parameter가 update될 때 활성화 분포가 이동하지 않도록 막습니다.

<br/>

- 정리한 글: [Batch Normalization (배치정규화)](https://velog.io/@cha-suyeon/DL-Batch-Normalization-%EB%B0%B0%EC%B9%98%EC%A0%95%EA%B7%9C%ED%99%94)