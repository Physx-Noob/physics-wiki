---
title: Day 10: Ideal Gases
description: 
published: true
date: 2020-09-04T08:15:26.742Z
tags: 
editor: markdown
---

# Ideal Gases
- We deal with non-interacting, or ideal gases. 
- We calculate the partition function for such gases in a fairly straightforward way. 
- The partition function can be separated into several components, representing each of the various modes of motion available to the atom or molecule. In some cases, simple algebraic relations are obtained. 
- For the monatomic gas, only translational and electronic motion must be considered. 
- For molecules, vibrational and rotational motion must be added. 
- This task is simplified if the Maxwell–Botzmann limit holds, and we will make that assumption for monatomic and molecular gases.

## Partition Function
- The single-component grand canonical partition function in a gas satisfying the Maxwell–Boltzmann limit is:
$$\ln Q_{M B}=\sum_{k} e^{-\beta \epsilon_{k}-\gamma}$$
- $\gamma$ is not a function of the summation index $k$, so, we can remove it from summation.
$$\ln Q_{M B}=e^{-\gamma} \sum_{k} e^{-\beta \epsilon_{k}}$$
- The summation represents “**molecular partition function**.” We can separate the molecular partition function by noting that the energy can be written as the sum of the translational and internal energy $\epsilon = \epsilon_{\text{tr}} + \epsilon_{\text{int}}$
- Since, both of them are statistically independent, we can write
$$\ln Q_{M B}=e^{-\gamma} \sum_{k} e^{-\beta \epsilon_{t r, k}} \sum_{k} e^{-\beta \epsilon_{i n t, k}}$$
- which implies $\ln Q_{\text{MB}} = e^{-\gamma} q_{\text{int}} q_{\text{tr}}$, where the $q$’s are the molecular partition functions. It remains to evaluate them.

## The Translational Partition Function
- To evaluate the translational partition function requires the quantum-mechanical expression for the translational energy, which is:
$$\epsilon_{t r}=\frac{h^{2}}{8 m}\left\{\left(\frac{n_{x}}{l_{x}}\right)^{2}+\left(\frac{n_{y}}{l_{y}}\right)^{2}+\left(\frac{n_{z}}{l_{z}}\right)^{2}\right\}$$
- Here, the $n$’s are the translational quantum numbers and the $l$’s the macroscopic dimensions in the three coordinate directions. Therefore, if the motions in the three coordinate directions are statistically independent, then
$$q_{t r}=q_{x} q_{y} q_{z}=\sum_{n_{x}} e^{-\frac{\beta h^{2}}{8 m} \frac{n_x^{2}}{l_{x}^{2}}} \sum_{n_{y}} e^{-\frac{\beta h^{2}}{8 m} \frac{n_y^{2}}{l_y^{2}}} \sum_{n_{z}} e^{-\frac{\beta h^{2}}{8 m} \frac{n_z^{2}}{l_{z}^{2}}}$$
- We can obtain an analytic expression for $q_{t r}$ if we note that, in practice, we are dealing with very large quantum numbers. Thus, we can treat the exponentials as continuous rather than discrete functions. For example
$$q_{x}=\sum_{n_{x}} e^{-\frac{\beta h^{2}}{8 m} \frac{n_x^{2}}{l_{x}^{2}}} \cong \int_{0}^{\infty} e^{-\frac{\beta h^{2}}{8 m} \frac{n_x^{2}}{l_x^{2}}} d n_{x}$$
- making a new definition $x =\left ( \frac{\beta h^{2}}{8 m} \right )\frac{n_x}{l_x}$, we have $q_{x} \cong\left(\frac{8 m}{\beta h^{2}}\right)^{1 / 2} l_{x} \int_{0}^{\infty} e^{-x^{2}} d x$
$$q_{t r}=\left(\frac{2 \pi m k T}{h^{2}}\right)^{1 / 2} V$$
- where $V = l_x l_y l_z$
- Let us now explore the distribution of particles over the allowed translational energy states. Recall that the number of particles in a given state is $N_k = e^{-\gamma} e^{-\beta \epsilon_k}$, we have
$$N = e^{-\gamma} \sum_{k}e^{-\beta \epsilon_k}$$
- the probability of finding a particle in a given state is
$$\frac{N_{k}}{N}=\frac{e^{-\beta \epsilon_{k}}}{\sum_{k} e^{-\beta \epsilon_{k}}}$$
- This is called the **Boltzmann ratio** and is generally applicable for any mode of motion. For translational energy the differences between energy levels are so small that energy varies continuously, and we can write
$$f(\epsilon) d \epsilon=\frac{e^{-\beta \epsilon_{k}}}{\sum_{k} e^{-\beta \epsilon_{k}}} d g$$
- where $f$ is a probability distribution function, $f (\epsilon)d \epsilon$  is the fraction of particles in the interval $\epsilon$ to $\epsilon + d\epsilon$, and $dg$ is the degeneracy for the energy increment. The denominator is, of course, the translational energy partition function that we have already derived. To relate $d\epsilon$ to $dg$ first consider that
$$\epsilon=\frac{h^{2}}{8 m V^{2 / 3}} n^{2}$$
- where $n$ is the total translational quantum number equal to $\sqrt{n_{x}^{2}+n_{y}^{2}+n_{z}^{2}}$. Therefore, $n$ is the radius of a one-eighth sphere in the positive octant of translational quantum number space. All states on the surface of the sphere have the same energy. Therefore, each state with energy between $\epsilon$ to $\epsilon + d\epsilon$ occupies the one-eighth spherical shell between $n$ and $n + dn$. The volume of this shell is
$$d g=\frac{4 \pi n^{2} d n}{8}$$
- Differentiating $\epsilon$ with respect to $n$ and substituting
$$d g=2 \pi V\left(\frac{2 m}{h^{2}}\right) \sqrt{\epsilon} d \epsilon$$
- now, substituting this we get
$$f(\epsilon)=\frac{2 \epsilon^{1 / 2}}{\pi^{1 / 2}(k T)^{3 / 2}} e^{-\epsilon / k T}$$
- Now, the translational energy of an individual molecule is $\epsilon = \frac{mc^2}{2}$
- where $c$ is the particle speed, so that $d\epsilon = mcdc$
- Note that we must have $f (\epsilon)d\epsilon = f (c)dc$ which follows from the idea that the probability of a particle assuming a certain energy must correspond to a certain speed.
$$f(c)=\left(\frac{2}{\pi}\right)^{1 / 2}\left(\frac{m}{k T}\right)^{3 / 2} c^{2} e^{-m c^{2} / 2 k T}$$
- This relationship, which plays a very important role in the kinetic theory of gases, is called the Maxwellian speed distribution
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/04/Annotation-2020-09-04-094143.png)
> - Useful properties that can be obtained from the Maxwellian speed distribution include the average speed, most probable speed and and the root-mean-squared speed respectively.
> $$\begin{array}{c}
\bar{c}=\int_{0}^{\infty} c f(c) d c=\left(\frac{8 k T}{\pi m}\right)^{1 / 2} \\
c_{m p}=\sqrt{\left(\frac{2 k T}{m}\right)} \\
\sqrt{c^{2}}=\int_{0}^{\infty} c^{2} f(c) d c=\frac{3}{2}\left(\frac{2 k T}{m}\right)=\frac{3}{2} c_{m p}
\end{array}$$

## Monatomic Gases
- Let us next consider a gas made up entirely of atoms. In that case the only other form of motion is that of the electrons orbiting the nucleus. The electronic partition function $q_e = \sum_k \exp({-\beta \epsilon_k})$.
- is a sum over quantum states. However, electronic energy states, in contrast to **quantum states**, are degenerate. Thus, we could also write
$$q_{e}=\sum_{k} g_{k} e^{-\beta \epsilon_{k}}=g_{0}+g_{1} e^{-\frac{\epsilon_{1}}{k T}}+g_{2} e^{-\frac{\epsilon_{2}}{k T}}+\cdots$$
- where now the summation is over energy states rather than quantum states.
- To evaluate $q_e$ we need to know the details for each specific atom. 
- However, recall that electronic energies are quite large, typically $20,000–80,000 \mathrm{K}$ in terms of characteristic temperature. Therefore, at reasonable temperatures, only a few terms in the summation are significant. 
- In fact, for most atoms, the room-temperature partition function is essentially equal to the first term in the summation. If that is the case, then $q_e = g_0$
- Ignoring electronic excitation, the fundamental relation for a monatomic ideal gas with no electronic excitation becomes
$$S\left[\frac{1}{T}, \frac{-\mu}{T}\right]=k e^{-\frac{\mu}{k T}}\left(\frac{2 \pi m k T}{h^{2}}\right)^{3 / 2} V g_{e}$$
- Now, recall that
$$d S\left[\frac{1}{T}, \frac{-\mu}{T}\right]=-U d \frac{1}{T}+\frac{p}{T} d V+N d \frac{\mu}{T}$$
- where $−U, p/T, \text{ and } N$ are the equations of state in the grand canonical representation. Evaluating $N$,
$$N=\frac{\partial S\left[\frac{1}{T}, \frac{-\mu}{T}\right]}{\partial \frac{-\mu}{T}}=\frac{1}{k} S\left[\frac{1}{T}, \frac{-\mu}{T}\right]=\frac{p V}{k T}$$
- This is the Ideal Gas Law we have discussed in Thermodynamics.
- Evaluating $U$, we obtain
$$U=\frac{-\partial S\left[\frac{1}{T}, \frac{-\mu}{T}\right]}{\partial \frac{1}{T}}=\frac{3}{2} T S\left[\frac{1}{T}, \frac{-\mu}{T}\right]=\frac{3}{2} p V=\frac{3}{2} N k T$$
- The average internal energy per atom is
$$u = \frac{U}{N} = \frac{3}{2} k_BT$$
- The entropy becomes
$$S=S\left[\frac{1}{T}, \frac{-\mu}{T}\right]+U \frac{1}{T}-N \frac{\mu}{T}=k\left[N+U \frac{1}{T}-N \frac{\mu}{T}\right]=k\left[\frac{5}{2}-\frac{\mu}{k T}\right]$$
- Finally, it is useful to calculate the specific heat $c_v$
$$c_v = \frac{\partial u}{\partial T}_V = \frac{3}{2} k_B$$
## Diatomic Gas
- For a diatomic gas, the total energy is $\epsilon = \epsilon_{tr} + \epsilon_{e} + \epsilon_r + \epsilon_v$
- Following the arguments made in discussing the monatomic gas, we write the internal energy portion of the partition function as
$$\sum_{k} e^{-\beta \epsilon_{k}}=\sum_{k} e^{-\beta \epsilon_{k t r}} \sum_{k} e^{-\beta \epsilon_{k e}} \sum_{k} e^{-\beta \epsilon_{k v}} \sum_{k} e^{-\beta \epsilon_{k r}}=q_{t r} q_{e} q_{v} q_{r}$$
- Thus, the partition function becomes $\ln Q = e^{-\gamma} q_{tr} q_e q_r q_v$
- We have already discussed the evaluation of the translational and electronic partition functions. We now consider rotation and vibration.
### Rotation
- Recall that for a rigid rotator $\epsilon_r = k \Theta_r J(J+1)$ where $\Theta_r$ is the characteristic rotational temperature. The rotational degeneracy is $g_J = 2J + 1$. Thus,
$$q_{r}=\sum_{J}(2 J+1) e^{-\frac{\epsilon_r}{k_B T}}=\sum_{J}(2 J+1) e^{-\frac{\Theta_{r} }{T}J(J+1)}$$
- One can approach the evaluation of this sum in several ways. The most accurate is to directly evaluate it numerically. The number of terms required will depend on the ratio $\Theta/T$. The higher the temperature, the more terms will be required. Alternatively, for $(\Theta/T)J(J + 1) << 1$, the sum can be approximated by an integral
$$q_{R} \simeq \int_{J=0}^{\infty}(2 J+1) e^{-\frac{\Theta_{R}}{T} J(J+1)} d J$$
- Defining $u = J(J + 1)$, the integral becomes
$$\int_{0}^{\infty} e^{-\frac{\Theta_{R}}{T} u} d u=\frac{T}{\Theta_{R}}$$
- This is referred as High Temperature Limit. But, the integral approximation is really the first term in an Euler–MacLaurin summation:
$$\begin{aligned}
\sum_{n=a}^{b} f(n)=& \int_{a}^{b} f(n) d n+\frac{1}{2}\{f(b)+f(a)\} \\
&+\sum_{j=1}^{\infty}(-)^{j}\left\{f^{(2 j-1)}(a)-f^{(2 j-1)}(b)\right\}
\end{aligned}$$
- The full equation then becomes:
$$q_{r}=\frac{T}{\Theta_{r}}\left[1+\frac{1}{3} \frac{\Theta_{r}}{T}+\frac{1}{15}\left(\frac{\Theta_{r}}{T}\right)^{2}+\frac{4}{315}\left(\frac{\Theta_{r}}{T}\right)^{3}+\cdots\right]$$
- There is a great advantage in using this equation to calculate the partition function at lower temperatures in that it converges quite rapidly compared to evaluating the sum for $q_r$ directly.
- There is a complication when the molecule is homonuclear (i.e. both atoms are the same type). For homonuclear molecules such as $H_2, O_2, N_2$, and so on, symmetry requirements prevent all possible values of the rotational quantum number. In fact, only even or odd ones are allowed, so that generally, taking $\sigma$ is a symmetry factor:
$$q_{r}=\frac{1}{\sigma} \frac{T}{\Theta_{r}} \left\{\begin{array}{ll}
\sigma=1 & \text { for heteronuclear } \\
\sigma=2 & \text { for homonuclear }
\end{array}\right.$$
- It is useful to explore the distribution of rotational states. This is given by the Boltzmann ratio
$$\frac{N_{J}}{N}=\frac{g_{J} e^{-J(J+1) \frac{\Theta_{r}}{T}}}{q_{r}(T)}$$
- The peak of the curve can be found by differentiating $N_J/N$. The result is
$$J_{\text{max}} = \sqrt{\left ( \frac{T}{2 \Theta_r}\right )}$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/04/Annotation-2020-09-04-114148.png)
- As the temperature increases, the distribution broadens as more and more energy levels are populated.
### Vibration
- The vibrational energy for a harmonic oscillator is $\epsilon_{\nu} = h \nu_{\nu}(\nu + 1/2)$
- However, before we use this expression to calculate the vibrational partition function, an issue of energy referencing must be resolved. The potential function of a real diatomic molecule will look similar to below graph:
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/04/Annotation-2020-09-04-121353.png)
-  In this coordinate system, the absolute energy of vibration is set to zero when there is a complete separation of the atoms that make up the molecule. This makes sense because
$$PE = -\int_r^{\infty} F(r) dr$$
- and as the atoms approach from a distance, there is initially no force and the potential energy is zero. As the distance closes, the electrostatic interaction force is initially attractive and the potential energy decreases. 
- When the force becomes repulsive, the potential energy increases. At small $r$ it reaches very large values.
- Because of this, and because referencing is important when working with reacting mixtures, it is usual to set the same zero reference when calculating the partition function. Therefore, we will write the vibrational energy as $\epsilon_{\nu} = h \nu_{\nu}(\nu + 1/2) - D_e$
- Here $D_e$ is called the electronic binding energy, and is the total depth of the potential well. (Note, this is different from the dissociation energy, $D_0$, which is $D_e$ minus the zero-point energy and is the energy required to dissociate the molecule from the ground vibrational state.)
- The partition function thus becomes
$$q_{v}=e^{\frac{D_{e}}{k_B T}} \sum_{\nu} e^{-\frac{h \nu(\nu+1 / 2)}{k_B T}}=e^{\frac{D_e}{k T}} \sum_{\nu} e^{-\frac{\Theta_{\nu}}{T}(\nu+1 / 2)}$$
- The sum can be expanded as
$$\sum_{\nu} e^{-\frac{\Theta_{\nu}}{T}(\nu+1 / 2)}=\sum_{\nu} e^{-\frac{\Theta_{\nu}}{2 T}(2 \nu+1)}=e^{-\frac{\Theta_{\nu}}{2 T}}\left[1+e^{-\frac{\Theta_{\nu}}{T}}+e^{-2 \frac{\Theta_{\nu}}{T}}+\cdots\right]$$
- Where $\Theta_{\nu}$ is the characteristic vibrational temperature. The term in brackets is a binomial expansion. Thus, the partition function can be written as
$$q_{\nu}=e^{\frac{D_e}{k_B T}} \frac{e^{-\frac{\Theta_{\nu}}{2 T}}}{1-e^{-\frac{\Theta_{\nu}}{T}}}=e^{\frac{D_{e}}{k_B T}} \frac{1}{2 \sinh \left(\Theta_{\nu} / 2 T\right)}$$

### Properties
- Substituting all the molecular partition functions into the full partition function, we have the fundamental relation for $T >> \Theta_r$ and $q_e = g_e$:
$$S\left[\frac{1}{T},-\frac{\mu}{T}\right]=e^{-\frac{\mu}{k T}}\left(\frac{2 \pi m k T}{h^{2}}\right)^{3 / 2} V\left(\frac{T}{\sigma \Theta_{r}}\right) \frac{e^{\frac{D_e}{k T}}}{2 \sinh \left(\Theta_{\nu} / 2 T\right)} g_e$$
- If we evaluate the equations of state, we would find that the perfect gas law still holds, and that the energy per molecule is
$$u=\frac{3}{2} k T+k T+\left[-D_{e}+\frac{k \Theta_{\nu}}{2} \operatorname{coth} \frac{\Theta_{\nu}}{T}\right]$$
- The other properties of interest are the entropy
$$s=\frac{S}{N}=k_B\left[\frac{7}{2}+\left(\frac{\Theta_{\nu}}{2 T} \operatorname{coth} \frac{\Theta_{\nu}}{2 T}-D_{e}\right)-\frac{\mu}{k_B T}\right]$$
- and the specific heat
$$c_{v}=k\left[\frac{3}{2}+1+\left\{\frac{\Theta_{\nu} / 2 T}{\sinh \left(\Theta_{\nu} / 2 T\right)}\right\}^{2}\right]$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/04/Annotation-2020-09-04-123810.png)
- We have seen that real diatomic molecules do not behave exactly like the simple rigid rotator/harmonic oscillator models. 
- If the vibrational and rotational states are merely distorted from the simple model, then one can still separate the molecular partition functions and use the more complete term expressions or experiment data to calculate the $q$’s. 
> #### For Reference:
> $$\ln Q = e^{-\gamma} q_{tr} q_e q_r q_v$$
- However, if there is coupling between the modes, then $q$ cannot be easily separated, and must be directly evaluated.
> ### For Example:
>  - Suppose that the sum of vibrational and rotational energies is
>  $$G(\nu) + F_{\nu}(J)$$
>  - where the subscript on $F$ indicates that the rotational energy depends on the vibrational state. Then we must write
>  $$q_{v, r}=\frac{1}{\sigma} \sum_{v} \sum_{J}(2 J+1) e^{-(h c / k T)\left[G(v)+F_{v}(J)\right]}$$

## Polyatomic Molecules:
- The principles for evaluating the partition function for polyatomic gases are similar to those we have already applied. 
- The results for translational energy are identical to those for monatomic and diatomic gas assemblies, as translational energy describes the motion of the center of mass of any molecular structure. 
- However, evaluating the internal modes of energy is somewhat more difficult because of the many modes of motion and the likelihood that they interact. For a body made up of $n$ atoms, there are $3n$ degrees of freedom. 
- Three of these are taken up by translational motion, leaving $3n − 3$ modes for vibrational and rotational motion. 
- For a linear molecule, such as $CO_2$, there are only two rotational modes, thus there are $3n − 5$ possible vibrational modes. 
- For the general nonlinear case, there are three rotational modes and thus $3n − 6$ vibrational modes.
- There is a concept called the “**equipartition of energy**.”