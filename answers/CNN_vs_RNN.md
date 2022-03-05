## cs231 lecture 10
### about CNN and RNN

- Q. CNN과 RNN의 주요 차이점은 무엇일까요?
- A. CNN과 RNN의 주요 차이점은 문장과 같이 순서대로 오는 data인 시간 정보를 처리하는 능력입니다. RNN은 이런 목적을 위해 설계된 반면, convolution neural network는 시간 정보를 효과적으로 해석할 수 없습니다. 결과적으로 CNN과 RNN은 다른 용도로 사용되며, 사용 사례가 다른 만큼 신경망 자체의 구조에 차이가 있습니다.

    CNN은 데이터를 변환하기 위해 Convolution layer에서 filter를 사용하는 반면, RNN은 sequence의 다른 data point에서 활성화 함수를 재사용하여 series의 다음 출력을 생성하는 예측 모델입니다.

### 개념

**CNN(Convolutional Neural Network)** 은 심층 신경망의 한 종류입니다. 시각적 이미지 분석에 가장 일반적으로 사용됩니다. 입력이 vector인 신경망과 달리 여기에서는 입력이 *multi-channeled image*입니다. CNN은 최소한의 전처리가 필요하도록 설계된 *multilayer perceptrons*의 변형을 사용합니다.

**RNN(Recurrent Neural Networks)** 은 text, genome(유전체), handwriting, spoken word, numerical times series data와 같은 데이터 시퀀스의 패턴을 인식하도록 설계된 일종의 인공 신경망입니다.

Recurrent Neural Networks는 훈련을 위해 역전파 알고리즘을 사용합니다. 내부 메모리 내부 메모리로 인해 RNN은 입력에 대한 중요한 정보를 기억할 수 있으므로 다음에 올 내용을 매우 정확하게 예측할 수 있습니다.

    
  