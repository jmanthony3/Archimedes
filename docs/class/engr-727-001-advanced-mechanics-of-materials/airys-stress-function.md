# airys-stress-function

Stress Function Technique
: Many engineering, plane-elastic problems can be solved by some method that employs the **#Airys-Stress-Function** to reduce the general formulation to a single governing equation in terms of a single unknown.

In this approach, the underlying question is: "What if this was dependent on the second derivative of some function?" These equations still satisfy the equations of equilibrium and are substituted into the compatibility equations.

#eq-biharmonic
$$\begin{equation}
\frac{\partial^{4}\Phi}{\partial x^{4}} + \frac{\partial^{4}\Phi}{\partial x^{2}\partial y^{2}} + \frac{\partial^{4}\Phi}{\partial y^{4}} = \nabla^{4}\Phi = 0
\end{equation}$$