## cs231 lecture 10
### gate, cell state 역할

- Q. LSTM에 도입된 세 가지 gate의 역할은 무엇인가요? 
- A.

    - Forget gate: 현재 입력과 이전 출력을 고려해서 cell state의 어떤 값을 버릴지를 결정합니다.
    - Input gate: 현재의 unit과 이전 출력으로 얻어진 값을 current state에 얼마나 반영할지 정하는 역할입니다.
    - Output gate: current cell의 어느 부분을 output으로 만들지 결정합니다.

<br/>