## cs231 lecture 3
### about Weight Initialization

- Q1. 가중치 초기화를 하는 이유는 무엇입니까?
- A1. 매개변수 가중치 초기화의 주요 목표는 feed forward neural network에서 exploding or vanishing gradients를 방지입니다. 또한, 초기 가중치 설정에 따라 학습 진행에 큰 영향을 미칩니다.

<br/>

- Q2. 0으로 초기화 되면 어떤 일이 발생합니까?
- A2.  0으로 초기화 할 경우, 뉴런이 동일한 가중치를 갖게 되어 동일한 기울기를 갖게 됩니다. 그렇다면 서로 다른 특성을 학습할 수 없게 됩니다.

<br/>

- Q3. 무작위로 초기화된 가중치가 매우 높거나 낮으면 어떤 일이 발생하나요?
- A3. 무작위로 가중치를 초기화하는 경우, Vanishing Gradient와 Exploading Gradient 문제에 직면하게 됩니다.

  첫 번째 경우는 parameter에 대한 cost의 gradient가 너무 작아서 최솟값에 도달하기 전 cost가 convergence하게 되는 경우이고,

  두 번째 경우는 cost가 최솟값을 중심으로 진동하며, 결국 overshooting이 발생되어 모든 neuron이 saturated 되는 경우입니다.