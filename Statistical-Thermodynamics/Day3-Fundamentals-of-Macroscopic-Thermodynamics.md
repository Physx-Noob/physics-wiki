---
title: Day 3: Fundamentals of Macroscopic Thermodynamics
description: 
published: true
date: 2020-08-26T06:15:28.458Z
tags: 
editor: undefined
---

# Fundamentals of Macroscopic Thermodynamics
## Quasi-static Processes and Thermal and Mechanical Energy Reservoirs
- Part of our idealization will be that during interaction with a reservoir, the reservoir evolves in a quasi-static manner. 
- By quasistatic we mean that the processes occur slowly enough that the reservoir can be treated as though it were in equilibrium at all times.
- The quasi-static idealization is very important in thermodynamic theory as it forms the basis of reversibility, a concept we will use to analyze the limiting behavior of systems.
- First consider the mechanical energy reservoir (MER)
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/25/mech-res.png)
- Very large piston and cylinder without friction. We use this reservoir to model work
done on (or by) the surroundings.
- $$dU = \delta W$$
- If the work is carried out in a quasi-static manner, then
- $$dS = \frac{1}{T} dU + \frac{p}{T} dV$$
- But work done is $\delta W = - pdV$ which makes MER **isentropic**.
- The thermal energy reservoir (TER) 
- We use this reservoir to model heat transfer with the surroundings. 
- If a system transfers heat to the TER, the 1st Law for the TER becomes
- $$dU = \delta Q$$
- For this constant-volume system, the differential form of the fundamental relation becomes
- $$dS = \frac{1}{T} dU$$
- the entropy of a TER is not constant. In fact, by the 1st Law
- $$dS = \frac{\delta Q}{T}$$
- This is Clausius’ famous relationship with which he defined entropy.
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/25/therm-res.png)

## Alternative Representations – Legendre Transformations
- Consider the case of a fundamental relation with a single independent variable, 
$$Y = Y(X)$$
- The intensive property is 
$$z = \frac{\partial Y}{\partial X}$$
- We wish to obtain a suitable function with $z$ as the independent variable that contains all the information of the original function. 
- We could replace $X$ with $z$ between these two relationships, so that 
$$Y = Y(z)$$
- However, the replacement would only be accurate to within an integration constant. 
- In other words, to invert the relationship we must integrate $z(Y)$ to recover $X$, or 
$$X = \int z(Y) + C$$ 
- where $C$ is unknown
- A method which takes this problem into account is the **Legendre transformation**.
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/25/legendre.png)
- it involves defining the transformed relationship in terms of both the local slope, $z$, and the $Y$ intercept, $\Psi$. For a given value of $X$, 
$$z = \frac{Y- \Psi}{X - 0}$$
- Hence, $\Psi = Y - zX$
- We can generalize by writing the form of the fundamental relation as
$$Y = Y(X_0, X_1, \cdots , X_t)$$
- where $Y$ is the entropy or energy and $X_i$ are the appropriate extensive properties. The intensive properties are then 
$$z_k = \frac{\partial Y}{\partial X_k} _{X_i \neq k}$$
- The transformation procedure then involves fitting planes, instead of straight lines, with 
$$\Psi = Y - \sum_k z_k X_k $$
- where the summation is over the independent properties we wish to replace. To invert $\Psi$, take the total derivative 
$$d \Psi=d Y-\sum_{k} z_{k} d X_{k}-\sum_{k} X_{k} dz_{k}=-\sum_{k} X_{k} d z_{k}$$
- $$-X_k = \frac{\partial \Psi}{\partial z_k}$$
- Note that we don’t need to replace every independent variable, only those that are convenient.
## Reversible Work
- The transformations of energy are particularly useful in the following way. 
- Suppose we ask what is the maximum amount of work that can be done by a system that is held at a constant temperature 
$$U_{SYS} + U_{TER} + U_{MER} = U_{TOT}$$
- or in other way 
$$dU_{MER} = −(dU_{SYS} + dU_{TER})$$
- from our discussion of reservoirs, we have 
$$dU_{TER} = −TdS$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/26/rev-work.png)
- $$dU_{MER} = −dF$$
- the **Helmholtz function** is a measure of the energy available to do useful work by
a constant-temperature system. 
- For this reason the Helmholtz function is also called the **Helmholtz free energy**.
- **Enthalpy** is the measure of energy available to do reversible work by a constant-pressure system 
$$dU_{MER} = −dH$$
- The **Gibbs function** is the measure of energy available to do reversible work by a constant-temperature and constant-pressure system 
$$dU_{MER} = −dG$$
- One can show that each of the thermodynamic potentials is a measure of a system to perform reversible work when the indicated intensive parameters are held constant.
## Maxwell’s Relations
- Consider the general function of two variables $f = f(x, y)$
- Chain Rule differentiation, 
$$df = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy = Mdx + Ndy$$
- Now, 
$$\frac{\partial M}{\partial y} = \frac{\partial^2 f}{\partial y \partial x} \text{ and } \frac{\partial N}{\partial x} = \frac{\partial^2 f}{\partial x \partial y}$$
- Therefore, 
$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$
- Do the same with these four equations:
  + $dU = TdS − pdV$
  + $dF = −SdT − pdV$
  + $dH = TdS + VdP$
  + $dG = −SdT + Vdp$
- We end up with famous four Maxwell Equations of Thermodynamics:
  + $$\frac{\partial T}{\partial V}_S = \frac{\partial (-p)}{\partial S}_V$$
  + $$\frac{\partial (-S)}{\partial V}_T = \frac{\partial (-p)}{\partial T}_V$$
  + $$\frac{\partial T}{\partial p}_S = \frac{\partial V}{\partial S}_p$$
  + $$\frac{\partial S}{\partial p}_T = \frac{\partial V}{\partial T}_p$$

