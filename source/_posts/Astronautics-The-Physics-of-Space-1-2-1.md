---
title: Astronautics The Physics of Space 1.2.1
date: 2019-05-27 21:33:24
tags: Astronautics The Physics of Space
categories: Astronautics
---

# 1.2.1 Nozzle Divergence

## Intro

As you know, in an ideal world, everything is supposed to go where-ever you want them to go. However, as we grow up, we noticed that life doesn't go the way you want it to go. Maybe the girl you like is going to a better university than you are. (sad face)

Anyway, let's get back the topic. Nozzle Divergence like that, jet spraying happens, which means that some of the fuels will be wasted no matter what.
$ddm_p = dm_p \times \mu(\theta) \times sin(\theta) \times d\theta$
$\mu(\theta)$ would be the angular mass-flow distribution function. Which basically means the small particles that have an angle when they are flowing out.

$v_e(\theta)$ is the ejection velocity with angle of $\theta$

The momentum will just be $F_e(\theta) = dm_pv_e(\theta)$
and if you only want the one that is actually pushing, it would have the $cos(\theta)$.

After all that, we would find out that $F_{ex} = dm_p\langle v_e cos(\theta) \rangle_\mu$ which is the momentum thrust.

$\eta_{div}dm_p \bar{v_e} \rightarrow \eta_{div}\bar{F_e} \rightarrow F_{ex}$

$\bar{v}_e$ is just the $\langle v_e \rangle_\mu$
and \bar{F_e}... You can tell.

$$\Large\eta_{div} = \frac{\langle v_e cos(\theta) \rangle_\mu}{\langle v_e \rangle_\mu}$$ this is the nozzle-divergence loss factor.
$1 - \eta_{div}$ would give you the loss amount of fuel.

by using the previous functions, we can deduce that $\large v_{ex} = \eta_{div}\bar{v_e}$

## After reading
