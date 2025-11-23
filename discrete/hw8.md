## 式子化简

1. $\varnothing$
2. $\{\varnothing, \{\varnothing\}\}$
3. $\{\{\varnothing\}\}$
4. $\{\varnothing\}$


## 集合元素列举

1.  $A = \{z | z = \{x, y\} \land x \in \mathbb{Z} \land y \in \mathbb{Z} \land 0 \le x \le 2 \land -2 \le y \le 1 \}$
    $A = \{\{0, -2\}, \{0, -1\}, \{0, 0\}, \{0, 1\}, \{1, -2\}, \{1, -1\}, \{1, 0\}, \{1, 1\}, \{2, -2\}, \{2, -1\}, \{2, 0\}, \{2, 1\}\}$


## 集合表达式书写

1.  $\{3, 5, 7, 11, 13, 17, 19, 23, 29\}$
    $\{x | x是大于2的质数\}$


## 集合举例

1.  $A \in B, B \in C, A \notin C$
    $A = \{1\}, B = \{\{1\}, 2\}, C = \{\{\{1\}, 2\}\}$

2.  $A \in B, B \in C, A \in C$
    $A = \{1\}, B = \{\{1\}, 2\}, C = \{\{1\}, \{\{1\}, 2\}\}$


## 判断集合命题的真假

1.  $若 A \in B 且 B \subseteq C 则 A \in C$
    $\because B \subseteq C \Leftrightarrow (\forall x)(x \in B \to x \in C)$
    $\therefore A \in B \to A \in C$
    $\because A \in B$
    $\therefore A \in C$

2.  $若 A \in B 且 B \sub C 则 A \subseteq C$
    $A = 1, B = \{1\}, C = \{1, 2\}$
    $A不是集合,所以不可能是C的子集$


## 幂集的书写

1.  $P(\{a, \{a\}\}) = \{\varnothing, \{a\}, \{\{a\}\}, \{a, \{a\}\}\}$

2. $P(\{\varnothing, a, \{b\}\}) = \{\varnothing, \{\varnothing\}, \{a\}, \{\{b\}\}, \{\varnothing, a\}, \{\varnothing, \{b\}\}, \{a, \{b\}\}, \{\varnothing, a, \{b\}\}\}$


## 文氏图的绘画与表示

2. $-A \cap (B \cap C)$


## 集合的运算

1. $\{2, 3, 4, 5\}$

2. $\{\{4\}, \{1, 4\}\}$