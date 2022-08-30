# Kronecker's Delta, $\delta_{ij}$

$$\begin{equation}
\begin{split}
\delta_{ij} &= \begin{cases}
1 &, i = j \\
0 &, i \neq j
\end{cases} \\
&= \underset{\sim}{e_{1}} \cdot \underset{\sim}{e_{2}} = \frac{\partial x_{i}}{\partial x_{j}}
\end{split}
\end{equation}$$

Eventually, this becomes the identity matrix which is always a second rank tensor. The last statement in the above equation, is the inner product of the two vectors: $|\vec{a}||\vec{b}|\cos(\theta)$. This delta is sometimes called the **#Substitution-Operator**. This absorbs the repeating index and replaces with the remaining free index: $\delta_{ij}\underset{\sim}{e_{j}} \rightarrow \underset{\sim}{e_{i}}$.