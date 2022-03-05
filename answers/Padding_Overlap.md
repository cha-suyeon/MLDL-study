## cs231 lecture 5

- Q. Pooling은 overlap 하지 않는 것이 일반적이라고 합니다. Pooling을 적용할 때 overlap하여 더 촘촘히 feature를 뽑으면 좋을 것 같은데, 그렇게 하지 않는 이유는 무엇일까요?
- A. overlap을 하면 조금 더 촘촘히 계산하여 특징을 더 많이 뽑아낼 수 있습니다. 해당 알고리즘 모델에 따라 overlap 하기도 합니다.

    다른 CNN 모델에서 Pooling은 일반적으로 filter를 겹치지 않게 Stride를 적절히 조정하여 사용합니다.

    그러나 AlexNet에서는 Stride를 좁혀 Overlapping 하는 구조를 만들었습니다.

    이 경우, 정확도는 약 0.4%가 향상되지만 Overlapping의 사용은 연상량을 증가시켰습니다.