## cs231 lecture 6
### about Strategy and the curse of dimensionality

### 개념

![img_5.png](img_5.png)

최상의 구성을 찾는데 네 가지 주요 전략이 있다고 합니다.

- **Babysitting (aka Trial & Error)**
- **Grid Search**
- **Random Search**
- **Bayesian Optimization**

이때 질문 하나가 나옵니다.

- 최적의 하이퍼 파라미터를 찾는데 시간을 투자하는 것보다 더 좋은 방법이 있나요?

그 방법으로 

- Grid Search
- Random Search
- Bayesian Optimization

이 세 가지가 제안됩니다.

![img_6.png](img_6.png)

위 두 가지는 강의에서 내용이 다뤄졌습니다.

이 이미지는 두 개의 하이퍼파라미터 공간에서 최상의 구성을 검색하여 두 가지 접근 방식을 비교합니다. 또한 한 매개변수가 다른 매개변수보다 더 중요하다고 가정합니다.

이미지의 각 레이아웃 상단에 있는 공간 탐색에서 알 수 있듯이 무작위 검색(특히 더 중요한 변수의 경우)을 통해 하이퍼파라미터 공간을 더 광범위하게 탐색했습니다. 이렇게 하면 더 적은 수의 반복으로 최상의 구성을 찾는 데 도움이 됩니다.

- Q. searching space에 3~4개 이상의 차원이 포함된 경우 그리드 검색을 사용하면 안 됩니다. high spaces에서는 아주 나쁜 성능을 보여주는데요. 그 이유는 무엇일까요?
- A. grid 검색의 경우 차원의 저주에 빠지게 됩니다. 더 많은 차원을 추가할수록 검색하는데 시간 복잡도가 폭발하면서 이 전략을 실행 불가능하게 만듭니다. 차원이 4보다 작거나 같을 때 grid를 사용하는 것이 일반적이며, 마지막에 최상의 값을 찾는다고 하더라도 권장되진 않습니다. 대신에 random search를 사용합니다.
- `+`: grid 검색의 경우 하이퍼파라미터를 고정된 값으로 sampling하기 때문에 어떤 하이퍼파라미터가 중요한지 판단할 수 없습니다. 하지만 random의 경우, 더 다양한 값을 sampling 할 수 있어서 더 중요한 하이퍼파라미터를 찾는 것이 가능합니다.
