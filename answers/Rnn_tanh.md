## cs231 lecture 10
### about RNN + tanh

- Q. RNN에서 activation function으로 tanh를 사용하는 이유는?
- A. tanh를 사용하는 것이 상대적으로 gradient vanishing & exploding 을 예방하는데 적합하기 때문입니다.

    tanh는 [-1, 1]로 output 값을 정형화시켜 사이즈를 일정하게 유지시킵니다. sigmoid보다 gradient descent가 더 잘 된다는 특징도 갖고 있습니다.

    sigmoid는 [0, 1]로 output을 정형화하지만, 미분의 최대값이 0.25이기 때문에 deep해질수록 기울기 소실이 발생하게 됩니다. (계속해서 값이 작아지다 소실되는 현상)

    ReLU = [0, max]의 경우, RNN은 같은 layer를 반복하는 성질이 있어서 1보다 큰 값이 들어오게 되면 deep해질수록 값이 너무 커지는 문제 발생합니다. (기울기가 발산해버리는 현상)

<br/>

- `+`: RNN은 CNN과 달리 이전 step의 값을 가져와서 사용하므로 ReLU를 쓰게되면 이전 값이 커짐에 따라 전체적인 출력이 발산하는 문제가 생길 수 있습니다. 따라서 과거의 값들을 recurrently하게  사용하는 RNN 모델에서는 이를 normalizing 하는 것이 필요하며 이를 위해 sigmoid보다 기울기의 역전파가 더 잘되는 tanh를 사용함으로써 좋은 결과를 볼 수 있다고 합니다.

  일반적 feed-forward neural network에서는 대부분 ReLU를 사용합니다. vanising gradient는 RNN의 주요 문제입니다. activation function의 linear region에서 gradient를 유지하려면 2차 도함수가 0이 되기 전 길게 유지할 수 있는 함수가 필요했습니다. tanh는 이러한 속성에 꽤 능숙하다고 합니다.

  RNN은 forward pass동안 특히 많은 수의 non-linear 활성화 함수 구성을 포함합니다. gradient가 backpropagation되면 이전 hidden state에 대한 야코비안 행렬의 스펙트럼 반경(최대 고유값)이 시간이 지남에 따라 여러 backward steps에 걸쳐 효과적으로 지수화되고, 그라디언트 소실 문제가 악화됩니다. 이것이 standard Dense network보다 RNN에서 훨씬 더 두드러진 문제인 이유일 수 있습니다.

  특히 sigmoid는 0과 1 사이의 값을 출력하기 때문에 LSTM에서 3개 gate(in, out, forget)에 대한 gating 기능으로 사용되며 gate 전체에 정보가 흐르지 않도록 하거나 완전한 흐름을 허용할 수 있습니다.

  반면에 Vanishing gradient 문제를 극복하려면 2차 도함수가 0이 되기 전에 긴 범위를 유지할 수 있는 함수가 필요하고, tanh의 속성이 좋습니다.

  좋은 뉴런 단위는 경계가 있고 쉽게 구별 가능할 수 있고, 단조롭고 다루기 쉬워야 합니다. 이러한 특성을 고려한다면 서로 아주 좋은 대안이 되기 때문에 `ReLU` 대신 사용해도 된다고 생각합니다.