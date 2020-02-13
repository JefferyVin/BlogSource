---
title: Astronautics The Physics of Space 1.3.2
date: 2019-05-31 16:47:35
tags: Astronautics The Physics of Space
categories: Astronautics
---

# 1.3.2 Rocket Efficiency

## Formula

Total Rocket Efficiency:
$$\eta_{tot} = \frac{E_{kin}(v_0+\Delta v) - E_{kin}(v_0)}{E_0}$$
KE/Utilized Energy

Internal Efficiency:
$$\eta_{int} = \frac{\frac{1}{2} m_p v^2_\ast}{E_0}$$
Thurst Energy/Utilized Energy

external Efficiency:
$$\eta_{ext} = \frac{\frac{1}{2}(v_0 + \Delta v)^2 - \frac{1}{2} m_0 v^2_0}{\frac{1}{2} m_p v^2_\ast}$$
KE/Thurst Energy

$\eta_{tot} = \eta_{ext} \cdot \eta_{int}$

though a little algebra magic(I did though it), we get:
$$\eta_{ext} = \frac{(\Delta v/v_\ast)^2}{exp(\Delta v/v_*) - 1}$$

(WOW its all about the physics isn't it)


However, the external energy efficiency formula isn't really useful because only rocket equation is able ot tell whether an impulsive manueuver is efficient or not.

> The internal efficiency is a valuable figure of merit of an engine because it determines $v_\ast = \sqrt{2 E_0 \eta_{int}/m_p}$, the better $\eta_{int}$ the higher $v_\ast$ and all the more $\Delta v$ is achieved.

## Transmitted Spacecraft Power

$P_{S/C} = F_\ast \cdot v$

Note: $F_\ast$ is independent from the reference system, while v depends on the chosen external reference frame.
