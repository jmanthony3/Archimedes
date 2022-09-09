# energy-methods

### [Strain Energy](strain-energy.md) and #Castiglianos-Theorem

[Strain Energy](strain-energy.md)
: Energy absorbed by the material during the loading process.
If we assume that the material follows *[Hooke's Law](hookes-law.md)*, then the load-displacement curve is a straight line.
Then the strain energy, *U* stored in the bar (equal to the work, $W$ done by the load) is: $U_{0} = W = \frac{P\delta}{2} = \frac{P^{2}L}{AE}$.

!!! example Problem Set: 7-1
    **Problem 1**: A cantilever shaft is made of a carbon steel bar and is loaded by a force, $P$.
    (a) Find the vertical displacement of point $C$.

    At $BC$

    $$\begin{align*}
    M_{BC} &= P_{x} &\implies \frac{\partial M_{BC}}{\partial P} &= x \\
    V &= P &\implies \frac{\partial V}{\partial P} &= 1
    \end{align*}$$

    At $AB$

    $$\begin{align*}
    M_{AB} &= Px &\implies \frac{\partial M_{AB}}{\partial P} &= x \\
    V &= P &\implies \frac{\partial V}{\partial P} &= 1 \\
    T &= PL &\implies \frac{\partial T}{\partial P} &= L
    \end{align*}$$

    The vertical deflection at $C$:= $\delta_{i} = \sum_{i} \frac{\partial U}{\partial P_{i}}$.
    Therefore,

    $$\begin{split}
    \delta_{i} &= \sum_{i} \frac{\partial U}{\partial P_{i}} \\
    &\equiv \frac{1}{EI}\Biggl[ \int_{0}^{L} Px(x)dx + \int_{0}^{L}Px(x)dx \Biggr] + \frac{1}{GJ}\int_{0}^{L}PL(L)dx \\
    &= \frac{2}{3}\frac{PL^{3}}{EI} + \frac{PL^{3}}{GJ}
    \end{split}$$

    ---

    **Problem 2**

    Equilibrium

    $$\begin{split}
    \sum M_{D} = 0 &:= C_{x} = \frac{3}{2}P \\
    \sum F_{x} = 0 &:= D_{x} = -C_{x} \\
    \sum F_{y} = 0 &:= D_{y} = P
    \end{split}$$

    By employing the **Method of Joints**:

    1. Joint $A$
    $$\begin{split} \sum F_{y} &= F_{AB}(\frac{4}{5}) - P \\
    \sum F_{x} &= F_{AB}(\frac{4}{5}) - F_{AD}
    \end{split}$$
    1. Joint $D$
    $$\begin{split}
    \sum F_{y} &= D_{y} - F_{BD}(\frac{4}{5}) \\
    F_{BD} &= \frac{5}{4}P
    \end{split}$$

    A table is used to apply the method.


    | **Member** | $F$ | $L$ [$m$] | $A$ [$mm^{2}$] | $\frac{\partial F}{\partial F_{i}}$ | $F\frac{\partial F}{\partial F_{i}}L$ |
    | --- | --- | --- | --- | --- | --- |
    | $AB$ | $\frac{5}{4}P$ | $2.5$ | $600$ | $\frac{5}{4}$ | $3.90625 \times P$ |
    | $AD$ | $-\frac{3}{4}P$ | $3$ | $600$ | $-\frac{3}{4}$ | $1.6875 \times P$ |
    | $BC$ | $\frac{3}{2}P$ | $1.5$ | $600$ | $\frac{3}{2}$ | $3.375 \times P$ |
    | $BD$ | $-\frac{5}{4}P$ | $2.5$ | $600$ | $-\frac{5}{4}$ | $3.90625 \times P$ |

    Summing the last column: $12.875 \times P \implies P = 64,375 N-m$.
    The deflection at point $A$ using the #Castiglianos-Theorem Theorem: $\delta_{A} = \frac{1}{AE}\sum_{i}\Bigl( \frac{\partial F}{\partial F_{i}} \Bigr)L = 0.518~mm$.