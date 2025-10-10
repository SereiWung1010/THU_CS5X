## 命题的基本概念

1. 
    - |$P$|$P \to P$|
        |:-:|:-:|
        |0|1|
        |1|1|

    - $(P \lor Q) \to (P \lor Q)$

        $= R \to R \quad (代入规则,R = (P \lor Q))$

        $= T \quad\quad\quad (等幂律)$

    - |$P$|$Q$|$P \lor Q$|$Q \lor P$|$\lnot ((P \lor Q) \to (Q \lor P))$|
        |:-:|:-:|:-:|:-:|:-:|
        |0|0|0|0|0|
        |0|1|1|1|0|
        |1|0|1|1|0|
        |1|1|1|1|0|

        $\lnot ((P \lor Q) \to (Q \lor P)) = F$

2. 
    - 非命题
    - 命题：假
    - 非命题

## 波兰式和逆波兰式

1.
    - $P \lor Q \to R \lor S$

        $P \lor Q \to \lor R S$

        $\lor P Q \to \lor R S$

        $\to \lor P Q \lor R S$
    
    - $\lnot P \land R \leftrightarrow P \land Q$

        $\lnot P \land R \leftrightarrow \land P Q$

        $\land \lnot P R \leftrightarrow \land P Q$

        $\leftrightarrow \land \lnot P R \land P Q$

    - $\lnot \lnot P \lor (W \land R) \lor \lnot Q$

        $\lnot \lnot P \lor \land W R \lor \lnot Q$

        $\lnot \lnot P \lor \lor \land W R \lnot Q$

        $\lor \lnot \lnot P \lor \land W R \lnot Q$

    - $P \land (Q \to \lnot R)$

        $P \land \to Q \lnot R$

        $\land P \to Q \lnot R$


## 等值公式的证明

1. 
    -   $$
        \begin{align*}
        P \to Q 
        &= \neg P \lor Q        &&& 蕴涵等值式 \\
        &= Q \lor \neg P        &&& 交换律 \\
        &= \neg Q \to \neg P    &&& 蕴涵等值式
        \end{align*}
        $$

    -   $$
        \begin{align*}
        ((P \to \neg Q) \to (Q \to \neg P)) \land R
        &= ((Q \to \neg P) \to (Q \to \neg P)) \land R  & 假言易位 \\
        &= (Q \to (\neg P \to \neg P)) \land R          & 分配律 \\
        &= (Q \to T) \land R                            & 等幂律 \\
        &= T \land R                                    & 零律 \\
        &= R                                            & 同一律
        \end{align*}
        $$

    -   $$
        \begin{align*}
        (P \leftrightarrow Q) \leftrightarrow ((P \land \neg Q) \lor (Q \land \neg P))
        &= (P \leftrightarrow Q) \leftrightarrow ((\neg P \land Q) \lor (P \land \neg Q))       & 交换律 \\
        &= (P \leftrightarrow Q) \leftrightarrow \neg P \leftrightarrow Q                       & 摩根律 \\
        &= \neg P \leftrightarrow (P \leftrightarrow Q) \leftrightarrow Q                       & 交换律 \\
        &= (\neg P \leftrightarrow P) \leftrightarrow Q \leftrightarrow Q                       & 结合律 \\
        &= F \leftrightarrow Q \leftrightarrow Q                                                & 补余律 \\
        &= \neg Q \leftrightarrow Q                                                             & 同一律 \\
        &= F                                                                                    & 补余律 \\
        &= P \land \neg P                                                                       & 补余律
        \end{align*}
        $$
    
    -   $$
        \begin{align*}
        P \to (Q \to R)
        &= \neg P \lor (Q \to R)            & 蕴涵等值式 \\
        &= \neg P \lor (\neg Q \lor R)      & 蕴涵等值式 \\
        &= (\neg P \lor \neg Q) \lor R      & 结合律 \\
        &= \neg (P \land Q) \lor R          & 摩根律 \\
        &= (P \land Q) \to R                & 蕴涵等值式
        \end{align*}
        $$

## 由真值表写表达式

1. 
    -   |$P$|$Q$|$\neg P \land \neg Q$|$\neg P \land Q$|$P \land \neg Q$|$P \land Q$|$A$|
        |:--|:--|:--|:--|:--|:--|:--|
        |0|0|1|0|0|0|1|
        |0|1|0|1|0|0|0|
        |1|0|0|0|1|0|0|
        |1|1|0|0|0|1|0|

        $A = \neg P \land \neg Q$
    
    -   |$P$|$Q$|$\neg P \land \neg Q$|$\neg P \land Q$|$P \land \neg Q$|$P \land Q$|$B$|
        |:--|:--|:--|:--|:--|:--|:--|
        |0|0|1|0|0|0|1|
        |0|1|0|1|0|0|1|
        |1|0|0|0|1|0|0|
        |1|1|0|0|0|1|1|

        $B = (\neg P \land \neg Q) \lor (\neg P \land Q) \lor (P \land Q)$
        $B = \neg P \land (\neg Q \lor Q) \lor (P \land Q) \quad\quad\quad (分配律)$
        $B = \neg P \land T \lor (P \land Q) \quad\quad\quad(补余律)$
        $B = \neg P \lor (P \land Q) \quad\quad\quad (同一律)$
        $B = (\neg P \lor P) \land (\neg P \land Q) \quad\quad\quad (分配律)$
        $B = T \land (\neg P \land Q) \quad\quad\quad (补余律)$
        $B = \neg P \land Q \quad\quad\quad (同一律)$
    
    -   |$P$|$Q$|$\neg P \lor \neg Q$|$\neg P \lor Q$|$P \lor \neg Q$|$P \lor Q$|$A$|
        |:--|:--|:--|:--|:--|:--|:--|
        |0|0|1|1|1|0|1|
        |0|1|1|1|0|1|0|
        |1|0|1|0|1|1|0|
        |1|1|0|1|1|1|0|

        $A = (\neg P \lor \neg Q) \land (\neg P \lor Q) \land (P \land \neg Q)$
        $A = \neg P \lor (\neg Q \lor Q) \land (P \land \neg Q) \quad\quad\quad (分配律)$
        $A = \neg P \lor T \land (P \land \neg Q) \quad\quad\quad (补余律)$
        $A = T \land (P \land \neg Q) \quad\quad\quad (零律)$
        $A = P \land \neg Q \quad\quad\quad (同一律)$
    
    -   |$P$|$Q$|$\neg P \lor \neg Q$|$\neg P \lor Q$|$P \lor \neg Q$|$P \lor Q$|$B$|
        |:--|:--|:--|:--|:--|:--|:--|
        |0|0|1|1|1|0|1|
        |0|1|1|1|0|1|1|
        |1|0|1|0|1|1|0|
        |1|1|0|1|1|1|1|

        $B = \neg P \lor Q$

## $\uparrow$和$\downarrow$的完备性

1. 
    -   用 $\uparrow$ 表示 $\neg P$
        $$
        \begin{align*}
        \neg P
        &= \neg (P \land P)     & (等幂律) \\
        &= P \uparrow P         & (与非定义)
        \end{align*}
        $$
    
    -   用 $\uparrow$ 表示 $P \land Q$
        $$
        \begin{align*}
        P \land Q
        &= \neg (\neg (P \land Q))                  & (双重否定率) \\
        &= \neg (P \uparrow Q)                      & (与非定义) \\
        &= (P \uparrow Q) \uparrow (P \uparrow Q)   & (非定义)
        \end{align*}
        $$
    
    -   用 $\uparrow$ 表示 $P \lor Q$
        $$
        \begin{align*}
        P \lor Q
        &= \neg (\neg P \land \neg Q)               & (摩根律) \\
        &= \neg P \uparrow \neg Q                   & (与非定义) \\
        &= (P \uparrow P) \uparrow (Q \uparrow Q)   & (非定义)
        \end{align*}
        $$
    
    -   用 $\uparrow$ 表示 $P \to Q$
        $$
        \begin{align*}
        P \to Q
        &= \neg P \lor Q                                                    & (蕴涵等值式) \\
        &= (P \uparrow P) \lor Q                                            & (非定义) \\
        &= ((P \uparrow P) \uparrow (P \uparrow P)) \uparrow (Q \uparrow Q) & (或定义)
        \end{align*}
        $$
    
    -   用 $\downarrow$ 表示 $\neg P$
        $$
        \begin{align*}
        \neg P
        &= \neg (P \lor P)       & (等幂律) \\
        &= P \downarrow P       & (或非定义)
        \end{align*}
        $$
    
    -   用 $\downarrow$ 表示 $P \land Q$
        $$
        \begin{align*}
        P \land Q
        &= \neg (\neg P \lor \neg Q)                        & (摩根律) \\
        &= \neg P \downarrow \neg Q                         & (或非定义) \\
        &= (P \downarrow P) \downarrow (Q \downarrow Q)     & (非定义)
        \end{align*}
        $$
    
    -   用 $\downarrow$ 表示 $P \lor Q$
        $$
        \begin{align*}
        P \lor Q
        &= \neg (\neg (P \lor Q))                           & (双重否定率) \\
        &= \neg (P \downarrow Q)                            & (或非定义) \\
        &= (P \downarrow Q) \downarrow (P \downarrow Q)     & (非定义)
        \end{align*}
        $$
    
    -   用 $\downarrow$ 表示 $P \to Q$
        $$
        \begin{align*}
        P \to Q
        &= \neg P \lor Q                & (蕴涵等值式) \\
        &= (P \downarrow P) \lor Q      & (非定义) \\
        &= ((P \downarrow P) \downarrow Q) \downarrow ((P \downarrow P) \downarrow Q)   &(或定义)
        \end{align*}
        $$