# BasicNLP

<details>
<summary>Seq2Seq with LSTM으로 독일어->영어 번역</summary>


torchtext.data가 Field를 지원하지 않는다.

train, test set을 설정하는 코드를 다시 짜야한다.

무사히 vocab dic에 unk, sos, eos token을 추가하고 한 문장을 숫자로 표현할 수 있게 됐다.
이제 이걸 tensor로 변환해서 모델에 훈련시켜야 한다...
tensor로 바꾼다고 해도 각 문장의 길이가 다르다. 길이를 가장 긴 문장에 맞춰야 한다.
긴 문장에 맞추는 방법은 예제 코드 중 RNN for Text Classification.ipynb에 있었다. 그런데 여기선 keras를 썼는데 torch로 하는 방법이 없을까?

torch.nn.utils.rnn.pad_sequence를 써서 배치에서 길이가 가장 긴 문장에 텐서 크기를 맞췄다.
학습 시켜봤지만 예측에서 가장 크기가 작은 벡터만 결과값으로 나온다.
학습을 잘못했는지 아니면 예측을 잘못했는지 모르겠다.

</details>