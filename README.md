# NewsClassification-LSTM

explain: <https://doheon.github.io/%EC%BD%94%EB%93%9C%EA%B5%AC%ED%98%84/nlp/ci-lstm-post/>

# Result

accuracy: 81.8%

```python
test_model("신형 아이패드 프로에 m1칩 탑재 예정", lstm, hannanum.morphs, model_morphs.wv)
```

```
뉴스의 카테고리는: 기술/IT
['정치:0.00%', '경제:0.16%', '사회:0.15%', '생활/문화:3.64%', '세계:0.12%', '기술/IT:94.37%', '연예:0.13%', '스포츠:1.42%']
신뢰도는: 94.37%
```

