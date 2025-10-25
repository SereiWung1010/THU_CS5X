## 归结法

$$
\begin{align*}
& (S \to \neg Q) \land (P \to Q) \land (R \lor S) \land (R \to \neg Q) \Rightarrow \neg P \\
&= (\neg S \lor \neg Q) \land (\neg P \lor Q) \land (R \lor S) \land (\neg R \lor \neg Q) \Rightarrow \neg P \\ \\
& A = \{\neg S \lor \neg Q, \neg P \lor Q, R \lor S, \neg R \lor \neg Q\} \\
& 1. \neg P \lor Q \\
& 2. \neg S \lor \neg Q \\
& 3. \neg P \lor \neg S & (1)(2) 归结 \\
& 4. R \lor S \\
& 5. \neg P \lor R & (3)(4) 归结 \\
& 6. \neg R \lor \neg Q \\
& 7. \neg P \lor \neg R & (1)(6) 归结 \\
& 8. \neg P & (5)(7) 归结 \\
\end{align*}
$$

## 罗素公理系统

1. 
$$
\begin{align*}
& 证明: \quad \vdash P \to (Q \lor P) \\
& 1. \vdash (Q \to R) \to ((P \lor Q) \to (P \lor R)) & 公里4 \\
& 2. \vdash (Q \to R) \to ((\neg P \lor Q) \to (\neg P \lor R)) & (1) 代入 \dfrac{P}{\neg P} \\
& 3. \vdash (Q \to R) \to ((P \to Q) \to (P \to R)) & (2) 定义1 \\
& 4. \vdash ((P \lor Q) \to (Q \lor P)) \to ((P \to (P \lor Q)) \to (P \to (Q \lor P))) & (3) 代入 \dfrac{Q}{P \lor Q}, \dfrac{R}{Q \lor P} \\
& 5. \vdash (P \lor Q) \to (Q \lor P) & 公理3 \\
& 6. \vdash (P \to (P \lor Q)) \to (P \to (Q \lor P)) & (4), (5) 分离 \\
& 7. \vdash P \to (P \lor Q) & 公理2 \\
& 8. \vdash P \to (Q \lor P) & (6), (7) 分离
\end{align*}
$$

2. 
$$
\begin{align*}
& 证明: \quad \vdash Q \to (P \to Q) \\
& 1. \vdash P \to (Q \lor P) & 第1题结论 \\
& 2. \vdash R \to (\neg P \lor R) & (1) 代入 \dfrac{P}{R}, \dfrac{Q}{\neg P} \\
& 3. \vdash Q \to (\neg P \lor Q) & (2) 代入 \dfrac{R}{Q} \\
& 4. \vdash Q \to (P \to Q) & (3) 定义1
\end{align*}
$$

3. 
$$
\begin{align*}
& 证明: \quad \vdash P \lor \neg P \\
& 1. \vdash P \to (P \lor Q) & 公理2 \\
& 2. \vdash P \to (P \lor P) & (1) 代入 \dfrac{Q}{P} \\
& 3. \vdash (Q \to R) \to ((P \lor Q) \to (P \lor R)) & 公理4 \\
& 4. \vdash (Q \to R) \to ((\neg P \lor Q) \to (\neg P \lor R)) & (3) 代入 \dfrac{P}{\neg P} \\
& 5. \vdash (Q \to R) \to ((P \to Q) \to (P \to R)) & (4) 定义1 \\
& 6. \vdash ((P \lor P) \to P) \to ((P \to (P \lor P)) \to (P \to P)) & (5) 代入 \dfrac{Q}{P \lor P}, \dfrac{R}{P} \\
& 7. \vdash (P \lor P) \to P & 公理1 \\
& 8. \vdash (P \to (P \lor P)) \to (P \to P) & (6), (7) 分离 \\
& 9. \vdash P \to P & (2), (8) 分离 \\
& 10. \vdash (P \lor Q) \to (Q \lor P) & 公理3 \\
& 11. \vdash (\neg P \lor P) \to (P \lor \neg P) & (10) 代入 \dfrac{P}{\neg P}, \dfrac{Q}{P} \\
& 12. \vdash (P \to P) \to (P \lor \neg P) & (11) 定义1 \\
& 13. \vdash P \lor \neg P & (9), (12) 分离
\end{align*}
$$

4. 
$$
\begin{align*}
& 证明: \quad \vdash (\neg P \lor \neg Q) \to \neg (P \land Q) \\
& 1. \vdash P \lor \neg P & 第3题结论 \\
& 2. \vdash \neg (\neg P \lor \neg Q) \lor \neg (\neg (\neg P \lor \neg Q)) & (1) 代入 \dfrac{P}{\neg (\neg P \lor \neg Q)} \\
& 3. \vdash (\neg P \lor \neg Q) \to \neg (\neg (\neg P \lor \neg Q)) & (2) 定义1 \\
& 4. \vdash (\neg P \lor \neg Q) \to \neg (P \land Q) & (3) 定义3
\end{align*}
$$

5.
$$
\begin{align*}
& 证明: \quad \vdash \neg (P \land Q) \to (\neg P \lor \neg Q) \\
& 1. \vdash P \lor \neg P & 第3题结论 \\
& 2. \vdash \neg P \lor \neg \neg P & (1) 代入 \dfrac{P}{\neg P} \\
& 3. \vdash P \to \neg \neg P & (2) 定义1 \\
& 4. \vdash \neg P \to \neg \neg \neg P & (3) 代入 \dfrac{P}{\neg P} \\
& 5. (Q \to R) \to ((P \lor Q) \to (P \lor R)) & 公理4 \\
& 6. (\neg P \to \neg \neg \neg P) \to ((P \lor \neg P) \to (P \lor \neg \neg \neg P)) & (5) 代入 \dfrac{Q}{\neg P}, \dfrac{R}{\neg \neg \neg P} \\
& 7. (P \lor \neg P) \to (P \lor \neg \neg \neg P) & (4), (6) 分离 \\
& 8. P \lor \neg \neg \neg P & (1), (7) 分离 \\
& 9. (P \lor Q) \to (Q \lor P) & 公理3 \\
& 10. (P \lor \neg \neg \neg P) \to (\neg \neg \neg P \lor P) & (9) 代入 \dfrac{Q}{\neg \neg \neg P} \\
& 11. \neg \neg \neg P \lor P & (8), (10) 分离 \\
& 12. \neg \neg P \to P & (11) 定义1 \\
& 13. \neg \neg (\neg P \lor \neg Q) \to (\neg P \lor \neg Q) & (12) 代入 \dfrac{P}{\neg P \lor \neg Q} \\
& 14. \neg (P \land Q) \to (\neg P \lor \neg Q) & (13) 定义2
\end{align*}
$$

## 王浩算法

$\neg (P \land Q) \to (\neg P \lor \neg Q)$

$$
\begin{align*}
(1) && \neg (P \land Q) & \stackrel s \Rightarrow (\neg P \lor \neg Q) & (写成相断论) \\
(2) && & \stackrel s \Rightarrow (P \land Q), (\neg P \lor \neg Q) & (\neg \Rightarrow) \\
(3) && & \stackrel s \Rightarrow P, Q, (\neg P \lor \neg Q) & (\land \Rightarrow) \\
(4) && & \stackrel s \Rightarrow P, Q, \neg P 而且 \\
    && & \stackrel s \Rightarrow P, Q, \neg Q & (\lor \Rightarrow) \\
(5) && P & \stackrel s \Rightarrow P, Q 而且 \\
    && Q & \stackrel s \Rightarrow P, Q & (\neg \Rightarrow) \\
\end{align*}
$$

$由 (5) 中的两个相继式均已无联结词，而且在 \stackrel s \Rightarrow 的两端都有共同命题变项了，从而都是公理。定理得证。$