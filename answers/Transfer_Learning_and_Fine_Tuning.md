## cs231 lecture 7
### about Transfer Learning & Fine Tuning

- Q. Transfer Learning & Fine Tuning의 차이가 무엇일까요?
- A. transfer learning이란 학습된 가중치 혹은 그 일부를 다른 신경망에 복사한 다음, 그 상태로 재학습을 수행합니다. 예를 들어, VGG와 구성이 같은 신경망을 준비하고, 미리 학습된 가중치를 초깃값으로 설정한 후, 새로운 데이터셋을 대상으로 재학습(fine tuning)을 수행합니다. transfer learning은 보유한 데이터셋이 적을 때 특히 유용한 방법입니다. Fine Tuning은 기존의 신경망을 이용한 재학습 과정을 의미합니다.