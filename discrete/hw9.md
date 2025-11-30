## 集合运算求值

1.  $\bigcup \{PPP(\empty), PP(\empty), P(\empty), \empty\}$
    $P(\empty) = \{\empty\}$
    $
    \begin{aligned}
    PP(\empty)
    &= P(\{\empty\}) \\
    &= \{\empty, \{\empty\}\}
    \end{aligned}
    $
    $
    \begin{aligned}
    PPP(\empty)
    &= P(\{\empty, \{\empty\}\}) \\
    &= \{\empty, \{\empty\}, \{\{\empty\}\}, \{\empty, \{\empty\}\}\}
    \end{aligned}
    $
    $
    \begin{aligned}
    \bigcup \{PPP(\empty), PP(\empty), P(\empty), \empty\}
    &= \{\empty, \{\empty\}, \{\{\empty\}\}, \{\empty, \{\empty\}\}\} \\
    &= PPP(\empty)
    \end{aligned}
    $

2.  
    $
    \begin{aligned}
    \bigcap \{PPP(\empty), PP(\empty), P(\empty), \empty\}
    &= \empty
    \end{aligned}
    $

3.  $A = \{\{\empty\}, \{\{\empty\}\}\}$
    $P(A) = \{\empty, \{\{\empty\}\}, \{\{\{\empty\}\}\}, \{\{\empty\}, \{\{\empty\}\}\}\}$
    $\bigcup P(A) = \{\empty, \{\empty\}, \{\{\empty\}\}\}$

4.  $A = \{\{\empty\}, \{\{\empty\}\}\}$
    $\bigcup A = \{\empty, \{\empty\}\}$
    $
    \begin{aligned}
    P(\bigcup A) 
    &= P(\{\empty, \{\empty\}\}) \\
    &= \{\empty, \{\empty\}, \{\{\empty\}\}, \{\empty, \{\empty\}\}\}
    \end{aligned}
    $


## 集合论证明

1.  
    $$
    \begin{align*}
    (A - B) - C
    &= (A - B) \cap -C \\
    &= (A \cap -B) \cap -C \\
    &= A \cap -B \cap -C \\
    &= A \cap (-B \cap -C) \cup (C \cap -C) \\
    &= A \cap -C \cap (-B \cup C) \\
    &= (A - C) \cap -(B \cap -C) \\
    &= (A - C) - (B - C)
    \end{align*}
    $$

2.  
    $$
    \begin{align*}
    A = B
    &\Leftrightarrow (A - A) \cup (A - A) = (A - B) \cup (B - A) \\
    &\Leftrightarrow (A \cap -A) \cup (A \cap -A) = A \oplus B \\
    &\Leftrightarrow \empty \cup \empty = A \oplus B \\
    &\Leftrightarrow A \oplus B = \empty
    \end{align*}
    $$

3.  
    "$A \cap B = \empty \Leftrightarrow A \subseteq -B$"
    $$
    \begin{align*}
    A \cap B = \empty
    &\Leftrightarrow (\forall x)(x \in A \to x \notin B) \\
    &\Leftrightarrow (\forall x)(x \in A \to x \in -B) \\
    &\Leftrightarrow A \subseteq -B
    \end{align*}
    $$
    "$A \cap B = \empty \Leftrightarrow B \subseteq -A$"
    $$
    \begin{align*}
    A \cap B = \empty
    &\Leftrightarrow (\forall x)(x \in B \to x \notin A) \\
    &\Leftrightarrow (\forall x)(x \in B \to x \in -A) \\
    &\Leftrightarrow B \subseteq -A
    \end{align*}
    $$
    $\because (A \cap B = \empty \Leftrightarrow A \subseteq -B) \land (A \cap B = \empty \Leftrightarrow B \subseteq -A)$
    $\therefore A \subseteq -B \Leftrightarrow B \subseteq -A$
    $\therefore A \cap B = \empty \Leftrightarrow A \subseteq -B \Leftrightarrow B \subseteq -A$


## 特殊性质的集合

1.  
    $$
    \begin{align*}
    A - B = B
    &\Leftrightarrow A \cap -B = B \\
    &\Leftrightarrow (A \cap -B) \cap E = B \\
    &\Leftrightarrow (A \cap -B) \cap (B \cup -B) = B \\
    &\Leftrightarrow ((A \cap -B) \cap B) \cup ((A \cap -B) \cap -B) = B \\
    &\Leftrightarrow (A \cap (-B \cap B)) \cup (B \cap -B) = B \\
    &\Leftrightarrow \empty \cup \empty = B \\
    &\Leftrightarrow \empty = B \\
    &\Leftrightarrow A - \empty = \empty \\
    &\Leftrightarrow A \cap -\empty = \empty \\
    &\Leftrightarrow A \cap E = \empty \\
    &\Leftrightarrow A = \empty
    \end{align*}
    $$

    $A = \empty, B = \empty$

2.  
    $$
    \begin{align*}
    A - B = B - A
    &\Leftrightarrow A \cap -B = B \cap -A \\
    &\Leftrightarrow (A \cap -B) \cap E = B - A \\
    &\Leftrightarrow (A \cap -B) \cap (B \cup -B) = B - A \\
    &\Leftrightarrow ((A \cap -B) \cap B) \cup ((A \cap -B) \cap -B) = B - A \\
    &\Leftrightarrow (A \cap (-B \cap B)) \cup ((B \cap -A) \cap -B) = B - A \\
    &\Leftrightarrow (A \cap \empty) \cup ((B \cap -B) \cap -A) = B - A \\
    &\Leftrightarrow \empty \cup (\empty \cap -A) = B - A \\
    &\Leftrightarrow \empty \cup \empty = B - A \\
    &\Leftrightarrow \empty = B \cap -A \\
    &\Leftrightarrow (\forall x)(x \in B \to x \notin -A) \\
    &\Leftrightarrow (\forall x)(x \in B \to x \in A) \\
    &\Leftrightarrow B \subseteq A \\
    &\Leftrightarrow A \cap -B = \empty \\
    &\Leftrightarrow (\forall x)(x \in A \to x \notin -B) \\
    &\Leftrightarrow (\forall x)(x \in A \to x \in B) \\
    &\Leftrightarrow A \subseteq B \\
    &\Leftrightarrow A = B
    \end{align*}
    $$

    $A = B$

3.  
    $$
    \begin{align*}
    A \cap B = A \cup B
    &\Leftrightarrow (\forall x)((x \in A \land x \in B) \leftrightarrow (x \in A \lor x \in B)) \\
    &\Leftrightarrow (\forall x)(((x \in A \land x \in B) \land (x \in A \lor x \in B)) \lor ((x \notin A \lor x \notin B) \land (x \notin A \land x \notin B))) \\
    &\Leftrightarrow (\forall x)((x \in A \land ((x \in B \land x \in A) \lor (x \in B \lor x \in B))) \lor (((x \notin A \land x \notin A) \lor (x \notin B \land x \notin A)) \land x \notin B)) \\
    &\Leftrightarrow (\forall x)((x \in A \land ((x \in B \land x \in A) \lor x \in B)) \lor ((x \notin A \lor (x \notin B \land x \notin A)) \land x \notin B)) \\
    &\Leftrightarrow (\forall x)(((x \in B \land x \in A \land x \in A) \lor (x \in B \land x \in A)) \lor ((x \notin A \land x \notin B) \lor (x \notin B \land x \notin A \land x \notin B))) \\
    &\Leftrightarrow (\forall x)(((x \in B \land x \in A) \lor (x \in B \land x \in A)) \lor ((x \notin A \land x \notin B) \lor (x \notin A \land x \notin B))) \\
    &\Leftrightarrow (\forall x)((x \in A \land x \in B) \lor (x \notin A \land x \notin B)) \\
    &\Leftrightarrow (\forall x)(x \in A \leftrightarrow x \in B) \\
    &\Leftrightarrow A = B
    \end{align*}
    $$

    $A = B$

4.  
    $$
    \begin{align*}
    A \oplus B = A
    &\Leftrightarrow (\forall x)(x \in A \veebar x \in B \leftrightarrow x \in A) \\
    &\Leftrightarrow (\forall x)((x \in A \lor x \in B) \land (x \notin A \lor x \notin B) \leftrightarrow x \in A) \\
    &\Leftrightarrow (\forall x)(((x \in A \lor x \in B) \land (x \notin A \lor x \notin B) \land x \in A) \lor (((x \in A \land x \in B) \lor (x \notin A \land x \notin B)) \land x \notin A)) \\
    &\Leftrightarrow (\forall x)(((x \in A \lor x \in B) \land ((x \notin A \land x \in A) \lor (x \notin B \land x \in A))) \lor (((x \in A \land x \notin A) \land x \in B) \lor (x \notin A \land x \notin B \land x \notin A))) \\
    &\Leftrightarrow (\forall x)(((x \in A \lor x \in B) \land x \notin B \land x \in A) \lor (x \notin A \land x \notin B)) \\
    &\Leftrightarrow (\forall x)((((x \in A \land x \notin B) \lor (x \in B \land x \notin B)) \land x \in A) \lor (x \notin A \land x \notin B)) \\
    &\Leftrightarrow (\forall x)((x \in A \land x \notin B \land x \in A) \lor (x \notin A \land x \notin B)) \\
    &\Leftrightarrow (\forall x)((x \in A \land x \notin B) \lor (x \notin A \land x \notin B)) \\
    &\Leftrightarrow (\forall x)(x \notin B \land (x \in A \lor x \notin A)) \\
    &\Leftrightarrow (\forall x)(x \notin B) \\
    &\Leftrightarrow B = \empty
    \end{align*}
    $$

    $B = \empty$


## 集合命题成立的充要条件

1.  
    $$
    \begin{align*}
    (A - B) \cup (A - C) = A
    &\Leftrightarrow (A \cap -B) \cup (A \cap -C) = A \\
    &\Leftrightarrow A \cap (-B \cup -C) = A \\
    &\Leftrightarrow A \subseteq (-B \cup -C) \\
    \end{align*}
    $$

2.  
    $$
    \begin{align*}
    (A - B) \oplus (A - C) = \empty
    &\Leftrightarrow A - B = A - C \\
    &\Leftrightarrow A - (A - B) = A - (A - C) \\
    &\Leftrightarrow A \cap -(A \cap -B) = A \cap -(A \cap -C) \\
    &\Leftrightarrow A \cap (-A \cup B) = A \cap (-A \cup C) \\
    &\Leftrightarrow (A \cap -A) \cup (A \cap B) = (A \cap -A) \cup (A \cap C) \\
    &\Leftrightarrow A \cap B = A \cap C
    \end{align*}
    $$


## 集合的笛卡尔积

1.  
    $$
    \begin{align*}
    A \times B = \empty
    \Leftrightarrow A = \empty \lor B = \empty
    \end{align*}
    $$

2.  
    $$
    \begin{align*}
    A = A \times A 可满足，A = \empty
    \end{align*}
    $$


## 有限集合的基数

1.  
    $
    \begin{aligned}
    A = \{x|x \in \mathbb{N}, x \leq 250, x \bmod{2} = 0\} \\
    B = \{x|x \in \mathbb{N}, x \leq 250, x \bmod{3} = 0\} \\
    C = \{x|x \in \mathbb{N}, x \leq 250, x \bmod{5} = 0\}
    \end{aligned}
    $

    $$
    \begin{align*}
    |A \cup B \cup C|
    &= |A| + |B| + |C| - |A \cap B| - |A \cap C| - |B \cap C| + |A \cap B \cap C| \\
    &= 125 + 83 + 50 - 41 - 25 - 16 + 8 \\
    &= 184
    \end{align*}
    $$