## cs231 lecture 10
### about RNN architecture

![img.png](img.png)

- Q. many-to-one RNN architecture를 적용하기 더 좋은 task 2개는?
1. Speech recognition (input an audio clip and output a transcript)
2. Sentiment classification (input a piece of text and output a 0/1 to denote positive or negative sentiment)
3. Gender recognition from speech (input an audio clip and output a label indicating the speaker’s gender)
4. Image classification (input an image and output a label)

- A. 2, 3
- 이유: a의 경우 Many-to-many는 각 time step마다 모두 output이 나오는 구조이고, audio clip이 transcript로 출력되는 것도 many-to-many에 속합니다.
