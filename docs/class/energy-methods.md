# energy-methods

### Strain Energy and Catigliano Theorem

Strain Energy  
Energy absorbed by the material during the loading process. If we assume that the material follows *Hooke’s Law*, then the load-displacement curve is a straight line. Then the strain energy, *U* stored in the bar (equal to the work, *W* done by the load) is: $U_{0} = W = \frac{P\delta}{2} = \frac{P^{2}L}{AE}$.

**Problem 1**

A cantilever shaft is made of a carvon steel bar and is loaded by a force, *P*. (a) Find the vertical displacement of point *C*.

At *B**C*

$$\begin{split}
M_{BC} &= Px &\implies \frac{\partial M_{BC}}{\partial P} &= x \\\
V &= P &\implies \frac{\partial V}{\partial P} &= 1
\end{split}$$

At *A**B*

$$\begin{split}
M_{AB} &= Px &\implies \frac{\partial M_{AB}}{\partial P} &= x \\\
V &= P &\implies \frac{\partial V}{\partial P} &= 1 \\\
T &= PL &\implies \frac{\partial T}{\partial P} &= L
\end{split}$$

The vertical deflection at *C*:= $\delta_{i} = \sum_{i} \frac{\partial U}{\partial P_{i}}$. Therefore,

$$\begin{split}
\delta_{i} &= \sum_{i} \frac{\partial U}{\partial P_{i}} \\\
 &\equiv \frac{1}{EI}\Biggl\[ \int_{0}^{L} Px(x)dx + \int_{0}^{L}Px(x)dx \Biggr\] + \frac{1}{GJ}\int_{0}^{L}PL(L)dx \\\
 &= \frac{2}{3}\frac{PL^{3}}{EI} + \frac{PL^{3}}{GJ}
\end{split}$$

**Problem 2**

Equilibrium

$$\begin{split}
\sum M_{D} = 0 &:= C_{x} = \frac{3}{2}P \\\
\sum F_{x} = 0 &:= D_{x} = -C_{x} \\\
\sum F_{y} = 0 &:= D_{y} = P
\end{split}$$

By employing the **Method of Joints**:

1.  Joint A

\begin{split} \sum F_{y} &= F_{AB}(\frac{4}{5}) - P \\\ \sum F_{x} &= F_{AB}(\frac{4}{5}) - F_{AD} \end{split}

$$\begin{split}
\sum F_{y} &= D_{y} - F_{BD}(\frac{4}{5}) \\\
F_{BD} &= \frac{5}{4}P
\end{split}$$

<table style="width:100%;"><caption>A table is used to apply the method.</caption><colgroup><col style="width: 16%" /><col style="width: 16%" /><col style="width: 16%" /><col style="width: 16%" /><col style="width: 16%" /><col style="width: 16%" /></colgroup><thead><tr class="header"><th style="text-align: left;">Member</th><th style="text-align: left;"><span class="math inline"><em>F</em></span></th><th style="text-align: left;"><span class="math inline"><em>L</em> [<em>m</em>]</span></th><th style="text-align: left;"><span class="math inline"><em>A</em> [<em>m</em><em>m</em><sup>2</sup>]</span></th><th style="text-align: left;"><span class="math inline">$\frac{\partial F}{\partial F_{i}}$</span></th><th style="text-align: left;"><span class="math inline">$F\frac{\partial F}{\partial F_{i}}L$</span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><p><span class="math inline"><em>A</em><em>B</em></span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{5}{4}P$</span></p></td><td style="text-align: left;"><p><span class="math inline">2.5</span></p></td><td style="text-align: left;"><p><span class="math inline">600</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{5}{4}$</span></p></td><td style="text-align: left;"><p><span class="math inline">3.90625 × <em>P</em></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="math inline"><em>A</em><em>D</em></span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{3}{4}P$</span></p></td><td style="text-align: left;"><p><span class="math inline">3</span></p></td><td style="text-align: left;"><p><span class="math inline">600</span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{3}{4}$</span></p></td><td style="text-align: left;"><p><span class="math inline">1.6875 × <em>P</em></span></p></td></tr><tr class="odd"><td style="text-align: left;"><p><span class="math inline"><em>B</em><em>C</em></span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{3}{2}P$</span></p></td><td style="text-align: left;"><p><span class="math inline">1.5</span></p></td><td style="text-align: left;"><p><span class="math inline">600</span></p></td><td style="text-align: left;"><p><span class="math inline">$\frac{3}{2}$</span></p></td><td style="text-align: left;"><p><span class="math inline">3.375 × <em>P</em></span></p></td></tr><tr class="even"><td style="text-align: left;"><p><span class="math inline"><em>B</em><em>D</em></span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{5}{4}P$</span></p></td><td style="text-align: left;"><p><span class="math inline">2.5</span></p></td><td style="text-align: left;"><p><span class="math inline">600</span></p></td><td style="text-align: left;"><p><span class="math inline">$-\frac{5}{4}$</span></p></td><td style="text-align: left;"><p><span class="math inline">3.90625 × <em>P</em></span></p></td></tr><tr class="odd"><td style="text-align: left;" colspan="5"></td><td style="text-align: left;"><p><span class="math inline">12.875 × <em>P</em> ⟹ <em>P</em> = 64, 375 <em>N</em> − <em>m</em></span></p></td></tr></tbody></table>

A table is used to apply the method.

The deflection at point *A* using the Castigliano Theorem: $\delta_{A} = \frac{1}{AE}\sum_{i}\Bigl( \frac{\partial F}{\partial F_{i}} \Bigr)L = 0.518~mm$.