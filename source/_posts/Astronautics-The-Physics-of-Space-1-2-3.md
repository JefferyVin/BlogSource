---
title: Astronautics The Physics of Space 1.2.3
date: 2019-05-29 12:41:02
tags: Astronautics The Physics of Space
categories: Astronautics
---

# 1.2.3 Momentum vs. Pressure Thrust

Real life works nothing like the ideal world. The pressure of the chamber will not suddenly be the same as the pressure outside.

Let's go back to Momentum thrust again.
$F_{front} = (p_0 - p_\infty)A_\phi$ will be the force in the front side of the chamber, and the $F_{rear} = (p_e-p_\infty)A_\phi$

As we know from the $F_{ex} = dm_p \times v_{ex}$ also combine withe the $dm_p = \rho_e\bar{v}_eA_e$ and $v_{ex} = \eta_{div}\bar{v_e}$, you will be able to get $F_{ex} = \eta_{div}\rho_eA_e\bar{v^2_e}$

Because $F_p = (p_e - p_\infty)A_e \leq p_eA_e = F_p|_\infty$, we can get $\frac{F_p}{F_{ex}} \approx \frac{F_p}{F_e} \leq \frac{p_eA_e}{\rho_e A_e \bar{v^2_e}}$.

Thus after that everything becomes simpler, We use the ideal gas law to convert the equation to $\frac{F_p}{F_e} \leq \frac{1}{n+2}(\frac{1}{\eta_e} - 1)$

And for reasons that I do not know, we use the average degree of freedom of gas molecules, $n \approx 8$ and $\eta_e = 0.5 - 1.0$ for jet engines. (this dash means to not subtract I was confused for a second)

We plot in the numbers and get the $\frac{F_p}{F_e} \approx 0 - 10 \% $
