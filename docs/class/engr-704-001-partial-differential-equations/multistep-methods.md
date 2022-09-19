# Multistep Methods

We may use more accurate, previous information to approximate next grid's solution.

Multistep Methods
: Methods using more than one grid point to approximate next grid point.

[Adam-Bashforth Technique](adam-bashforth-technique.md)
: A $4^{th}$-order **explicit** method.
$$\begin{equation}
\begin{split}
u_{k+1} &= u_{k} \\
&+ \frac{h}{24}[55f'(t_{k}, u_{k}) - 59f'(t_{k- 1}, u_{k - 1}) + 37f'(t_{k - 2}, u_{k - 2}) - 9f'(t_{k - 3}, u_{k - 3})]
\end{split}
\end{equation}$$

[Adam-Moulton Technique](adam-moulton-technique.md)
: A $4^{th}$-order **implicit** method.

In general, an implicit method has better [stability](stability.md) and accuracy than explicit methods.
Why? Because implicit methods use more information of the data.
When linear, the equation can be algebraically solved...

!!! example Solve #IVP $\dot{u} = e^{u}$.