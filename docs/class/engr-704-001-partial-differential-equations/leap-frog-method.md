# Leap Frog Method

Thus far, we have studied **first-order** methods accurate for the linear wave equation.
*Leap Frog Method* is the simplest, **second-order** accurate method.
An explicit, one-step, three-time-level scheme for the first-order wave equation:
$$\begin{equation}
\frac{u_{j}^{n + 1} - u_{j}^{n - 1}}{2\Delta t} + c\frac{u_{j + 1}^{n} - u_{j - 1}^{n}}{2\Delta x} = 0 \text{, T.E.: } \mathscr{O}((\Delta t)^{2}, (\Delta x)^{2})
\end{equation}$$

$u$ must be known at time step, $n$ and $n - 1$ to find $u$ at time step, $n + 1$ (explicit).
==Stability condition $|v| \leq 1$.==
The #Modified-Leap-Frog-Method:

\eqlabe

The leading term in the #truncation-error term has the odd derivative, hence it would have predominantly #dispersive-error, which is typical for second-order methods.
No even in #truncation-error, hence no #dissipative-error.

| ![](../../../attachments/engr-704-001-partial-differential-equations/leap_frog_amplification_factor_and_relative_phase_angle_211119_185245_EST.png) |
|:--:|
| The #amplification-factor, $G = \frac{}{}$ is always $1$ because of no #dissipative-error. Therefore, the #relative-phase-angle, $\frac{\phi}{\phi_{e}} = \frac{\tan^{-1}\bigg(\frac{-\nu\sin(\beta)}{\pm\sqrt{1 - \nu^{2}\sin^{2}(\beta)}}\bigg)}{asdf}$. |