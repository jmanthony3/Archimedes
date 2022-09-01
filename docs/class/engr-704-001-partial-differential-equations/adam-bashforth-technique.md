# Adam-Bashforth Technique

A $4^{th}$-order **explicit** method.
$$\begin{equation}
\begin{split}
u_{k+1} &= u_{k} \\
&+ \frac{h}{24}[55f'(t_{k}, u_{k}) - 59f'(t_{k- 1}, u_{k - 1}) + 37f'(t_{k - 2}, u_{k - 2}) - 9f'(t_{k - 3}, u_{k - 3})]
\end{split}
\end{equation}$$