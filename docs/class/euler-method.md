# Euler Method

Solving #Euler-Method in forward (using previous iteration to solve next iteration) gives lower accuracy in quicker time than solving backward (using future information to solve the future iteration), which gives great accuracy in much time.

$$\begin{equation}
\begin{split}
\frac{du}{dt} &= f'(t, u), u(t_{0}) = u_{0}, h = t_{k+1} - t_{k} \\\\
u_{k+1} &= u_{k} + hf'(t_{k}, u_{k})
\end{split}
\label{eq:forward_euler}
\end{equation}$$

| ![](../../attachments/engr-704-001-partial-differential-equations/euler_method_graph_example_210924_171911_EST.png) |
|:--:|
| The accuracy for curved functions can be improved with smaller $h$. |

!!! example
	| ![](../../attachments/engr-704-001-partial-differential-equations/euler_method_example_error_210924_172623_EST.png) |
	|:--:|
	| First order error proportional to step size. |