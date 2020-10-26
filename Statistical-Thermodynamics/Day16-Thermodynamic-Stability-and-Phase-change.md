---
title: Day 16: Thermodynamic Stability and Phase Change
description: 
published: true
date: 2020-10-26T02:02:44.928Z
tags: 
editor: markdown
---

# Thermodynamic Stability and Phase Change
- Phase change is interesting because it presents the possibility of two or more phases coexisting with the same pressure and temperature. 
- In this session we explore the role of thermodynamic stability in determining the allowable phases of a substance.
# Thermodynamic Stability
- Recall the fundamental problem of thermodynamics, as outlined in in our beginning discussions. 
- To find the equilibrium state following the removal of a constraint we found the maximum of the entropy by setting its derivative equal to zero, $dS = 0$, and solving for the independent variables that satisfied that condition. 
- However, finding a zero derivative of a function only means that there is a critical point, namely a minimum, $d^2S \geq 0$, a maximum, $d^2S \leq 0$, or a saddle point, $d^2S = 0$. 
- Here we explore the consequences of those cases where the second derivative is not less than zero.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-190733.png)
- Start by considering this figure. Assume that the two sides contain the same substance and have the same fundamental relations but are initially isolated from one another.
- Then, for the system as a whole,
$$S_{\text{initial}} = S_1(U_1, V_1,N_1) + S_2(U_2, V_2,N_2)$$
- Now suppose that we explore transferring a small amount of energy from subsystem $1$ to subsystem $2$. The final value of the entropy for the system would be
$$S_{\text{final}} = S_1(U_1 − \Delta U, V_1,N_1) + S_2(U_2 + \Delta U, V_2,N_2)$$
- The value of the second derivative will depend on the shape of $S(U)$. 
- If the initial state is located in a concave region of $S(U)$, then $d^2S > 0$ and the state is not located at a maximum of $S$. 
- This is illustrated in above figure, which shows that $S_{\text{final}} > S_{\text{initial}}$. If the barrier to heat transfer were removed, then energy would flow between the two subsystems. 
- Hence, the initial condition is unstable. This example illustrates the concept of mutual stability, that is the stability of two or more systems with respect to each other. 
- This is what we explored in our beginning discussions, where we determined that for two systems to be in equilibrium with respect to each other requires that their intensive properties $T, P,$ and $\mu$ be equal. 
- Intrinsic stability, which is our interest in this session, refers to the stability of a single system, and to phase stability in particular.
- Suppose we have a single system in an initial thermodynamic state. Imagine that in a very small volume, $dV$, the energy is perturbed a small amount, $dU$. 
- By conservation of energy, the energy of the remaining system must change by an amount $−dU$. Thus (ignoring changes in $V$ and $N$),
$$dS = S_{ss}(U_{ss} + dU) + S_s(U_s − dU)$$
- where the subscripts $ss$ refer to the subsystem and $s$ to the remainder. If $dS$ is greater than zero, then the initial state must be unstable. 
- Such can be the case if the fundamental relation has the shape illustrated in above figure.
- It is possible that a fundamental equation shows the behavior illustrated in the below figure.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-190821.png)
- Although the regions BC and EF appear to be stable, in practice the effective fundamental relation will be given by the tangent line E'. 
- The two regions BC and EF are said to be locally stable, while the region BCDEF is globally unstable. 
- Points on the tangent line E' have separated phases. While we have illustrated the stability problem by postulating small changes in energy, the same reasoning applies to perturbation in the volume or mole numbers. 
- If $f = f (x, y)$, and $f_x$ and $f_y$ are the first derivatives of $f$ with respect to $x$ and $y$, respectively, then the total second derivative of the function is
$$D(x, y) = f_{xx}f_{yy} − f^2_{xy}$$
- where $f_{xx} = \partial^2 f / \partial x \partial x$, and so on. This leads to the following possibilities:
  + If $D > 0$ and $f_{xx} < 0$, then $f (x, y)$ has a relative maximum at $(x, y)$.
  + If $D > 0$ and $f_{xx} > 0$, then $f (x, y)$ has a relative minimum at $(x, y)$.
  + If $D < 0$, then $f (x, y)$ has a saddle point at $(x, y)$,
  + If $D = 0$, the second derivative test is inconclusive.

- We have learnt that while the entropy and its transforms, the Massieu functions, are maximized, the energy and the thermodynamic potentials are minimized. For example, this requires that for the potentials, the stability criteria are
$$\frac{\partial^{2} U}{\partial S^{2}} \frac{\partial^{2} U}{\partial V^{2}}-\left(\frac{\partial^{2} U}{\partial S \partial V}\right) \geq 0$$
$$\left.\frac{\partial^{2} F}{\partial T^{2}}\right)_{V, N} \leq 0\text{ and }\left.\frac{\partial^{2} F}{\partial V^{2}}\right)_{T, N} \geq 0$$
$$\left.\frac{\partial^{2} H}{\partial T^{2}}\right)_{P, N} \geq 0\text{ and }\left.\frac{\partial^{2} H}{\partial P^{2}}\right)_{S, N} \leq 0$$
$$\left.\frac{\partial^{2} G}{\partial T^{2}}\right)_{P, N} \leq 0\text{ and }\left.\frac{\partial^{2} G}{\partial P^{2}}\right)_{T, N} \leq 0$$
- Using Maxwell’s relations, one can show that local stability also requires
$$\kappa_{T} \geq \kappa_{S} \geq 0$$
$$C_{p} \geq C_{v} \geq 0$$
$$
\left.\frac{\partial P}{\partial v}\right)_{T}=-\frac{1}{\kappa_{T}} \leq 0
$$
- where $\kappa_T$ and $\kappa_S$ are the isothermal and isentropic compressibility, respectively.
# Phase Change
- Now consider the stability of a substance described by van der Waals equation:
$$
P=\frac{R T}{v-b}-\frac{a}{v^{2}}
$$
- Local stability requires that
$$
\left.\frac{\partial P}{\partial v}\right)_{T} \leq 0
$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Annotation-2020-10-25-190851.png)
- If we plotted $p–v$ isotherms of van derWaals equation in the liquid vapor region it would look something like the above figure. 
- This is typical of many simple compressible substances.
- A single isotherm is shown in the below figure. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Capture.png)
- The local stability criterion is clearly violated over the region F–K–M and therefore a phase transition must be involved. 
- We can explore this more exactly by calculating the Gibbs potential, noting that the chemical potential is the Gibbs function per mole in the Gibbs representation and stable points have minimum $\mu$:
$$d\mu = -sdT + vdP$$
- Along the line of constant $T$:
$$\mu = \int vdP + \phi(T)$$
- where $\phi(T)$ is an integration constant (that will be a function of $T$). Thus, the change in chemical potential between two points on an isotherm is
$$\mu_B - \mu_A = \int_A^B v(p)dp$$
- If we were to carry out the integration over a range of pressures, the results would look like this figure here.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Annotation-2020-10-25-191054.png)
- As the pressure is increased, the physical state is the one with minimum $\mu$. At the points D, O where the two sides overlap, both liquid and vapor branches are at minimum $\mu$. 
- Recall the $pvT$ phase diagram for a simple compressible substance. One diagram is presented here for convenience.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Annotation-2020-10-25-191122.png)
- The phase change lines are locations where two branches of the Gibbs potential meet and $\mu$ is at a minimum. 
- As a result, the $pv$ behavior of an isotherm must look something like shown below, where the isotherm falls on the line DKO and not DFKMO. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Annotation-2020-10-25-191212.png)
- The areas I and II must be equal, because
$$\mu_D - \mu_O = \int_O^D v(p)dp = 0$$
- Finally, the vapor dome is constructed by applying the above equation over the full range of volumes.
- The saturation properties can be calculated using
$$\left.s_{f g}=s_{D}-s_{O}=\int_{O M K F D} \frac{\partial p}{\partial T}\right)_{v} d v$$
$$u_{f g}=u_{D}-u_{O}=T s_{f g}-p\left(v_{D}-v_{O}\right)$$
$$h_{f g}=\left(u_{D}+p_{D} v_{D}\right)-\left(u_{O}+p_{O} v_{O}\right)=u_{f g}+p\left(v_{D}-v_{O}\right)$$
- One can easily derive the Clapeyron equation by writing $s$ as a function of $v$ and $T$ and taking the derivative
$$
d s=\left(\frac{\partial s}{\partial v}\right) d v+\left(\frac{\partial s}{\partial T}\right) d T
$$
- During a phase change the temperature is constant, so
$$
d s=\left(\frac{\partial s}{\partial v}\right) d v
$$
- Using Maxwell’s relation
$$
d s=\left(\frac{\partial p}{\partial T}\right)_{v} d v
$$
- Since the pressure and temperature are constant, the derivative cannot change, and can be replaced with the total derivative:
$$ds = \frac{dp}{dT} dv$$
- Integrating from one phase to the other,
$$\frac{dp}{dt} = \frac{\Delta s}{\Delta v}$$
- Now $du = Tds − pdv$. Introducing the enthalpy, $dh = du + pdv = Tds$
- Given constant pressure and temperature,
$$\Delta s = \frac{\Delta h}{T} = \frac{L}{T}$$
- where $L$ is the latent heat phase change. Therefore,
$$\frac{dp}{dT} = \frac{L}{T\Delta v}$$
# Gibbs Phase Rule
- The stability requirement that the Gibbs free energy be minimized also applies in the case of multi-component mixtures. 
- The complexity grows with the number of components. 
- However, there is a simple rule, called the Gibbs phase rule. If $r$ is the number of components, and $M$ the number of phases, then $$f = r − M + 2$$ where $f$ is the number of independent intensive parameters allowed. 
- $f$ is also called the thermodynamic degrees of freedom. 
- The number of phases that can coexist is $M = f + r + 2$. 
- The maximum number of phases that can coexist is found by setting $f = 0$. 
- For a single-component system, a maximum of three phases can coexist. 
- We call that point the triple point, as shown in previously. 
- The possibilities for a two-component system are illustrated in the table below.

|$f$|$M$ |
|--|--|
| 0 | 4 |
| 1 | 3 |
| 2 | 2 |
| 3 | 1 |
# Thermodynamic versus Dynamic Stability
- Just because the thermodynamics suggest that a phase change should occur, in practice it might not. 
- This is because action at the microscopic level is required for the phase change to occur. 
- A classic example is the heat treating of steel, where quenching “locks in” a harder phase state than would exist at room temperature were the metal to be at equilibrium.
- Another example is the supersaturation of dissolved sugar in water. To understand this phenomenon, consider the two snowboarding half-pipes (potential energy curves) illustrated here. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/26/Annotation-2020-10-26-072554.png)
- Imagine that a snowboarder is poised to drop into the pipe (well), as shown on the left side. For the snowboarder it is all downhill, no work is required to “fall” into the well. 
- The snowboarder on the right, however, finds herself in a small hole on the lip of the potential. To get into the halfpipe (well) will require work to get over the hump. 
- In thermodynamic systems that little bit of work must come from fluctuating motions at the microscopic level. 
- If they are large enough, then the system can be pushed over into a globally stable configuration.
- The snowboarder on the right is in a local energy minimum, and therefore a “local” stable point, while the bottom or the large well is a “global” stability point.