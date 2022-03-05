## cs231 lecture 7
### Why does dropout increase the training time per epoch in a neural network?

- Q. Dropout을 사용하게 되면 전체 학 습시간이 늘어나는 이유로 각 스텝마다 업데이트되는 파라미터의 수가 줄어들기 때문이라고 하였는데요. 파라미터의 수가 줄어들면 학습시간이 줄어드는 게 아닌지요?
- A. Dropout은 일부 Neuron을 0으로 만들기 때문에 계산량이 줄어들 것이라 생각하는 논리는 어느 정도 이해가 됩니다. 하지만 이 경우는 sparse matrix는 해당되지만, dense matrix는 해당되지 않습니다.

    Dense Matrix에서 Vectorized 된 연산을 사용하기 때문에 모든 항목을 이용한 연산을 진행합니다. 따라서 0의 개수에는 차이가 없습니다.

    결론적으로 Dropout을 적용하면 일반적으로 training time이 늘어나고, matrix에서 row 또는 column 단위로 unit을 삭제하는 다른 Dropout 기법으로 training time을 향상 시키는 방법도 존재합니다.

- `+`: 또 다른 이유로 난수 생성에 대한 접근인데요. 드롭아웃은 `random number generation`이라는 것입니다. 실제로 매우 많은 수의 차원에 적용하면 모든 차원에서 이상적으로 **무작위**로 작동하지 않습니다. 즉, 차원 간의 상관 관계가 증가하는데요. 이 random number generation을 더 복잡하게 만들면 computing에 더 많은 비용이 들 수 있다는 점입니다.
