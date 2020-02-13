---
title: Astronautics The Physics of Space 1.3.1
date: 2019-05-30 19:49:33
tags: Astronautics The Physics of Space
categories: Astronautics
---

# 1.3.1 Payload Considerations

So of course to any one who has a logic sense, you can already tell that the amount of payload that a rocket can carry depends on the amount of the thurst that the rocket have.

So the author defined these(not really):
$$m_f = m_s + m_L$$
Mass ratio:
$$\mu := \frac{m_f}{m_0} = \frac{m_s+m_L}{m_0}$$
Structural ratio:
$$\varepsilon := \frac{m_s}{m_0 - m_L} = \frac{m_s}{m_s + m_p}$$
payload ratio:
$$\lambda := \frac{m_L}{m_0 - m_L} = \frac{m_L}{m_s + m_p}$$

$m_f$ is the final mass without the propellent.
$m_0$ is the initial mass with the propellent.
$m_s$ is the mass of the structure of the rocket.
$m_L$ is the mass of the payload.

thus for $\mu (1 + \lambda)$ we get $\varepsilon + \lambda$... very ez to get. and then $\mu = \frac{\varepsilon + \lambda}{1 + \lambda}$

and I took a sneak peak at the later chapter 2.2.2.
we have the formula $\Delta v = v_\ast ln\frac{m_0}{m} @ v_\ast = constant$ which is the rocket equation(for single stage)...

We plot it in, we know that $\frac{\Delta v}{v_ast} = -ln\frac{\varepsilon + \lambda}{1 + \lambda}$

thus we have the paload ratio equation$$\lambda = \frac{e^{-\Delta v/v_\ast} - \varepsilon}{1 - e^{-\Delta v/v_\ast}}$$

And I need to find a way to insert mathematical graph into this........
OK.

#### Notes after reading this chapter
Relative easy chapter, my "theory" about why does the rocket need to have different stages got confirmed. Very Easy to read compare to the last several chapters.
