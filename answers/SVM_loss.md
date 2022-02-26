## cs231 Lecture 3
### Slide 15


![img.png](img.png)

- Q. 해당 슬라이드에서 Car score가 cat score보다 높아서 loss가 0이 됩니다. 그것은 무엇을 의미하는 것인가요?
- A. SVM loss의 경우 max(0, s_j, s_yi+1)로 계산됩니다. s_yi가 정답 스코어입니다. 그래서 더 잘 예측할 수록(위의 슬라이드 기준으로 car score가 cat, frog score보다 더 높은 경우) s_j, s_yi+1는 음수를 가질 가능성이 더 커지겠죠. 여기서 1은 noise를 의미합니다(safety margin). 그래서 음수값을 가진다는 건 잘 분류했다는 뜻이고 loss는 max 공식에 의해 0을 갖게 됩니다.
