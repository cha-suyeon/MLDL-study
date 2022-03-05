## cs231 lecture 10
### about LSTM and GRU

- Q. feedback RNN과 LSTM/GRU의 차이점
- A. 모든 RNN은 recurrent layer에 feedback loop를 가지고 있습니다. 이를 통해 시간이 지남에 따라 'memory'에 정보를 유지할 수 있습니다.

    그러나 long-term temporal dependencies을 학습해야 하는 문제를 해결하기 위해 Standard RNN을 훈련 시키는 것은 어렵습니다.

    이는 loss function의 gradient가 시간에 따라 기하급수적으로 감소하기 때문입니다. 이를 Vanishing Gradient라고 합니다.

    LSTM 네트워크는 표준 단위 외에 특수 단위를 사용하는 RNN 유형입니다. LSTM 유닛에는 long-term 동안 정보를 memory에 유지할 수 있는 'memory cell'이 포함됩니다.

    gate set는 정보가 메모리에 입력(input)되는 시기, 정보가 출력(output)되는 시기 및 잊혀지는(forget) 시기를 제어하는 데 사용됩니다.

    이 architecture를 통해 장기적인 종속성을 학습할 수 있습니다. GRU는 LSTM과 유사하지만 단순화된 구조를 사용합니다.