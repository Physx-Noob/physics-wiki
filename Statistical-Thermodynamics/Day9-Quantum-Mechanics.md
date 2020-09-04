---
title: Day 09: Quantum Mechanics
description: 
published: true
date: 2020-09-04T08:21:28.379Z
tags: 
editor: markdown
---

# Quantum Mechanics
## Solutions of the Wave Equation contd ..,
### The Born–Oppenheimer Approximation and the Diatomic Molecule
- The analytic solution of the wave equation for molecules is a complex, time dependent problem.
- There is a great simplification if the electronic motion can be decoupled from the nuclear motion, as pointed out by Max Born and J. Robert Oppenheimer in 1927 using the fact that the mass of an electron is $1/1830$ of a proton.
- The electrons are moving much faster than the nuclei, and approach steady motion rapidly. 
- The effect of the electrons on the nuclei is an effective force between the nuclei that only depends on the distance between them. 
- The force can be described as due to a potential field. We know that stable potentials (i.e. ones that can result in chemical bonding) are attractive at a distance and repulsive as the nuclei approach each other. 
- One simple function that contains all this behavior is the **Morse potential**
$$V(r) = D_e [1 - e^{-\beta}(r-r_e)^2]^{1/2}$$
- Real potentials must either be determined experimentally or from numerical solutions of the wave equation.
- But most bonding potentials look like the below one:
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/30/Annotation-2020-08-30-094624.png)
- If we concern ourselves with molecules in quantum states such that only the **lower-energy portion of the potential is important**, then the typical potential looks much like that for a harmonic oscillator. In this case the force between the nuclei and potential energy respectively are:
$$F = - k(r-r_e) \text{ and } V(r) = k\frac{(r-r_e)^2}{2}$$
- Consider the two extra modes of motion available to a molecule: rotational and vibrational.
- **Rotational:** In a real molecule, rotation will exert a centripetal force that will cause the bond between the nuclei to stretch. However, if we assume that the two nuclei are rigidly affixed to each other, then we can use the angular solution to the wave equation that we developed above. 
- This is called the **rigid rotor approximation**. The angular momentum is
$$L = I \omega \text{ where $I$ is moment of Inertia } I = \mu r^2$$
$$\text{and $\mu$ is the reduced mass } \mu = \frac{m_1 m_2}{m_1 + m_2}$$
- The energy of rotation then becomes
$$\epsilon_{R}=\frac{1}{2} I \omega^{2}=\frac{L^{2}}{2 I}=l(l+1) \frac{\hbar^{2}}{2 \mu r^{2}}$$
- For molecular rotation it is common to use $J$ as the rotational quantum number, so
$$\epsilon_{R} = J(J+1) \frac{\hbar^{2}}{2 \mu r^{2}}$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/30/Untitled.png)
- **Vibration:** or the relative motion of nuclei with respect to each other.
- If we neglect rotation and consider that the intermolecular force acts like a linear spring, then we can use the harmonic potential in Radial Wave Equation as follows:
$$\frac{\hbar^{2}}{2 \mu r^{2}} \frac{d}{d r}\left(r^{2} \frac{d R}{d r}\right)+\left\{\epsilon-V(r)-\frac{\hbar^{2}}{2 \mu r^{2}} l(l+1)\right\} R=0$$
- This equation can be solved analytically using series methods. 
- Introducing the transformations $K(r) = rR(r) \text{ and } x = r − r_e$ the equation becomes
$$\frac{d K^{2}}{d x^{2}}+\frac{2 \mu}{\hbar^{2}}\left(\epsilon_{V}-\frac{k x^{2}}{2}\right) K=0$$
- Introducing a non-dimensional form for energy (where $v$ is a characteristic frequency)
$$\lambda=\frac{2 \epsilon_{V}}{h v_{V}}, \text { where } v_{V}=\frac{1}{2 \pi} \sqrt{\frac{k}{\mu}}$$
- and defining a new independent variable $y=\left(\frac{2 \pi v_{V} \mu}{\hbar}\right)^{1 / 2} x$
- one obtains a non-dimensional form of the radial wave equation
$$\frac{d^{2} K}{d y^{2}}+\left(\lambda-y^{2}\right) K=0$$
- Let us examine the solution as $y \to \infty$
$$\frac{d^{2} K}{d y^{2}}-y^{2} K \cong 0 \Rightarrow K \cong \exp \left(-y^{2} / 2\right)$$
- Assume that we can express $K(y)$ as a factor $H(y)$ times the large $y$ limiting solution $K(y)=H(y) \exp \left(-y^{2} / 2\right)$ . Then, we have
$$\frac{d^{2} H}{d y^{2}}-2 y \frac{d H}{d y}+(\lambda-1) H=0$$
- This is another equation solved by a nineteenth-century mathematician, Charles **Hermite**. It has solutions only when $(\lambda-1)=2 v, v=0,1,2,3, \ldots$ .
- $H(y)$ is the Hermite polynomial of degree $u$:
$$H_{u}(y)=(-1)^{u} e^{y^{2}} \frac{d^{u}}{d y^{u}}\left(e^{-y^{2}}\right)$$
- The Energy is:
$$\epsilon_{v}=\left(v+\frac{1}{2}\right) h v_{v}, \text { where } v=0,1,2,3, \ldots$$
- The Energy never goes to Zero!! This lowest energy level is called **zero-point energy**.
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/30/Annotation-2020-08-30-101821.png)
- Putting the **rotational and vibrational** solutions together, the total energy of these two modes becomes
$$\epsilon_{R}+\epsilon_{v}=\frac{\hbar^{2}}{2 I_{e}} J(J+1)+h v_{v}\left(v+\frac{1}{2}\right)$$
- with $J = 0, 1, 2, 3, \ldots \text{ and }v = 0, 1, 2, 3, \ldots$ having degeneracies $g_J = 2J + 1\text{ and }g_v = 1$
- The energy is more commonly expressed as
$$F(J)=\frac{\epsilon_{R}}{h c}=B_{e} J(J+1) \text { and } G(\mathrm{v})=\frac{\epsilon_{v}}{h c}=\omega_{e}\left(v+\frac{1}{2}\right)$$
- whose units are $\mathrm{cm}^{-1}$. This is given by Spectroscopists. Alternatively, we can express the energy in terms of characteristic temperatures
$$T_{R} \equiv \frac{\hbar^{2}}{2 I_{e} k}=\frac{B_{e}}{(k / h c)} \text { and } T_{V} \equiv \frac{h v_{v}}{k}=\frac{G_{v}}{(k / h c)}$$
> #### For N2, for example
> $$\begin{array}{ll}
B_{e}=1.998 \mathrm{cm}^{-1}, & T_{R}=2.87 \mathrm{K} \\
\omega_{e}=2357.6 \mathrm{cm}^{-1}, & T_{V}=3390 \mathrm{K}
\end{array}$$

- $B_e << \omega_e$, the rotational energy levels are much more closely spaced than the vibrational levels.

## Real Atomic Behavior
Unfortunately, real atoms (including the hydrogen atom) are not very well described by the simple theory. The following contribute to actual structure:
- Quantum mechanics of identical particles: the Pauli exclusion principle.
- Higher-order effects:
  + spin–orbit coupling
  + relativistic effects
  + nuclear spin
  + Zeeman effect.
- Multiple electrons

### Pauli Exclusion Principle
- The Pauli exclusion principle states that no two electrons of a multi-electron atom can assume the same quantum state. 
- This comes about because of symmetry considerations when dealing with multiple particles. Consider, for example, the wave equation for two identical particles in a box:
$$-\frac{\hbar^{2}}{2 m}\left(\frac{\partial \psi^{2}}{\partial^{2} x_{1}}+\frac{\partial \psi^{2}}{\partial^{2} x_{2}}\right)+V \psi=0$$
- If the particles are interchanged, the probability density of the system should be unchanged. This means $p(1,2) = p(2,1)$
- For probabilities to be unchanged we have $p(\vec{r}, t) d V=\Psi^{*}(\vec{r}, t) \Psi(\vec{r}, t) d V=|\Psi(\vec{r}, t)|^{2}$
- Giving us $\psi(1,2) = \psi(2,1)$ for symmetric wavefunction and $\psi(1,2) = -\psi(2,1)$ for antisymmetric wavefunction.
- Assume we can write the potential energy function as $V = V(x_1) + V(x_2) = V(1) + V(2)$, then
$$\psi_{\alpha, \beta}(1,2) = \psi_{\alpha}(1) \psi_{\beta}(2)$$
- here $1,2$ represent particle and $\alpha, \beta$ represent quantum state. We can now construct a wave
function that satisfies the symmetry requirement
$$\psi_{\alpha, \beta}(1,2)=\frac{1}{\sqrt{2}}\left\{\psi_{\alpha}(1) \psi_{\beta}(2) \pm \psi_{\alpha}(2) \psi_{\beta}(1)\right\}$$
- This clearly satisfies $\psi(1,2) = \pm \psi(2,1)$. Here, if the two particles are in the same quantum state, and the wave function is anti-symmetric, then $\psi \to 0$. 
- Thus, fermions cannot occupy the same quantum state at the same time. 
- Hence, the Pauli exclusion principle and the structure of all multi-electron atoms derive from this fact.
### Higher-Order Effects: Spin–Orbit Coupling
- Electrons have spin, and thus angular momentum, as does the entire atom. These two motions generate magnetic fields that interact, thus changing the energies of individual quantum states. 
- The total angular momentum vector is $\vec{J} = \vec{L} + \vec{S}$. We can show that
$$\begin{array}{l}
J=\sqrt{j(j+1)} \hbar \text { and } J_{z}=m_{j} \hbar \\
m_{j}=-j,-j+1, \ldots, j-1, j \\
l=0: j=1 / 2 \\
l \neq 0: j=l \pm 1 / 2
\end{array}$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/31/fine-structure-splitting.png)

### Higher-Order Effects: Relativistic Effects
- If we included relativistic effects we would find that they change the quantum state energies by an amount similar to spin–orbit splitting and approximately equal to
$$\Delta \epsilon_{R}=-\frac{Z^{2} \alpha^{2}}{e n^{2}}\left(\frac{4 n}{l+1 / 2}-3\right)\left|\epsilon_{n}\right|$$

> $\alpha$ is the structure constant with
> $$\alpha \sim \frac{1}{137}$$

### Higher-Order Effects: Nuclear Spin
- As with electrons, nuclei have angular momentum or spin. Spin induces a magnetic dipole moment that interacts with orbital angular momentum, although to a much lesser degree than electron spin. 
- This interaction leads to a splitting of otherwise degenerate quantum levels. The resulting splits are called the hyperfine structure, and from a thermodynamics point of view are usually ignored.

### Higher-Order Effects: The Zeeman Effect
- If an atom is placed in an external magnetic field $H$, the quantum states will be altered in a way that can cause level splitting. This is known as the **Zeeman effect**. 
- The size of the splitting depends on the orientation of the total orbital angular momentum vector $J$ and $H$, and therefore depends on the magnetic quantum number $m_j$. The energy splitting is given by
$$\Delta \epsilon_{z}=\frac{e \hbar}{2 m_{e} c} g m_{j} H$$
- where $g$ is the Lande $g$ factor.
