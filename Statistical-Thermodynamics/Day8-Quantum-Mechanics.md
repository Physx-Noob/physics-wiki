---
title: Day 8: Quantum Mechanics
description: 
published: true
date: 2020-08-30T03:03:12.625Z
tags: 
editor: markdown
---

# Quantum Mechanics
## The Postulates of Quantum Mechanics
### Postulate 1
Each system can be characterized by a wave function, which may be complex
$$\Psi(\vec{r},t)$$
and which contains all the information that is known about the system.
### Postulate 2
The wave function is defined such that
$$p(\vec{r}, t) d V=\Psi^{*}(\vec{r}, t) \Psi(\vec{r}, t) d V=|\Psi(\vec{r}, t)|^{2}$$
is the probability of finding the system in the volume element dV. The consequence of this is that
$$\int_{-\infty}^{\infty} \Psi^{*}(\vec{r}, t) \Psi(\vec{r}, t) d V=1$$
That is, the system will be found somewhere.
### Postulate 3
With every dynamical variable, there are associated operators
$$\begin{aligned}
\vec{r}: \vec{r}_{o p} &=\vec{r} \\
\vec{p}: \vec{p}_{o p} &=\vec{p} \\
\epsilon: \epsilon_{o p} &=\epsilon \\
B(\vec{r}, t): B_{o p} &=B(\vec{r},-i \hbar \vec{\nabla})
\end{aligned}$$
### Postulate 4
The expectation value of any physical observable is
$$\langle B\rangle=\int_{-\infty}^{\infty} \Psi^{*}(\vec{r}, t) B_{o p} \Psi(\vec{r}, t) d V$$

---
- The wave function is described by Schrödinger’s equation, which starts with the classical form for conservation of energy ($H$ is the Hamiltonian of classical mechanics)
$$H=\frac{p^{2}}{2 m}+V(\vec{r}, t)=\epsilon$$
- and substitutes the operators so that
$$-\frac{\hbar^{2}}{2 m} \nabla^{2} \Psi(\vec{r}, t)+V(\vec{r}, t) \Psi(\vec{r}, t)=i \hbar \frac{\partial \Psi(\vec{r}, t)}{\partial t}$$
## Solutions of the Wave Equation
- As thermodynamicists, we are interested in obtaining the allowed quantum states of individual atoms and molecules so that we may calculate the allowed quantum states of ensemble members. 
- The complete specification of the atomic or molecular quantum state requires understanding translational and electronic motion in the case of atoms, with rotational and vibration motion also important for molecules.
- We start by assuming that the potential energy term $V$ is a function only of position
$$V(\vec{r}, t) = V(\vec{r})$$
- As a result, the wave equation can be written as
$$i \hbar \frac{\partial \Psi(\vec{r}, t)}{\partial t}=-\frac{\hbar^{2}}{2 m} \nabla^{2} \Psi(\vec{r}, t)+V(\vec{r}) \Psi(\vec{r}, t)$$
- We assume that the wave function can be written as a product of a time-dependent function and a spatially dependent function
$$\Psi(\vec{r}, t) = \psi(\vec{r}) \phi (t)$$
- Substituting this into the wave equation and then dividing by the same function, we obtain
$$\frac{i \hbar}{\phi} \frac{\partial \phi}{\partial t}=\frac{1}{\psi}\left[-\frac{\hbar^{2}}{2 m} \nabla^{2} \psi+V(\vec{r}) \psi\right]$$
- Since the two sides are functions of different variables, they must be equal to within an arbitrary constant, so that the time-dependent wave equation becomes
$$\frac{i \hbar}{\phi} \frac{\partial \phi}{\partial t}= C$$
- and the spatially dependent wave equation becomes
$$\frac{1}{\psi}\left[-\frac{\hbar^{2}}{2 m} \nabla^{2} \psi+V(\vec{r}) \psi\right] = C$$
- The solutions are:
$$\begin{array}{c}
\phi(t)=\exp \left(-i \frac{C}{\hbar} t\right) \\
\Psi(\vec{r}, t)=\psi(\vec{r}) \exp \left(-i \frac{C}{\hbar} t\right)
\end{array}$$
- It turns out that the separation constant $C$ has a very important physical meaning which we can understand if we use the wave function to calculate the expectation value of the energy:
$$\langle\epsilon\rangle=\int_{V} \Psi^{*}\left(i \hbar \frac{\partial}{\partial t}\right) \Psi d V=\int_{V} \psi^{*} e^{i \frac{C}{\hbar} t} C \psi e^{-i \frac{C}{\hbar} t} d V=C$$
- Thus, $C$ is equal to the expectation value of the energy, and the spatially dependent wave equation becomes
$$-\frac{\hbar^{2}}{2 m} \nabla^{2} \psi+V(\vec{r}) \psi=\epsilon \psi$$
- This equation is also called the **stationary wave equation**, because its solutions result in expectation values of the dynamical properties that do not depend on time. 
- To solve it requires two boundary conditions in space, and knowledge of the potential energy function.
- We can solve for the motion of a **single particle** using the above equations. 
- For a **two particle system**, say a diatomic molecule or an atom with a single electron, the energy becomes
$$\epsilon=\frac{p_{1}^{2}}{2 m_{1}}+\frac{p_{2}^{2}}{2 m_2^{2}}+V(\vec{r})$$
- transforming the wave equation into center of mass coordinates results in the following equations for external and internal motion:
> $$\frac{\hbar^{2}}{2 m_{t}} \nabla^{2} \psi_{e}+\epsilon_{e} \psi_{e}=0$$
> $$\frac{\hbar^{2}}{2 \mu} \nabla^{2} \psi_{i n t}+\left(\epsilon_{e}-V(\vec{r})\right) \psi_{e}=0$$
> $$\mu=\frac{m_{1} m_{2}}{m_{1}+m_{2}}$$
### The Particle in a Box
- Equation for single particle in a Quantum State becomes
$$\frac{\hbar^{2}}{2 m} \frac{\partial \psi^{2}}{\partial^{2} x}=-\epsilon_{x} \psi$$
- $\psi(0)=\psi(L)=0$
- The solution for this equation is
$$\psi(x)=A \sin \left[\sqrt{\frac{2 m \epsilon_{x}}{\hbar^{2}}} x\right]+B \cos \left[\sqrt{\frac{2 m \epsilon_{x}}{\hbar^{2}}} x\right]$$
- applying the boundary values
$$0 = A \sin \left[\sqrt{\frac{2 m \epsilon_{x}}{\hbar^{2}}} x\right]$$
- constraint on energy levels of system
$$\epsilon_{x}=\frac{\hbar^{2} \pi^{2}}{2 m L} n_{x}^{2}$$
- normalization gives us coefficients: $\int | \psi |^2 dx = 1 \implies A = \sqrt{\frac{2}{L}}$
- and the stationary wave function becomes
$$\psi(x)=\sqrt{\frac{2}{L}} \sin \left(\frac{\pi n_{x} x}{L}\right), n_{x}=0,1,2, \ldots$$
> #### Few Extensions:
> - The three-dimensional problem is now easily solved. 
> - Because the potential function is zero, the three coordinate directions are independent of each other. 
> - Therefore, the solutions for the y and z directions are the same as for the x direction, assuming the appropriate dimension is used. 
> - Assuming that the box is a cube, we thus have
> $$\epsilon=\epsilon_{x}+\epsilon_{y}+\epsilon_{z}=\frac{h^{2}}{8 m V^{2 / 3}}\left(n_{x}^{2}+n_{y}^{2}+n_{z}^{2}\right)$$
> $$\psi(\vec{r})=\sqrt{\frac{8}{L^{3}}} \sin \left(\frac{\pi n_{x} x}{L}\right) \sin \left(\frac{\pi n_{y} y}{L}\right) \sin \left(\frac{\pi n_{z} z}{L}\right)$$
> - An important finding is that the energy is a function of the volume of the box. 
> We will see that for an ideal gas, this leads to all the volume dependency in the fundamental relation.
> $$\begin{array}{lllll}
> \hline n_{x} & n_{y} & n_{z} & n_{x}^{2}+n_{y}^{2}+n_{z}^{2} & g \\
\hline 1 & 1 & 1 & 3 & 1 \\
2 & 1 & 1 & 6 & \\
1 & 2 & 1 & 6 & 3 \\
1 & 1 & 2 & 6 & \\
\hline
\end{array}$$
> - It is very important to note that different combinations of the three quantum numbers can result in the same energy.
> - Quantum state have the same energy, they are often lumped together and identified as an “energy state” in contrast to a “quantum state” or “eigenstate.” The energy state is then said to be **degenerate**. 
> - The letter $g$ is used to denote the value of the degeneracy.
> - The average kinetic energy of an atom or molecule is equal to $\langle \epsilon \rangle = \frac{3}{2} k_B T$
> - A typical value of the translational quantum number at room temperature is about $10^8$

### Internal Motion
- Let's only explore analytic solutions for the simplest cases, the one-electron or hydrogen atom and the diatomic molecule. We will resort to numerical methods to explore more realistic behavior.
- We start with the stationary wave equation
$$\frac{\hbar^{2}}{2 \mu} \nabla^{2} \psi_{i n t}+\left(\epsilon_{i n t}-V(\vec{r})\right) \psi_{i n t}=0$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/29/sphersyst.png)
- Converting this equation into spherical coordinates
$$\begin{aligned}
\left[\frac{1}{r^{2}} \frac{\partial}{\partial r}\left(r^{2} \frac{\partial}{\partial r}\right)+\frac{1}{r^{2} \sin ^{2} \theta} \frac{\partial^{2}}{\partial \phi^{2}}\right.&\left.+\frac{1}{r^{2} \sin \theta} \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial}{\partial \theta}\right)\right] \psi_{ i n t} \\
&+\frac{2 \mu}{\hbar^{2}}\left[\epsilon_{i n t}-V_{i n t}(r)\right] \psi_{i n t}=0
\end{aligned}$$
- Again we pursue separation of variables, defining
$$\psi_{\text{int}} (r, \theta, \phi) = R(r) Y(\theta, \phi)$$
- Plugging this in the previous equation, we have
$$\frac{1}{R} \frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)+\frac{2 \mu r^{2}}{\hbar^{2}}\left[\epsilon_{i n t}-V_{i n t}(r)\right]=-\frac{1}{Y}\left[\frac{1}{\sin \theta} \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)+\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}}\right]$$
- Calling the separation variable $\alpha$, we get a radial equation and one that contains all the
angular dependence
$$\frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)+\left\{\frac{2 \mu r^{2}}{\hbar^{2}}\left[\epsilon_{i n t}-V_{i n t}(r)\right]-\alpha\right\} R=0$$
$$\left[\frac{1}{\sin \theta} \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial Y}{\partial \theta}\right)+\frac{1}{\sin ^{2} \theta} \frac{\partial^{2} Y}{\partial \phi^{2}}\right]=-\alpha Y$$
- Separating the angular wave equation using $Y(\theta, \phi) = \Theta(\theta)\Phi(\phi)$,we get
$$\begin{array}{c}
\frac{d^{2} \Phi}{d \phi^{2}}+\beta \Phi=0 \\
\frac{1}{\sin \theta} \frac{d}{d \theta}\left(\sin \theta \frac{\partial \Theta}{\partial \theta}\right)+\left(\alpha-\frac{\beta}{\sin ^{2} \theta}\right) \Theta=0
\end{array}$$
- where $\beta$ is the separation constant. 
- Note that neither equation depends on the potential energy term, $V(r)$, so they can be solved once and for all. The general solution for $\Phi$ is simply $\Phi(\phi) = \exp(i \beta^{1/2} \phi)$
- This function must be continuous and single valued, so $\Phi(\phi) = \Phi(\phi + 2\pi)$. This is true if $\beta^{1/2}$ is constant, and we name it $m_l = 0, \pm 1, \pm 2, \ldots$
- Plugging the expression for $\beta$ into the equation for $\Phi$, we get
$$\frac{1}{\sin \theta} \frac{\partial}{\partial \theta}\left(\sin \theta \frac{\partial \Theta}{\partial \theta}\right)+\left(\alpha-\frac{m_{l}^{2}}{\sin ^{2} \theta}\right) \Theta=0$$
- This is a Legendre equation.
- To satisfy the boundary conditions
we must have $\alpha = l(l + 1), l = i + |m_l| , i = 0, 1, 2, 3, \ldots$ 
- The solution is the associated Legendre function
$$\Theta=P_{l}^{|m_l|}(\cos \theta)=\frac{1}{2^l l !}\left(1-\cos ^{2} \theta\right)^{|m_l| / 2} \frac{d^{|m_l|+l}}{d(\sin \theta)^{|m_l|+l}}\left(\sin ^{2} \theta-1\right)^{l}$$
- So, the angular part becomes:
$$Y_l^{m_l}(\theta, \phi) = Y_{l, m_l}(\theta, \phi) = C_{l, m_l}P_{l}^{|m_l|}(\cos \theta) e^{im_l \phi}$$
- $Y_l^{m_l}(\theta, \phi) = Y_{l, m_l}(\theta, \phi)$ is the popular **Spherical Harmonics** used in Electromagnetism and other fields. A very useful mathematical tool.
- Here, $C_{l, m_l}$ is the normalization constant
$$C_{l, m_{l}}=\frac{1}{(2 \pi)^{1 / 2}}\left[\frac{(2 l+1)\left(l-\left|m_{l}\right|\right) !}{2\left(l+\left|m_{l}\right|\right) !}\right]^{1 / 2}$$
- The integer constants $l$ and $m_l$ turn out to be quantum numbers associated with angular momentum.
- If we calculated the angular momentum of our system
- $\langle L^2 \rangle = l(l+1)\hbar^2$
- Thus $l$ determines the expectation value of the angular momentum and is called the **angular momentum quantum number**.
- $\langle L_z \rangle = m_l \hbar$
- Normally, atoms or molecules are randomly oriented. However, in the presence of a magnetic field they will align. Thus, $m_l$ is called the **magnetic quantum number**.
### The Hydrogenic Atom
- Assume that the potential energy term is given by Coulomb’s law:
$$V(r)=\int_{\infty}^{r} \frac{e^{2}}{4 \pi \epsilon_{0}} \frac{d r}{r^{2}}=-\frac{e^{2}}{4 \pi \epsilon_{0} r}$$
- Starting with the radial wave equation
$$\frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)+\left\{\frac{2 \mu r^{2}}{\hbar^{2}}\left[\epsilon_{i n t}-V_{i n t}(r)\right]-\alpha\right\} R=0$$
- It is useful to transform this equation so that
$$\frac{1}{\rho^{2}} \frac{d}{d \rho}\left(\rho^{2} \frac{d R}{d \rho}\right)-\left[\frac{l(l+1)}{\rho^{2}}-\frac{n}{\rho}+\frac{1}{4}\right] R=0$$
- where $\rho=\frac{2 r}{n a_{0}}, n^{2}=-\frac{\hbar^{2}}{2 \mu a_{0}^{2} \epsilon_{e l}},$ and $a_{0}=-\frac{\hbar^{2}}{\pi \mu e^{2}}$
- Edmond Laguerre solved the above equation. so the solution is named as Laguerre Polynomials.
$$R_{n l}(\rho)=-\left\{\frac{(n-l-1) !}{2 n[(n+l) !]^{3}}\right\}^{1 / 2}\left(\frac{2}{n a_{0}}\right)^{3 / 2} \rho^{l} \exp (-\rho / 2) L_{n+1}^{2 l+1}(\rho)$$
- where $L_{n+1}^{2 l+1}(\rho)$ is
$$L_{n+1}^{2 l+1}(\rho)=\sum_{k=0}^{n-l-1}(-1)^{k+1} \frac{[(n+l) !]^{2}}{(n-l-1-k) !(2 l+1+k) ! k !} \rho^{k}$$
- Again we obtain an index, $n$, called the **principal quantum number**. It can take on values $n = 1, 2, 3, \ldots$ 
- Values of $l$, the angular momentum quantum number, are restricted to being less than $n$, or $l = 0, 1, 2, \ldots , n − 1$.
> #### Atomic Orbitals we are aware of:
> ![enter image description here](https://upload.wikimedia.org/wikipedia/commons/c/c7/Orbitales.png)
> Since we have the complete wavefunction $\psi_{\text{int}} = R_{n l}(\rho)Y_l^{m_l}(\theta, \phi)$, it's plotting for different values of $n, l, m_l$ will reveal us different shapes of atomic orbitals as depicted above. 
> Image Source: [Wikimedia Commons](https://commons.wikimedia.org/wiki/File:Orbitales.png)
- We have the wave function $\psi_{\text{int}} = R_{n l}(\rho)Y_l^{m_l}(\theta, \phi)$, solving for the energy
$$\epsilon_{n}=-\frac{Z^{2} e^{4} \mu}{32 \pi^{2} \epsilon_{0}^{2} \hbar^{2}} \frac{1}{n^{2}}, n=1,2,3, \ldots$$
- The total degeneracy is $g_n = 2n^2$
> #### Fasinating Observation from this Energy Equation
> - Difference in energy levels $\Delta E_{n_1, n_2}$
> $$\Delta E_{n_1, n_2} = \epsilon_{n_1} - \epsilon_{n_2} = -\frac{Z^{2} e^{4} \mu}{32 \pi^{2} \epsilon_{0}^{2} \hbar^{2}} \frac{1}{n_1^{2}} + \frac{Z^{2} e^{4} \mu}{32 \pi^{2} \epsilon_{0}^{2} \hbar^{2}} \frac{1}{n_2^{2}}$$
> - Simplifying further we get
> $$\Delta E_{n_1, n_2} = \epsilon_{n_1} - \epsilon_{n_2} = \left \{ \frac{Z^{2} e^{4} \mu}{32 \pi^{2}  \epsilon_{0}^{2} \hbar^{2}} \right \} \left ( \frac{1}{n_2^{2}} - \frac{1}{n_1^{2}}\right )$$
> - Rydberg's Equation:
> $$\Delta E = R \left ( \frac{1}{n_2^{2}} - \frac{1}{n_1^{2}}\right )$$
> - The Rydberg's Constant reads as follows
> $$R = \left \{ \frac{Z^{2} e^{4} \mu}{32 \pi^{2} \epsilon_{0}^{2} \hbar^{2}} \right \}$$