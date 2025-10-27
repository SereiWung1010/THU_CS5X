## 判断公式

1. 普遍有效
2. 普遍有效
3. 可满足
4. 不可满足
5. 可满足
6. 普遍有效
7. 可满足

## 语句的符号化

1.  $$
    \begin{align*}
    令 & L(x):x是直线; \\
    & P(x):x是一个点 \\
    & E(x, y):x等于y \\
    & T(l, x, y):l通过x和y
    \end{align*}
    $$

    $过平面上两个点，有且仅有一条直线通过$
    $\quad (\forall x)(\forall y)((P(x) \land P(y)) \to (\exists l)((L(l) \land T(l, x, y)) \land (\forall m)((L(m) \land T(m, x, y)) \to (E(l, m)))))$

2.  $$
    \begin{align*}
    令 & R(x):x是实数 \\
    & G(x, y):x大于y \\
    & E(x, y):x等于y
    \end{align*}
    $$

    $凡实数都能比较大小。$
    $\quad (\forall x)(\forall y)((R(x) \land R(y)) \to (G(x, y) \lor G(y, x) \lor E(x, y)))$

3.  $$
    \begin{align*}
    令 & P(x):x是人 \\
    & W(x):x在北京工作 \\
    & B(x):x是北京人
    \end{align*}
    $$

    $在北京工作的人未必都是北京人。$
    $\quad (\exists x)(P(x) \land (W(x) \land \neg B(X)))$

4.  $$
    \begin{align*}
    令 & M(x):x是金属 \\
    & L(x):x是液体 \\
    & D(x, y):x可以溶解y
    \end{align*}
    $$

    $任何金属都可溶解在某种液体内。$
    $\quad (\forall x)(\exists y)(M(x) \land L(y) \land D(y, x))$

## 将谓词公式翻译成自然语言

1. 所有的正整数都是有理数和实数
2. 所有的正整数都是有理数而且不是所有的有理数都是正整数

## 谓词公式写成命题逻辑公式

1.  $(\forall x)(\exists y)(P(x, y) \to Q(x, y))$
    $((P(a, a) \to Q(a, a)) \lor (P(a, b) \to Q(a, b)) \lor (P(a, c) \to Q(a, c))) \land ((P(b, a) \to Q(b, a)) \lor (P(b, b) \to Q(b, b)) \lor (P(b, c) \to Q(b, c))) \land ((P(c, a) \to Q(c, a)) \lor (P(c, b) \to Q(c, b)) \lor (P(c, c) \to Q(c, c)))$

2.  $(\exists x)(\exists y)P(x, y)$
    $P(a, a) \lor P(a, b) \lor P(a, c) \lor P(b, a) \lor P(b, b) \lor P(b, c) \lor P(c, a) \lor P(c, b) \lor P(c, c)$

3. $(\forall y)((\exists x)P(x, y) \to (\forall x) Q(x, y))$
    $(((P(a, a) \to Q(a, a)) \land (P(a, a) \to Q(b, a)) \land (P(a, a) \to Q(c, a))) \lor ((P(b, a) \to Q(a, a)) \land (P(b, a) \to Q(b, a)) \land (P(b, a) \to Q(c, a))) \lor ((P(c, a) \to Q(a, a)) \land (P(c, a) \to Q(b, a)) \land (P(c, a) \to Q(c, a)))) \land (((P(a, b) \to Q(a, b)) \land (P(a, b) \to Q(b, b)) \land (P(a, b) \to Q(c, b))) \lor ((P(b, b) \to Q(a, b)) \land (P(b, b) \to Q(b, b)) \land (P(b, b) \to Q(c, b))) \lor ((P(c, b) \to Q(a, b)) \land (P(c, b) \to Q(b, b)) \land (P(c, b) \to Q(c, b)))) \land (((P(a, c) \to Q(a, c)) \land (P(a, c) \to Q(b, c)) \land (P(a, c) \to Q(c, c))) \lor ((P(b, c) \to Q(a, c)) \land (P(b, c) \to Q(b, c)) \land (P(b, c) \to Q(c, c))) \lor ((P(c, c) \to Q(a, c)) \land (P(c, c) \to Q(b, c)) \land (P(c, c) \to Q(c, c))))$