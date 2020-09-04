---
title: Day 05: Microscopic Thermodynamics
description: 
published: true
date: 2020-09-04T08:20:19.305Z
tags: 
editor: markdown
---

# Microscopic Thermodynamics
## Systems with Negligible Inter-Particle Forces
- If a system is composed of particles that are indistinguishable from one another, and do not, for the vast majority of time, interact with one another, then for all practical purposes the mechanical properties of the system are those of each particle, summed over all the particles.
> ### Some Definitions to Remember:
> - $U_j$ = energy of ensemble member in quantum state $j$
> - $N_j$ = number of particles in ensemble member in quantum state $j$
> - $U_{ij}$ = energy associated with type-$i$ particle of member in quantum state $j$
> - $N_{ij}$ = number of $i$-type particles in member in quantum state $j$
> - $\epsilon_{ik}$ = energy of $i$-type particle in particle quantum state $k$
> - $N_{ikj}$ = number of $i$-type particles in particle quantum state $k$ in member in quantum state $j$
> - $i$ = particle type index
> - $j$ = member quantum state number
> - $k$ = particle quantum state number
- Using quantum mechanics, we can obtain $N_{ij}$ and $\epsilon_{ij}$ so that we are now in a position to start calculating the mechanical properties and the partition function. 
- In the grand canonical representation, we are concerned with the ensemble member energy and particle numbers, which become
$$U_{j}=\sum_{i} U_{i j}=\sum_{i} \sum_{k} \epsilon_{i k} N_{i k j}$$
$$N_{j}=\sum_{i} N_{i j}=\sum_{i} \sum_{k} N_{i k j}$$
- The partition function then becomes
$$\begin{aligned}
Q &=\sum_{j} \exp \left(-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}\right) \\
&=\sum_{j} \exp \left(-\sum_{i} \sum_{k}\left(\beta \epsilon_{i k}+\gamma_{i}\right) N_{i k j}\right) \\
&=\sum_{j} \prod_{i} \prod_{k} \exp \left(-\left(\beta \epsilon_{i k}+\gamma_{i}\right) N_{i k j}\right)
\end{aligned}$$
- The above one after simplification, we get
$$Q=\prod_{i} \prod_{k} \sum_{\eta=0}^{\operatorname{Max} N_{i k j}} e^{-\left(\beta \epsilon_{i k}+\gamma_{i}\right) \eta}$$
- where Max $N_{ikj}$ is the maximum number of $i$-type particles which may simultaneously occupy the $k$th particle quantum state. 
- The advantage of this form for the partition function is that the sum is for a single quantum state of a single-type particle.
- To proceed further, we must take note of a physical phenomenon that can have a profound impact on the final form of the partition function.
$$\begin{array}{lllll}
\hline \text { Symmetry } & \text { Max } N_{i k j} & \text { Particle name } & \text { System name } & \text { Examples } \\
\hline \begin{array}{l}
\text { Anti-symmetric } \\
\text { Symmetric }
\end{array} & \begin{array}{l}
\text { 1 } \\
\text { $\infty$ }
\end{array} & \begin{array}{l}
\text { fermion } \\
\text { boson }
\end{array} & \begin{array}{l}
\text { Fermi-Dirac}\\
\text { Bose-Einstein}
\end{array}& \begin{array}{l}
\text { $D$, $He^3$, $e$}\\
\text { $H$, $He^4$, photons}
\end{array} \\
\hline
\end{array}$$
- One may show that the partition function for the Fermi–Dirac and Bose–Einstein cases becomes:
$$\begin{aligned}
Q_{F D, B E} &=\prod_{i} \prod_{k}\left(1 \pm e^{-\beta \epsilon_{i k}-\gamma_{i}}\right)^{\pm 1} \\
\ln Q_{F D, B E} &=\sum_{i} \sum_{k} \ln \left(1 \pm e^{-\beta \epsilon_{i k}-\gamma_{i}}\right)^{\pm 1}
\end{aligned}$$
- We can now evaluate $N_i$, since
$$\langle N_i \rangle = -\frac{\partial \ln Q}{\partial \gamma_i}_{\beta, V, \gamma_{k \neq i}}$$
- So, we have with us
$$\begin{aligned}
\left\langle N_{i}\right\rangle_{F D, B E}=& \sum_{k} \frac{1}{e^{+\beta \epsilon_{i k}+\gamma_{i}} \pm 1} \\
\left\langle N_{i, k}\right\rangle_{F D, B E} &=\frac{1}{e^{+\beta \epsilon_{i k}+\gamma_{i}} \pm 1}
\end{aligned}$$
- **Maxwell-Boltzmann Statistics** springs up for a limit $e^{+\beta \epsilon_{i k}+\gamma_{i}}>>1$.
$$\ln Q_{M B}=\sum_{i} \sum_{k} e^{-\beta \epsilon_{i k}-\gamma_{i}}$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/28/statrs.png)
$$\begin{array}{c}
\left\langle N_{i}\right\rangle_{M B}=\sum_{k} e^{-\beta \epsilon_{i k}-\gamma_{i}} \\
\langle N\rangle_{M B}=\sum_{i}<N_{i}>=\ln Q_{M B}
\end{array}$$
- The Maxwell–Boltzmann limit is important because it leads to the ideal gas law. Recall that since
$$k \ln Q = \frac{PV}{T}$$
we must have
$$PV = NkT$$
- This is actually the proof that $\beta = \frac{1}{k_B T}$.
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/28/Annotation-2020-08-28-190707.png)
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/28/Annotation-2020-08-28-190802.png)

## Systems with Non-negligible Inter-Particle Forces
- If inter-particle forces become important, then a complete specification of the quantum state includes specifying the positions, or configuration, of particles. 
- The dilemma we face when forced to consider configuration is that there is no longer a simple way to calculate the partition function.
- For simplicity, consider the canonical partition function
$$Q = \sum_j e^{- \beta U_j}$$
- For a system in which particle interactions are important, the energy of the member in quantum state $j$ becomes
$$U_j = \sum_i \sum_k \epsilon_{ik} N_{ikj} + \phi ( \vec{r_1}, \vec{r_2}, \vec{r_3}, \cdots , \vec{r_n} )$$
- where $\phi$ is the energy associated with interactions between particles
$$Q = \sum \exp -\beta \left \{  \sum_i \sum_k \epsilon_{ik} N_{ikj} + \phi ( \vec{r_1}, \vec{r_2}, \vec{r_3}, \cdots , \vec{r_n} )\right \}$$
- This can be written as
$$Q = \frac{q_{\text{int}} q_{\text{tr}}}{N !} Z_N$$
where 
$$Z_N = \int \cdots \int e^{-\phi/k_B T} d\vec{r_1} d\vec{r_2} d\vec{r_3} \cdots d\vec{r_n}$$
- is called the configuration integral.
- We will have to evaluate $Z_N$ to calculate the partition function.