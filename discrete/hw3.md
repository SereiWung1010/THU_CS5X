## 重言蕴含式的证明

证 $P \to (Q \to R) \Rightarrow (P \to Q) \to (P \to R)$

需证 $P \to (Q \to R) \to ((P \to Q) \to (P \to R)) = T$

$$
\begin{align*}
P \to (Q \to R) \to ((P \to Q) \to (P \to R))
&= P \to (Q \to R) \to (P \to (Q \to R)) & 分配律 \\
&= (P \land Q) \to R \to ((P \land Q) \to R) & 前提合取合并 \\
&= \neg (P \land Q) \lor R \to (\neg (P \land Q) \lor R) & 蕴涵等值式 \\
&= \neg ((\neg P \land Q) \lor R) \lor (\neg (P \land Q) \lor R) & 蕴涵等值式 \\
&= T & 补余律
\end{align*}
$$

需证 $P \to (Q \to R) \land \neg ((P \to Q) \to (P \to R)) = F$

$$
\begin{align*}
P \to (Q \to R) \land \neg ((P \to Q) \to (P \to R))
&= P \to (Q \to R) \land \neg (P \to (Q \to R)) & 分配律 \\
&= (P \to (Q \to R)) \land \neg (P \to (Q \to R)) & 优先顺序 \\
&= F & 补余律
\end{align*}
$$

$$
\begin{align*}
&P \to (Q \to R) = T \\
&设 P = T \\
&\quad 则 (Q \to R) = T \\
&\quad 设 Q = T \\
&\quad\quad 则 R = T \\
&\quad\quad 则 P \to Q = T, P \to R = T \\
&\quad\quad 则 (P \to Q) \to (P \to R) = T \\
&\quad 设 Q = F \\
&\quad\quad 则 (P \to Q) = F \\
&\quad\quad 则 (P \to Q) \to (P \to R) = T \\
&设 P = F \\
&\quad 则 P \to Q = T，P \to R = T \\
&\quad 则 (P \to Q) \to (P \to R) = T \\
&P \to (Q \to R) \Rightarrow (P \to Q) \to (P \to R)
\end{align*}
$$

## 推理规则的证明1

$\neg Q \lor S, (E \to \neg U) \to \neg S \Rightarrow Q \to E$

$$
\begin{align*}
& 1. \neg Q \lor S & 前提引入 \\
& 2. Q \to S & 1 置换 \\
& 3. (E \to \neg U) \to \neg S & 前提引入 \\
& 4. \neg (\neg S) \to \neg (E \to \neg U) & 3 置换 \\
& 5. S \to \neg (E \to \neg U) & 4 置换 \\
& 6. Q \to \neg (E \to \neg U) & 2、5 三段论 \\
& 7. Q \to \neg (\neg E \lor \neg U) & 6 置换 \\
& 8. Q \to (E \land U) & 7 置换 \\
& 9. Q & 附加前提引入 \\
& 10. E \land U & 8、9 分离 \\
& 11. E & 10 + 基本公式 E \land U \Rightarrow E \\
& 12. Q \to E & 条件证明规则
\end{align*}
$$

## 推理规则的证明2

如果国家不对农产品给予补贴，那么国家就要对农产品进行控制。
如果对农产品进行控制，农产品就不会短缺。
或者农产品短缺或者农产品过剩。
事实上农产品不过剩。从而国家对农产品给予了补贴。

$P = 国家对农产品给予补贴$
$Q = 国家对农产品进行控制$
$R = 农产品短缺$
$S = 农产品过剩$

$\neg P \to Q, Q \to \neg R, R \lor S, \neg S \Rightarrow P$

$$
\begin{align*}
& 1. \neg P \to Q & 前提引入 \\
& 2. Q \to \neg R & 前提引入 \\
& 3. \neg P \to \neg R & 1、2 三段论 \\
& 4. R \to P & 3 置换 \\
& 5. R \lor S & 前提引入 \\
& 6. \neg (\neg R) \lor S & 5 置换 \\
& 7. \neg R \to S & 6 置换 \\
& 8. \neg S \to R & 7 置换 \\
& 9. \neg S \to P & 4、8 三段论 \\
& 10. \neg S & 前提引入 \\
& 11. P & 9、10 分离
\end{align*}
$$