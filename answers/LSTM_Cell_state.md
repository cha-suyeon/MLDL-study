## cs231 lecture 10 

- Q. LSTM에는 cell state와 hidden state가 모두 있습니다. cell로 long-term dependency를 다룰 수 있다고 하는데요. cell state의 역할은 무엇인가요?
- A.

    - cell state: 정보를 기억하는 역할
    - cell state는 sequence chain 아래로 정보를 전달하는 고속도로 역할을 합니다. 네트워크의 'memory'라고 볼 수 있습니다. 
    - 이론적으로는 cell state는 sequence 처리 전반에 걸쳐 관련 정보를 전달할 수 있습니다.
    - 따라서 이전 time step의 정보여도 이후 time step에 이동하여 short-term memory의 영향을 줄입니다.
    - cell state가 진행됨에 따라 정보는 gate를 통해 cell state에 추가되거나 제거됩니다.
    - gate는 cell state에 대해 허용되는 정보를 결정하는 다양한 neural network입니다. training 중 유지하거나 잊어야 할 정보가 무엇인지를 학습합니다.
    - 각 gate마다 사용하는 전용 가중치가 있고, 전달해야하는 정보를 결정하기 위해 tanh와 sigmoid의 출력값을 곱해 다음 layer로 전달하는 방식이었습니다.
    - 따라서 LSTM이 layer에 사용되는 gate는 data와 gradient의 흐름을 적절히 조절하는 mechanism이 됩니다!