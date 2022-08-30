# Permutation Tensor, $\epsilon_{ijk}$

$$\begin{equation}
\begin{split}
\epsilon_{ijk} &= \begin{cases}
1 &, \text{ for even permutation of } i, j, k \\
-1 &, \text{ for odd permutation of } i, j, k \\
0 &, \text{ two or more equal indices }
\end{cases}
\end{split}
\end{equation}$$

Essentially, if the indices increase, cyclically (left-right) then is $1$, else if decrease left-right is $-1$, otherwise is $0$.

!!! example Calculating a Moment
    $M = x \times F \equiv \epsilon_{ijk}x_{j}F_{k}$