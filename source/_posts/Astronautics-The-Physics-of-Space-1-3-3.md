---
title: Astronautics The Physics of Space 1.3.3
date: 2019-06-02 10:40:46
tags: Astronautics The Physics of Space
categories: Astronautics
---

# 1.3.3 Performance Parameters

## formulas

Total Impulse:
$$I_{tot} = \int_{0}^{t} F_\ast dt = m_p v_\ast @v_* = const$$

(weight-) specific impulse:
The achieveable total impulse of an engine with respect to a iven exhausted propellant weight $m_p g_0$
$$I_sp := \frac{I_{tot}}{m_p g_0} = \frac{v_0}{g_0}$$

In ESA, $I_{sp} = v_\ast$ is the mass-specific impulse.

> The specific impulse is an importatnt figure of merit of an engine, and is in essence the effective exhaust velocity

Jet Power:

> The change of KE of the ejected gas(jet energy) per time Unit

$$P_jet := \langle \frac{dE_{jet}}{dt} \rangle_\mu = \langle \frac{d}{dt} \rangle_\mu = \frac{1}{2} dmp/dt \langle v_e^2 \rangle_\mu = \frac{1}{2}
\frac{\bar{F_e} \bar{v_e}}{\eta_{VDF}} > \frac{1}{2} \bar{F_e}\bar{v_e}$$

VDF is the velocity distribution function $v_e(\theta)$

VDF loss factor:
$$\eta_{VDF} := \frac{\langle v_e \rangle^2_\mu}{\langle v_e^2 \rangle_\mu} \leq 1$$

Uniform ejection velocity $\bar{v_e} = v_e$ and $\eta_{VDF} = 1$
thus, $P_jet = \frac{1}{2} F_e v_e @ v_e(\theta) = const = v_e$

From the jet power equation and the total engine efficiency equation of a real rocket, we will be able to get $\eta_{tot} = \frac{1 \times \bar{F_e} \bar{v_e}}{2 \times \eta_{VDF} P_{in}}$

because for real jet power:
$P_{jet} = 1/2 dm_p/dt \langle v_e^2 \rangle_mu$
and ideal s same with jet,id as subscript

thus the $$\eta_{tot} = \frac{dm_p/dt \langle v_e^2 \rangle_mu P_{jet,id}}{dm_{p,id} \langle v_{e,id}^2 \rangle_mu P_{in}}$$

Therefore, $\zeta_d = \frac{dm_p/dt a_0 \sqrt{n}}{A_t C_\infty p_0} = 0.98 - 1.15$
which is the discharge correction factor,

and for velocity correciton factor, $\zeta_v := \sqrt{\frac{\langle v_e^2 \rangle_mu}{\langle v_{e,id}^2 \rangle_mu}} = 0.85 - 0.98$

After all the calulation, we get that $\eta_{tot} = \zeta_d \zeta_v^2 \eta_{ec}$

$$\eta_T = \frac{F_\ast}{F_{e,id}} = \eta_{div} \zeta_d \zeta_v$$

Thrust to power ratio
$$r_{TTPR} := \frac{F_\ast}{P_{in}} = \frac{F_{ex}}{P_{in}} @ p_e = p_\infty = \frac{2}{\bar{v_e}} \eta_{div} \eta_{VDF} \zeta_d \zeta_v^2 \eta_{ec} @p_e = p_\infty$$
thus $\eta_{div} = 0.989 - 0.996$
