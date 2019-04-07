### ABC081 C-Not so Diverse

```python

```

import collections
from operator import itemgetter
N,K = map(int,input().split())
ball = [int(j) for j in input().split()]

kind = dict(collections.Counter(ball))

if len(kind) <= K:
    print(0)
else:
    skind = sorted(kind.items(),key=itemgetter(1))
    sumNum = 0
    for i in range(len(skind)-K):
        sumNum += skind[i][1]
    print(sumNum)

```

```



### 所感
　`collections` で元とその個数を辞書型で格納。そのとき、`dict()` で囲わないと `Countor({})` となってしまい、その後色々困る。あと、きちんと変数で `dict()` を受け取ること。もとの `Countor({})` に `dict()` は影響しない。
　辞書のソートは厄介。 `skind = sorted(kind.items(),key=lambda x: x[1)` ではうまくいかず。 `lambda` 式のところがうまくいってないらしく、 `skind = sorted(kind.items(),key=operator.itemgetter(1))` でようやくうまくいった。意味は一緒らしいが、はたして何が違うのか？？？