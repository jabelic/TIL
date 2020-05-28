# Adams法
数値計算


- 線形多段法の一種。

## Adams-Bashforth法

$$
\frac{dy}{dx} = f(x, y)
$$
は
$$
y(x_{k+1}) = y(x_k) + \int_{x_k}^{x_{k+1}} f(x, y(x)) dx
$$
と同値である。したがって、知っている情報を用いて、右側の積分を近似的に表現することにより、次のステップの$y$に対する近似値 $y_{k+1}$を求めることができる.

### Lagrangeの補間多項式

予備知識。
$(n+1)$個の異なる$x$座標 $x_0, x_1, ..., x_n$に対して $y$座標$y_0, y_1, ..., y_n$が与えられた時, これらすべての点を通過する$n$次の多項式$P_n(x)$, すなわち

$$
P_n(x) = a_0 + a_1 x + a_1 x^2 + \cdots + a_n x_n\ \ \ \ (a_n \not =0)\\
P_n(x_i) = y_i\ \ \ \ (i = 0,1,...,n)
$$

を満たすような$P_n(x)$がただ一つ存在する.

-----

$$
\begin{align}
L_i(x) &= \prod^n_{j=0\\j\not=i} \frac{(x - x_j)}{(x_i - x_j)}\\
&= \frac{(x - x_0)(x-x_1)\cdots(x - x_{i-1})(x - x_{i+1})\cdots (x- x_{n})}{(x_i - x_0)(x_i - x_1)\cdots (x_i - x_{i-1})(x_i - x_{i+1})\cdots (x_i - x_n)}\ \ \ (i = 0,1,...,n)\\
\end{align}
$$


を定義する. $L_i (x)$は明らかに$n$次の多項式で
$$
\begin{equation*}
L_i(x_k) = \delta_{ik}=
      \left\{
      \begin{aligned}
             1 \hspace{5mm}\mbox{if}\ i = k\\
             0 \hspace{5mm} \mbox{if}\ i\not= k\\
      \end{aligned}
      \right.
  \end{equation*}
$$

が成り立つ.

このように定義された $L_i (x)\ \ (i = 0,1,...,n)$を用いると, 求める補間多項式$P_n(x)$は明らかに
$$
P_n(x)= \sum_{i=0}^n y_i L_i(x)\\
$$

のように表すことができる. この$P_n(x)$はLagrangeの補間多項式(Lagrange interpolation polyno-mial)と呼ばれる.








