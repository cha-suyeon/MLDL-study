## cs231 lecture 7
### about Dropout

- Q1. Dropout의  효과는 무엇인가요? (필요한 이유)
- A1. Dropout은 network의 일부를 중지시킨다는 것과 같은 의미인데요. FC-layer는 대부분의 parameter를 차지하므로, training 중에 neuron이 서로 의존하게 하여 개별 능력이 억제됩니다. 이는 training data의 과적합을 초래합니다. 따라서 Dropout은 일부를 탈락시킴으로서 Overfitting을 방지합니다.

    > 드롭아웃은 뉴런 간의 상호 의존적 학습을 줄이는 데 도움이 되는 신경망의 정규화에 대한 접근 방식입니다.

<br/>

- Q2. BN(Batch Normalization)이 나오고 나서 Dropout은 실제로 잘 안 쓰이나요?
- A2. 


<br/>

- Q3. Dropout은 주로 어디에 위치하는 것이 권장될까요?
- A3. 전반적으로 드롭아웃 레이어가 있는 모델은 BN 모델에 비해 성능이 상당히 좋다고 합니다.

    Data science 분야의 많은 사람들이 BN이 dropout 계층보다 더 잘 작동한다고 신뢰하고 결국 이 두 layer를 비교하려고 시도하지 않습니다. 하지만 Dropout layer가 경우에 따라 BN보다 더 나은 성능을 발휘할 수도 있습니다. 

    중요한 것은 직접 test하고 비교해보는 것입니다. BN은 고급스럽고 복잡한 기술이지만 간단한 Dropout layer도 이미지 데이터와 유사하거나 더 나은 결과를 얻을 수 있습니다.