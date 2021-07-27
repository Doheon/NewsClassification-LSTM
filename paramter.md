no | result                                    | max_len | epochs | lstm_n      | fc_n | token  | embedding
---|-------------------------------------------|---------|--------|-------------|------|--------|-------------
1  | loss=0.189, testacc=0.755, trainacc=0.907 | 64      | 200    | 2           | 2    | sp     | fasttext
2  | loss=0.292, testacc=0.788, trainacc=0.857 | 64      | 200    | 2           | 2    | morphs | fasttext
3  | loss=0.539, testacc=0.818, trainacc=0.782 | 64      | 100    | 2           | 2    | morphs | fasttext
4  | loss=0.401, testacc=0.772, trainacc=0.842 | 64      | 100    | 2           | 1    | morphs | fasttext
5  | loss=0.736, testacc=0.788, trainacc=0.749 | 64      | 100    | 1           | 2    | morphs | fasttext
6  | loss=0.512, testacc=0.796, trainacc=0.795 | 64      | 100    | 2(concat h) | 2    | morphs | fasttext
7  | loss=0.453, testacc=0.729, trainacc=0.813 | 32      | 100    | 2           | 2    | morphs | fasttext
8  | loss=0.145, testacc=0.501, trainacc=0.900 | 64      | 100    | 2           | 2    | sp     | nn.Embedding



best: no.3, loss=0.539, testacc=0.818, trainacc=0.782  
정확도는 나쁘지 않지만 긴 문장에 대해서만 훈련을 시켜서 짧은 문장을 직접 작성해서 테스트해보면 좋지 않은 성능을 보인다. 
문장의 길이에 상관없이 고정된 벡터로 문맥을 저장하기 때문에 생긴 문제라고 생각된다.  

max_len을 낮추면 테스트 문장에 대해서는 정확도는 떨어지지만 직접 입력한 문장에 대해서는 더 잘 분류하는 결과가 나왔다.  

모델에 임베딩까지 학습시키면 오버피팅 되는 결과가 나왔고 fasttext를 이용한 결과가 더 좋은 것을 확인했다.  

sentence piece보다 morphs 단위로 tokenize하는 것이 성능이 더 좋게 나왔다  

