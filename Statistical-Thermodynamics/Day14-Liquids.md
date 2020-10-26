---
title: Day 14: Liquids
description: 
published: true
date: 2020-10-26T02:00:26.561Z
tags: 
editor: markdown
---

# Liquids
- Liquids represent a significant complication over the systems we have discussed so far. 
- In the case of dense gases, for example, to evaluate the configuration integral we assumed that the total potential energy is the sum of the pairwise potential energies between molecules. 
- We pointed out that this only strictly applies to gases that are not too dense. 
- However, in a liquid, atoms and/or molecules are very closely spaced, and the potential experienced by each particle depends on the positions of all the surrounding particles out to some distance. 
- This is true in solids as well, but unlike solids, in a liquid there is diffusion and particles change position with respect to each other constantly. 
- As a result, statistical methods are most suited to analyzing liquid behavior. 
- In this session we will introduce the concept of distribution functions and ultimately relate thermodynamic properties to the radial distribution function. 
- Finally, we will discuss the use of molecular dynamics simulations to obtain the radial distribution function and the thermodynamic properties.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/24/ann.png)
# The Radial Distribution Function and Thermodynamic Properties
- We start
by introducing the generalized distribution function, where $Z_{\phi}$ is the configuration integral:
$$
P^{(N)}\left(r_{1}, r_{2}, \ldots, r_{N}\right) d r_{1} d r_{2} \cdots d r_{N}=\frac{e^{-\phi / k_{B} T} d r_{1} d r_{2} \cdots d r_{N}}{Z_{\phi}}
$$
- This function describes the probability that molecule $1$ is in volume $dr_1$ at $r_1$, molecule $2$ in $dr_2$ at $r_2$, and so on. 
- However, $N$ is normally a very large number. Suppose we deal with a reduced system with $n$ molecules and ask what is the probability that molecule $1$ is in $dr_1$ at $r_1, \dots ,$ molecule $n$ is in $dr_n$ at $r_n$, irrespective of the configuration of the remaining $N − n$ molecules. This can be written
$$
P^{(n)}\left(r_{1}, r_{2}, \ldots, r_{n}\right)=\frac{\int \cdots \int e^{-\phi / k_{B} T} d r_{n+1} \cdots d r_{N}}{Z_{\phi}}
$$
- Assuming all the particles are identical, we could ask what is the probability that any $n$ of them are located in position $r_1 \dots r_n$ irrespective of the configuration of the rest. This is the $n$-particle density, $\rho$ in this development is a number density:
$$
\rho^{(n)}\left(r_{1}, \ldots, r_{n}\right)=\frac{N !}{(N-n) !} P^{(n)}\left(r_{1}, \ldots, r_{n}\right)
$$
- The simplest distribution function is $\rho^{(1)}(r_1)$, which is the number density. In a crystal this will be a periodic function, but in a fluid all points are equivalent and $\rho^{(1)}(r_1)$ is independent of $r_1$. Therefore,
$$
\frac{1}{V} \int \rho^{(1)}\left(r_{1}\right) d r_{1}=\rho^{(1)}=\frac{N}{V}=\rho
$$
- We now define a correlation function, $g^{(n)}$, relating $\rho^n$ to $\rho^{(n)}$:
$$\rho^{(n)}\left(r_{1}, \ldots, r_{n}\right) = \rho^n g^{(n)} \left(r_{1}, \ldots, r_{n}\right)$$
- $g^{(n)}$ is correlation function which takes into account of the interactions. Hence, we can show that
$$
\begin{aligned}
g^{(n)}\left(r_{1}, \ldots, r_{n}\right) &=\frac{V^{n} N !}{N^{n}(N-n) !} \frac{\int \cdots \int e^{-\phi / k_{B} T} d r_{n+1} \cdots d r_{N}}{Z_{\phi}} \\
&=V^{n}\left(1+\mathcal{O}\left(N^{-1}\right)\right) \frac{\int \cdots \int e^{-\phi / k_{B} T} d r_{n+1} \cdots d r_{N}}{Z_{\phi}}
\end{aligned}
$$
- $g^{(2)}(r_1, r_2)$ is especially important since it can be determined experimentally using light-scattering
techniques. 
- In a liquid of spherical symmetry, where particles are randomly distributed, $g^{(2)}$ depends only on the relative distance between particles. 
- It is usually designated merely as $g(r)$ and called the “**radial distribution function**” (RDF). The integral of the radial distribution function over all space is
$$
\int_{0}^{\infty} \rho g(r) 4 \pi r^{2} d r=N-1 \approx N(\text { for large } N)
$$
- One can show that if we assume that the total potential energy of the $N$-body system is pairwise additive, that is
$$
U_{N}\left(r_{1}, \ldots, r_{N}\right)=\sum_{i<j} \phi\left(r_{i j}\right)
$$
- then all thermodynamic functions can be written in terms of $g(r)$. The number density of molecules with centers between $r$ and $r + dr$ relative to a specific molecule is
$$
4 \pi r^{2} \frac{N}{V} g(r) d r
$$
- For a spherically symmetric pairwise potential function, it follows that
$$
4 \pi r^{2} \phi(r) \frac{N}{V} g(r) d r
$$
- is the inter-molecular potential energy between the central molecule and other molecules with centers between $r$ and $r + dr$. One can then show that
$$u=\frac{3}{2} R k_{B} T+\frac{N_{A}}{2} \rho \int_{0}^{\infty} \phi(r) g(r, \rho, T) 4 \pi r^{2} d r$$
$$p=\rho k_{B} T-\frac{\rho^{2}}{6} \int_{0}^{\infty} r \frac{d \phi(r)}{d r} g(r, \rho, T) 4 \pi r^{2} d r$$
# Molecular Dynamics Simulations of Liquids
- Molecular dynamics (MD) involves following the microscopic behavior at the atomistic level by making the **Born–Oppenheimer approximation** and solving $F = ma$ for all the nuclei present. 
- One can calculate the forces using either empirical or quantum methods, but empirical methods are almost always used for reasons of computational efficiency.
- The advantage of MD is that it accounts directly for the thermal motion of atoms and molecules. 
- It directly outputs position and velocity of all particles as a function of time. 
- Thus, it provides all information about phase space, the space determined by the position, velocity, and orientation of all molecules. 
- If phase space is known at all times, then both the thermodynamic properties and dynamic behavior of the system can be determined. 
- MD has been used for a wide array of problems, including :
  + protein folding, 
  + thermodynamic properties, 
  + stress–strain relations, 
  + surface tension of drops, 
  + behavior of supercritical fluids, 
  + micro heat transfer, and 
  + diffusional processes.
- MD solvers start with Newton’s Law
$$\vec{F} = m\vec{a}$$
- where the force is usually provided in terms of the potential function experienced by each nuclei:
$$\vec{F_i} = -\frac{\partial V}{\partial \vec{x_i}}$$
- It is usual to rewrite Newton’s Law as
$$\vec{a_i} = \frac{\vec{F_i}}{m_i}$$
- for each particle $i$, resulting in a set of second-order ordinary differential equations that must be solved simultaneously:
$$\frac{d^2 \vec{x_i}}{dx^2} = \frac{\vec{F_i}}{m_i}$$
- A number of solution techniques have been used in MD simulations. 
- However, because realistic simulations are often quite large, efforts have been made to develop very fast solvers at the expense of some accuracy. 
- One of the most common is the **Verlet method**, which is developed by writing Taylor series expansions for the position forward and backward in time:
$$\vec{r}(t+\Delta t)=\vec{r}(t)+\vec{v}(t) \Delta t+\frac{1}{2} \vec{a}(t) \Delta t^{2}+\frac{1}{6} \vec{b}(t) \Delta t^{3}+\mathcal{O}\left(\Delta t^{4}\right)$$
$$\vec{r}(t-\Delta t)=\vec{r}(t)-\vec{v}(t) \Delta t+\frac{1}{2} \vec{a}(t) \Delta t^{2}-\frac{1}{6} \vec{b}(t) \Delta t^{3}+\mathcal{O}\left(\Delta t^{4}\right)$$
- where $a$ is the acceleration and $b$ the third derivative of position with time. Adding the two expressions, one obtains
$$
\vec{r}(t+\Delta t)=2 \vec{r}(t)-\vec{r}(t-\Delta t)+\vec{a}(t) \Delta t^{2}+\mathcal{O}\left(\Delta t^{4}\right)
$$
- the difficulty with this method is that the velocities are calculated
$$
\vec{v}(t)=\frac{\vec{r}(t+\Delta t)-\vec{r}(t-\Delta t)}{2 \Delta t}
$$
- However, this is only second-order accurate in time. A better scheme is to do the following, which is fourth-order accurate in both position and velocity:
$$r(t+\Delta t) =r(t)+v(t) \Delta t+\frac{1}{2} a(t) \Delta t^{2} $$ 
$$v(t+\Delta t / 2) =v(t)+\frac{1}{2} a(t) \Delta t $$ $$a(t+\Delta t) =\frac{F(r(t+\Delta t))}{m} $$
$$v(t+\Delta t) =v(t+\Delta t / 2)+\frac{1}{2} a(t+\Delta t) \Delta t $$
- Note how we need $9N$ memory locations to save the $3N$ positions, velocities, and accelerations, but we never need to have simultaneously stored the values at two different times for any one of these quantities. 
- An alternative method used by some programs is the **leapfrog Verlet**, which uses a time-splitting approach:
$$
v(t+\Delta t / 2) =v(t-\Delta t / 2)+a(t) \Delta t $$
$$
v(t) =\frac{1}{2}\left(v\left(t+\frac{1}{2} \Delta t\right)+v\left(t-\frac{1}{2} \Delta t\right)\right) $$
$$r(t+\Delta t) =r(t)+v(t)\left(t+\frac{1}{2} \Delta t\right) \Delta t$$
- One can, of course, use more accurate solvers at the expense of greater computational resource requirements. Examples include **Beeman’s method**, **Runge–Kutta**, and **Gera’s method**.
- To carry out the simulation requires knowledge of the potential energy function. Equation below is in the so-called **Amber form**:
$$
\begin{aligned}
V=& \sum_{\text {Bonds}} K_{r}\left(r-r_{e q}\right)^{2}+\sum_{\text {Angles}} K_{\theta}\left(\theta-\theta_{e q}\right)^{2}+\sum_{\text {Dihedrals}} V_{n}(1+\cos (n \phi-\gamma)) \\
&+\sum_{i=1}^{N-1} \sum_{j>i}^{N}\left[\frac{A_{i j}}{R_{i j}^{12}}-\frac{B_{i j}}{R_{i j}^{6}}+\frac{q_{i} q_{j}}{r_{i j}}\right]
\end{aligned}
$$
- The first term is harmonic bond stretching, the second three-atom bond bending, and the third four-atom torsion. 
- The final term includes non-bonded Lennard–Jones attraction and repulsion and electrostatic interaction. 
- $A_{ij} \text{ and } B_{ij}$ are written in terms of the well depth and size parameter $\epsilon$ and $\sigma$:
$$
\begin{aligned}
A_{i j} &=4 \varepsilon_{i j} \sigma_{i j}^{12} \\
B_{i j} &=4 \varepsilon_{i j} \sigma_{i j}^{6}
\end{aligned}
$$
- The Lennard–Jones parameters are obtained from the Lorentz–Berthelot mixing rule:
$$
\begin{aligned}
\varepsilon_{i j} &=\sqrt{\varepsilon_{i} \varepsilon_{j}} \\
\sigma_{i j} &=\left(\sigma_{i i}+\sigma_{j j}\right) / 2
\end{aligned}
$$
# Determining $g(r)$ from Molecular Dynamics Simulations
- $g(r)$ can be determined experimentally. However, it is quite easy to obtain from molecular dynamics. For a particular type of atom at a particular time,
$$
g(r)=\frac{\langle N(r, \Delta r)\rangle}{\frac{N}{2} \rho V(r, \Delta r)}
$$
- where the numerator is the average over all such atoms. $N(r,\Delta r)$ is the number of atoms found in a spherical shell between $r$ and $r + \Delta r$, $V(t,\Delta r)$ is the volume of the spherical shell, $N$ the total number of atoms sampled, and $\rho$ the total density (number per unit volume) within the sampled volume. 
- If the simulation is run for $M$ time steps, then the time average is
$$
g(r)=\frac{\sum_{k=1}^{M}\langle N(r, \Delta r)\rangle}{M \frac{N}{2} \rho V(r, \Delta r)}
$$
# Molecular Dynamics Software
- You will have to wait till we over DFT so that we can do MD in **Quantum-Espresso**
