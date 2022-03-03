## cs231 lecture 5
### about CNN Architecture

- Q1. 왜 layer가 Conv layer와 Pooling Layer가 반복되며 나올까요?
- A1. CNN 마지막 부분에는 이미지 분류를 위한 Fully Connected layer가 추가됩니다. 이미지의 특징을 추출하는 부분과 이미지를 분류하는 부분 사이에 이미지 형태의 데이터를 배열 형태로 만드는 Flatten layer가 위치 합니다.

<br/>

- Q2. 마지막에는 Fully Connected Layer를 사용하는 이유는 뭘까요?
- A2. Flatten Layer는 CNN의 데이터 타입을 Fully Connected Neural Network의 형태로 변경하는 layer입니다. Flatten layer에는 parameter가 존재하지 않고, 입력 데이터의 Shape 변경만 수행합니다.