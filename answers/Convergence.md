## cs231 lecture 6
### What is Convergence?

- Q. 수렴(`convergence`)을 빨리 할 수 있다는 것은 무슨 의미인가요?
- A. 간단히 말하자면 수렴한다는 것은 모델이 최적의 parameter를 찾는다는 것이고, 수렴이 빠르다는 것은 적합한 가중치를 빨리 계산하여 찾아낸다는 것입니다.

### 개념

딥러닝에서 문제를 공식화할 때 모델 weights를 parameter로 사용하는 loss function을 생각해 내야 합니다.

backpropagation은 loss function에 의해 정의된 error manifold의 임의의 지점에서 시작하고 매 반복마다 weights를 업데이트하여 error 값을 최소화하는 지점에 더 가까이 이동하려고 합니다.

기본적으로 모델이 가질 수 있는 모든 가능한 가중치 세트와 주어진 loss function에 대해 관련된 loss가 있으며, 우리의 목표는 이 manifold에서 최소점을 찾는 것입니다.

Convergence는 series와 sequences 연구에서 수학적으로 가장 일반적인 용어입니다. `loss = 0`이 실제로 달성되지 않고 learing rate가 계속 작아진다고 가정하는 경우에 급수가 무한 급수입니다.

모델은 loss가 실제로 감소하는 추세와 함께 최소값(local 또는 global)로 이동할 때 수렴됩니다.

완벽하게 수렴하는 모델을 실제로 만드는 것은 매우 드물지만 수렴은 일반적으로 convexity과 유사한 방식으로 사용됩니다.