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
��Ȯ���� ������ ������ �� ���忡 ���ؼ��� �Ʒ��� ���Ѽ� ª�� ������ ���� �ۼ��ؼ� �׽�Ʈ�غ��� ���� ���� ������ ���δ�. 
������ ���̿� ������� ������ ���ͷ� ������ �����ϱ� ������ ���� ������� �����ȴ�.  

max_len�� ���߸� �׽�Ʈ ���忡 ���ؼ��� ��Ȯ���� ���������� ���� �Է��� ���忡 ���ؼ��� �� �� �з��ϴ� ����� ���Դ�.  

�𵨿� �Ӻ������� �н���Ű�� �������� �Ǵ� ����� ���԰� fasttext�� �̿��� ����� �� ���� ���� Ȯ���ߴ�.  

sentence piece���� morphs ������ tokenize�ϴ� ���� ������ �� ���� ���Դ�  

