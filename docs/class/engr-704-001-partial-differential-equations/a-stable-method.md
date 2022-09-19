# A-stable Method

The [region of absolute stability](region-of-absolute-stability.md) contains entire, left half-plane of $\gamma h$ for $\gamma < 0$ on the complex plane, $\mathbb{Z}$.
Likely named for the absolute value property.

!!! example Example
    [Forward Euler](euler-method.md#forward) is conditionally stable: $$|1 + \gamma h| < 1,~h<\frac{2}{|\gamma|},~\text{for}~\gamma < 0,~h < \frac{-2}{\gamma}$$
    The region of stability...

    | ![](../../../attachments/engr-704-001-partial-differential-equations/a_stable_method_example_of_forward_euler_211001_175330_EST.png) |
    |:--:|
    | The [region of stability](region-of-absolute-stability.md), $\gamma h = z,~abs(1 + z) < 1$. **This is not A-Stable method**, because the [stability region](region-of-absolute-stability.md) is not entire, left half-plane. #stability is limited by step size, $h$. |