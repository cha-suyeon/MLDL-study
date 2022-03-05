## cs231 lecture 10
### about LSTM



- Q. LSTM이 RNN의 어떤 문제를 해결하였습니까? 
- A. LSTM은 gate가 추가된 RNN이라고 부르기도 합니다.

    RNN은 vanishing or exploding gradient 문제를 갖고 있는 반면, gate가 추가된 LSTM이 해당 문제를 해결하는데 효과가 있다고 합니다.

    LSTM의 핵심 개념은 cell state와 various gates입니다.

    cell state는 sequence chain 아래로 정보를 전달하는 고속도로 역할을 합니다. 네트워크의 'memory'라고 볼 수 있습니다.

    이론적으로는 cell state는 sequence 처리 전반에 걸쳐 관련 정보를 전달할 수 있습니다.

    따라서 이전 time step의 정보여도 이후 time step에 이동하여 short-term memory의 영향을 줄입니다.

    ![img_2.png](img_2.png)
    * RNN의 문제점은 short-term memory이다.

<br/>

