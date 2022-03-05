## cs231 lecture 5

![img_5.png](img_5.png)

- Q. padding에서 zero-padding을 많이 사용하는 이유는 무엇일까요?
- A. filter 내부에 zero padding 을 추가해서 강제로 Receptive Field 를 늘립니다.

  위 그림에서 진한 파란색 부분만 weight가 있고 나머지 부분은 0으로 채워집니다.

  이 Receptive Field는 filter가 한 번 보는 영역으로 사진의 Feature를 파악하고 추출하기 위해서 넓은 Receptive Field를 사용하는 것이 좋습니다. 

    Dimension 손실이 적고, 대부분의 weight 가 0 이기 때문에 연산의 효율이 좋다집니다.

    그래서 zero-padding은 공간적 특징을 유지하는 Segmentation에서 주로 사용됩니다.