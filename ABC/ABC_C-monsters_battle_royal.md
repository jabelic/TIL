### ABC C-Monsters Battle Royal
[C-Monsters Battle Royale](https://atcoder.jp/contests/abc118/tasks/abc118_c)

いわば最大公約数を求める問題だが、少し困ったことがあったのでメモを残す。

`RE`
```python
 import functools
 import math
 N = int(input())
 monster = [int(i) for i in input().split()]
 print(abs(functools.reduce(math.gcd,monster)))
```

`AC`
```python
 import functools
 import fractions
 N = int(input())
 monster = [int(i) for i in input().split()]
 print(abs(functools.reduce(fractions.gcd,monster)))
```

`gcd()`関数は3.4以前では`fractions`モジュールにあり、3.5からは`math`モジュールにある
（[9.5. fractions — 有理数¶](https://docs.python.org/ja/3.5/library/fractions.html)による）