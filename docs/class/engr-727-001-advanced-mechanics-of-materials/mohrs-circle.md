# Mohrs-Circle

1. Assumes a #homogeneous material.
2. Maximum #principal-stress, $\sigma_{1}$ where $\tau = 0$: no shearing!
3. Can move from any #stress-state, but there is still a **maximum principal plane with no shearing**.

- A graphical way to represent stress #transformation to alternative orientations.
- These are set of equations that describe stress #transformation, but a graphical solution is often useful.

![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_illustration_210907_153956_EST.png)

- #principal-stress: maximum/minimum #normal-stresses (no shear)

![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_transformation_equation_illustration_210907_154859_EST.png)

- $R = \sqrt{(\frac{\sigma_{11} - \sigma_{22}}{2})^{2} + \tau_{12}^{2}}$
- $\sigma_{11}' = \frac{\sigma_{11} + \sigma_{22}}{2} + \frac{\sigma_{11} - \sigma_{22}}{2}cos(2\theta) + \sigma_{12}sin(2\theta)$
- $\sigma_{12}' = -\frac{\sigma_{11} - \sigma_{22}}{2}sin(2\theta) + \sigma_{12}cos(2\theta)$

!!! example What is the #stress-state if rotated $30\degree$ CCW?
    ![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_problem_1_210907_155042_EST.png)

    *Given: $\sigma_{11} = -8 ksi, \sigma_{22} = 12 ksi, \sigma_{12} = -6 ksi$*
    Center point, $C = \sigma_{avg} = \frac{\sigma_{11} + \sigma_{22}}{2} = \frac{-8 + 12}{2} = 2 ksi$

    ![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_problem_step_t_find_r_210907_155511_EST.png)

    $R = \sqrt{10^{2} + 6^{2}} = 11.66$

    ![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_cricle_example_1_problem_step_to_find_angle_210907_155632_EST.png)

    Use trig to find $\phi$ and $\psi$: $\phi = tan^{-1}(\frac{6}{10}) = 30.96\degree, \psi = 60 - \phi = 29.04\degree$
    $\sigma_{11}' = 2 - 11.66cos(29.04) = -8.2 ksi$
    $\sigma_{12}' = -11.66sin(29.04) = 5.66 ksi$

    | ![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_210907_160049_EST.png) |
    |:--:|
    | Slight drop increase of #normal-stress and slight decrease of #shear-stress. |
    | ![](../../../attachments/engr-839-001-mechanical-metallurgy/mohrs_circle_example_1_complete_clean_210908_192355_EST.png) |
    | Basic steps to find all stresses and strains at orientations relative to what you start with. |