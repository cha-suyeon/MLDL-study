## cs231 lecture 5

- Q. Downsampling을 하는 이유는 무엇인가요? size가 작아지는 것을 막기 위해 padding을 하는데, 왜 pooling을 통해 또 줄이는 걸까요?
- A. Pooling을 사용하는 이유는 앞선 layer들(Conv layer, Activation, etc... )을 거치고 나서 나온 output feature map의 **모든 data가 필요하지 않기 때문**입니다.

    즉, inference를 하는데 있어 적당량의 data만 있어도 되기 때문입니다.

### Pooling의 효과

1. parameter를 줄이기 때문에, 해당 network의 표현력이 줄어들어 overfitting을 막습니다.
2. Parameter를 줄이므로, 그만큼 비례하여 computation이 줄어들어서 hardware resource(energy)를 절약하고 속도가 향상됩니다.

### Pooling의 특징

1. training을 통해 train되어야 할 parameter가 없습니다.
2. Pooling의 결과는 channel 수에는 영향이 없으므로 channel 수는 유지됩니다. -> independent
3. input feature map에 변화(shift)가 있어도 pooling의 결과는 변화가 적습니다. -> robustness