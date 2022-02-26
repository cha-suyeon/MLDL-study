## cs231 lecture 5

![img.png](img.png)

- Q. 1x1 Convolution layer를 사용하는 이유는 무엇일까요?
- A. 1x1 Conv layer를 사용하는 이유는 filter의 수를 조절하려고 쓰는 건데, depth가 동일하면 convolution은 큰 의미가 없습니다.

    그런데 차원(dimension)을 바꿔준다면 차원을 크게도 작게도 만들 수 있습니다.

    입력값에 비해 더 적은 수의 차원으로 바꿔주기 위해, filter의 수로 depth를 조정한다면 차원이 축소된 정보로 연산량을 크게 줄일 수 있습니다.

    한 번 이렇게 줄여두면 뒤로가면 연계되는 연산량의 수, parameter 수가 줄어들어 효율이 높아집니다.