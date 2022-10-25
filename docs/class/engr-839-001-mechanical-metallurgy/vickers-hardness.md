# Vickers Hardness

Also known as *#Diamond-Pyramid*, because indenter is pyramid with $136\degree$, which is based on $d_{Brinell} = 0.375D$ relationship.
Can be used on any material.
Indentation size measured by average length across diagonals.
Hardness computed by...
$$\begin{equation}
HV = \frac{2Psin(\frac{\alpha}{2})}{d^{2}} \approx = \frac{1.8544P}{d^{2}}
\end{equation}$$
If known, the Vicker's Hardness may be correlated to #tensile-strength by:
$$\begin{equation}
\sigma_{TS}(MPa) = 3.2 HV
\end{equation}$$
For Vickers hardness, measured value is related to #yield-stress through Tabor's relation:
$$\begin{equation}
H = 3\sigma_{y}
\end{equation}$$

This assumes no [work-hardening](deformation-and-work-hardening.md); therefore, use $\epsilon_{p} = \frac{d'}{5D} \approx 0.075$ for $d = 0.375D$ with a #flow-stress, $\tau = 8-10 \%$ in hardness conversions.