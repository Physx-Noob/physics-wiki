---
title: Day 13: Dense Gases
description: 
published: true
date: 2020-10-23T02:36:28.526Z
tags: 
editor: markdown
---

# Dense Gases
- So far we have explored the situation where the density is low enough that we can treat the particles (atoms/molecules) as non-interacting. 
- Let us lift the approximation, things get a bit more complicated and inter-atomic/molecular forces must be taken into account. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/30/Annotation-2020-08-30-094624.png)
- Recall the character of the inter-atomic potential function as illustrated here. It is typically the case that as two atoms (or molecules) are brought closer together, they first experience an attractive force. This is called the van der Waals force.
- However, if the positively charged nuclei are brought too closely together, a very strong force of repulsion develops. 
- The presence of these forces will have a significant effect on the system energy, which can be expressed as
$$
U_{j}=\sum_{i=1}^{N}\left(\epsilon_{i}\right)_{i n t}+\sum_{i=1}^{N} \frac{\left|p_{i}\right|^{2}}{2 m}+\phi\left(\vec{r}_{1}, \vec{r}_{2}, \ldots\right)
$$
where the first term is the internal energy, the second is the translational energy and the third is the energy associated with intermolecular forces. 
- The (canonical) partition function then becomes
$$
Q=\sum_{j} e^{-\beta U_{j}}=\sum_{j} e^{-\beta U_{j}^{i n t}} \cdot \sum_{j} e^{-\beta\left(U_{j}^{trans}+\phi_{j}\right)}
$$
where we have factored out the internal energy term. Since
$$
\begin{aligned}
U_{j}^{i n t} &=\sum_{i=1}^{N} \epsilon_{i}^{i n t} \\
\sum_{j} e^{-\beta U_{j}^{i n t}} &=\prod_{i=1}^{N} \sum_{k} e^{-\beta \epsilon_{k}^{i n t}}
\end{aligned}
$$
Note that the sum is the internal energy partition function. Therefore,
$$
\sum_{j} e^{-\beta U_{j}^{i n t}}=q_{i n t}^{N} $$
$$Q=q_{i n t}^{N} \cdot \sum_{j} e^{-\beta\left(U_{j}^{t r a n s}+\phi_{j}\right)}
$$
Because translation states are so closely spaced, one can replace the sum with an integral:
$$
\sum_{j} e^{-\beta\left(U_{j}^{\text {trans}}+\phi_{j}\right)}=\frac{1}{N ! h^{3 N}} \int \cdots \int e^{-\beta H} d \vec{p}_{1} d \vec{p}_{2} \ldots d \vec{p}_{N} d \vec{r}_{1} d \vec{r}_{2} \ldots d \vec{r}_{N}
$$
where $H$ is the classical Hamiltonian
$$
H=\frac{1}{2 m} \sum_{n=1}^{N}\left(p_{x n}^{2}+p_{y n}^{2}+p_{z n}^{2}\right)+\phi\left(\vec{r}_{1}, \vec{r}_{2} \ldots \vec{r}_{N}\right)
$$
The integral over momentum is just the translational energy
$$
\left\langle\varepsilon_{t r}\right\rangle=\left(\frac{2 \pi m k T}{h^{2}}\right)^{\frac{3}{2} N}
$$
while the integral over space is
$$
Z_{\phi}=\int \cdots \int e^{-\phi / k T} d r_{1} d r_{2} \ldots d r_{N}
$$
- We call this the “**configuration integral**” because it depends on the configuration (i.e. the location of all the atoms and molecules). The canonical partition function then becomes
$$
Q=q_{i n t}^{N} \frac{1}{N !}\left(\frac{2 \pi m k T}{h^{2}}\right)^{\frac{3}{2} N} Z_{\phi}
$$
- Finally, evaluating the **canonical Massieu function**, we obtain the fundamental relation
$$
\frac{S[1 / T]}{k}=-\frac{F}{k T}=-\ln Q=N\left[\ln q_{i n t}-(\ln N-1)+\frac{3}{2} \ln \left(\frac{2 \pi m k T}{h^{2}}\right)\right]+\ln Z_{\phi}
$$
# Evaluating the Configuration Integral
- Evaluating the configuration integral analytically requires some simplifying assumptions.
- We start with these two:
  + The orientation of molecules is unimportant, so that the force between any two molecules is a function of distance only. (This is not true for highly nonsymmetric molecules.)
  + The potential energy is the sum of the pairwise potential energies between molecules. (This only strictly applies to a gas that is not too dense.)
- The first assumption greatly simplifies the calculation of intermolecular forces. Essentially we treat molecules as spherically symmetric points and the intermolecular potentials depend only on the distance between the points. 
- The second assumption simplifies calculating the force on a given molecule by all other molecules. Thus we can write
$$
\phi\left(\vec{r}_{1}, \vec{r}_{2} \ldots\right)=\frac{1}{2} \sum_{i \neq j} \phi_{i j}\left(r_{ij} \right)=\sum_{1 \leq i<j \leq N} \phi_{i j}\left(r_{ij} \right) \text{ with } r_{ij} = | \vec{r_i} - \vec{r_j} |
$$
- We can simplify by introducing the function $f_{ij}(r_{ij}) = e^{-\phi_{ij}(r_{ij})} -1$ in which case we can write
$$
e^{-\phi / k T}=\prod_{1 \leq i<j \leq N} e^{-\phi_{i j}\left(r_{i j}\right) / k T}=\prod_{1 \leq i<j \leq N}\left(1+f_{i j}\right)
$$
- Next we assume that the gas is only weakly interacting. If that is the case, then $f_{ij}$ must be much less than one. (Alternatively put, we will explore the result when $f_{ij} << 1$.) 
- This allows us to drop the higher-order terms in the expansion of above equation, in which case
$$
e^{-\phi / k T} \simeq 1+\sum_{1 \leq i<j \leq N} f_{i j}
$$
and the configuration integral becomes
$$
Z_{\phi}=\int \cdots \int\left(1+\sum_{1 \leq i<j \leq N} f_{i j}\right) d r_{1} d r_{2} \ldots d r_{N}
$$
noting that $\int_{- \infty}^{+\infty} dr = V$, we have 
$$
Z_{\phi}=V^{N}+\int \cdots \int \sum_{1 \leq i<j \leq N} f_{i j} d r_{1} d r_{2} \ldots d r_{N}
$$
However, since $f_{ij}$ depends only on $r_{ij}$,
$$
Z_{\phi}=V^{N}+V^{N+1} 2 \pi N^{2} \int_{-\infty}^{\infty} f(r) d r
$$
where we have assumed that all the $f_{ij}$ are the same function. Finally, it is conventional to write $Z_{\phi}$ in the form
$$
Z_{\phi}=V^{N}\left[1-\frac{N^{2} B(T)}{V}\right]
$$
where $B(T)$ is called the **second virial coefficient** $B(T) = -2 \pi \int_{- \infty}^{+\infty} f(r)dr$
- If we were to drop the weakly interacting assumption and start admitting higher-order terms, then we could more generally write
$$
Z_{\phi}=V^{N}\left[1-\frac{N^{2} B(T)}{V}+\text { higher-order terms }\right]
$$
# The Virial Equation of State
- Once we know the configuration integral it turns out that we can derive an equation of state for pressure, called the virial equation of state. In the canonical representation:
$$
d S[1 / T]=-U d(1 / T)+\frac{p}{T} d V-\frac{\mu}{T} d N
$$
Recalling that $\frac{p}{T}=k \ln Q$ & $S[1 / T]=k \ln Q$, we have
$$
\left.p=k T \frac{\partial \ln Q}{\partial V}\right)_{1 / T, N}
$$
The only term in $\ln Q$ that contains $V$ is $\ln Z_{\phi}$, so
$$
\left.p=k T \frac{\partial \ln Z_{\phi}}{\partial V}\right)_{1 / T, N}
$$
Now, $\ln Z_{\phi}$ is in the form of $\ln (1 + x)$ where $x$ is small, and $\ln (1 + x) = x - \frac{x^2}{2} + \dots$ Using this fact we can write $p$ as
$$p=\frac{N k T}{V}+\frac{N^{2} k T B(T)}{V^{2}}+\cdots$$
$$p=\frac{k T}{v}+\frac{k T B(T)}{v^{2}}+\cdots \text{ with } v = \frac{V}{N}$$
In molar units, $R = N_Ak$ where $N_A$ is Avogadro’s number. Thus,
$$
p=\frac{R T}{v}+\frac{R T N_{A} B(T)}{v^{2}}+\cdots \text{ with } v = \frac{VN_A}{N}
$$
This equation is more commonly expressed in the following form:
$$
p=\frac{R T}{v}+\frac{a(T)}{v^{2}}+\frac{b(T)}{v^{3}}+\cdots
$$
with the coefficients determined empirically. Most other real gas equations of state are similarly expansions about the ideal gas limit. Examples are the **van derWaals**, **Beattie–Bridgeman**, **Redlich–Kwong**, and **Benedict–Webb–Rubin** equations.
# Other Properties
Since we have an expression for the partition function in terms of the configuration integral, we can calculate the other thermodynamic properties. Recall that
$$
d S[1 / T]=-U d(1 / T)+\frac{p}{T} d V-\frac{\mu}{T} d N
$$
Therefore,
$$
\left.U=-\frac{\partial S[1 / T]}{\partial[1 / T]}\right)_{V, N}
$$
and the energy becomes
$$
U=\frac{3}{2} N k T+k T^{2}\left(\frac{\partial \ln Z_{\phi}}{\partial T}\right)_{N V}=\frac{3}{2} N k T+\bar{U}
$$
where
$$
\bar{U}=\frac{\int \cdots \int \phi e^{-\phi / k T} d r_{1} d r_{2} \ldots d r_{N}}{Z_{\phi}}
$$
can be considered as the configuration energy.
# Potential Energy Functions
- To evaluate the configuration integral using the above equation, for example, requires knowing the function $\phi (r)$, which is known as the potential energy function. 
- In general, the potential energy function is a somewhat complex function of distance between the two particles, even for collisions between atoms that are spherically symmetric. 
- However, is the fact that this function only appears in an integral, which is somewhat insensitive to the exact shape of the potential. As a result, there have been many algebraic forms proposed for use.
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/22/Annotation-2020-10-22-175045.png)
- The simplest form is that for a rigid sphere , where $\sigma$ is the line-of-center distance at which two particles are touching. 
- Also called the **billiard ball model**, it assumes no forces between the particles until they hit a solid surface.
- Also shown in this figure are the weakly attracting, square well, and **Lennard–Jones potentials**.

- The rigid sphere model has one parameter, $\sigma$. 
- While it obviously has the wrong shape, by comparing with experimental $pvT$ data, a value for $\sigma$ can be obtained by regression.
- In some cases, and for not too broad a range of conditions, the resulting equation of state can work reasonably well. 
- However, the ability to fit data over a wider range of conditions requires a potential energy function that more closely approximates reality.
- Take the weakly attracting sphere or **Sutherland potential**, for example, which is a three parameter function, $\sigma$, $\epsilon$, and $\gamma$ ($\gamma$ is typically $\gamma > 3$):
$$
\phi(r)=\left\{\begin{array}{ll}
\infty & r \leq \sigma \\
-\epsilon\left(\frac{\sigma}{r}\right)^{\gamma} & \sigma<r
\end{array}\right.
$$
- One can estimate the parameters $a$ and $b$ by setting $(\partial P / \partial v)_{T_{c}}=\left(\partial^{2} P / \partial v^{2}\right)_{T_{c}}=0$. So,
$$ a =\frac{9 R T_{c} v_{v}}{8} \text{ and } b =\frac{v_{c}}{3}$$
- We know that while the van der Waals equation is very useful for illustrating the role of attractive and repulsive forces, it is not very accurate. 
- An even better form of the potential energy function that mimics the shape of many real potential functions is the **Lennard–Jones** potential, also known as the **6–12 potential**:
$$
\phi(r)=4 \epsilon_{i j}\left[\left(\frac{\sigma_{i j}}{r}\right)^{12}-\left(\frac{\sigma_{i j}}{r}\right)^{6}\right]
$$
- Here, $\sigma_{ij}$ is the interatomic distance at which the attractive and repulsive forces exactly balance and is the well depth where $\phi$ is a minimum. Lennard–Jones is commonly used, especially for calculating transport properties. 
- However, it, and other more realistic potential functions, do not result in an algebraic form for $B(T)$, rather the integral expression
$$
B(T)=2 \pi \int_{0}^{\infty}\left[1-\exp \left\{-\frac{4 \epsilon}{k T}\left[\left(\frac{\sigma}{r}\right)^{12}-\left(\frac{\sigma}{r}\right)^{6}\right]\right\}\right] r^{2} d r
$$
# Other Equations of State
- We have explored the underlying physics of non-ideal gas behavior using relatively simple approximations. 
- These include pairwise potential functions and simple analytic forms, and have allowed derivation of van der Waals equation. 
- Unfortunately, van der Waals equation, while very useful for illustrating the important physics of $pvT$ behavior, is not very accurate for real substances. 
- Furthermore, even today when very powerful quantum mechanics software is available, the difficulties imposed by the three-dimensional structures of most interesting substances means that empirically based
methods have historically been used to provide more accurate equations of state, including ones that extend into liquid and supercritical regions. 
- Here we present three wellknown such equations.
- The **Redlich–Kwong equation** was published in 1949. It is a two-parameter equation of state, and does well at small to moderate densities and when $T > T_c$:
$$
P=\frac{R T}{v-b}-\frac{a}{T^{1 / 2} v(v+b)}
$$
- Values of the parameters a and b can be found in many thermodynamics textbooks. 
- In the absence of experimental data, one can estimate the parameters using critical data.
- As illustrated for van der Waals equation, setting $(\partial P / \partial v)_{T_{c}}=\left(\partial^{2} P / \partial v^{2}\right)_{T_{c}}=0$
- Another two-parameter equation of state is **Peng–Robinson**, developed for vapor–liquid equilibrium calculations
$$
P=\frac{R T}{v-b}-\frac{a \alpha}{v(v+b)+b(v-b)}
$$
- The **Benedict–Webb–Rubin equation** of state is a more complex virial expansion-type equation. It contain eight constants
$$
P=\frac{R T}{v}+\frac{B_{0} R T-A_{0}-C_{0} / T^{2}}{v^{2}}+\frac{b R T-a}{v^{3}}+\frac{a \alpha}{v^{6}}+\frac{c}{v^{3} T^{2}}\left(1+\frac{\gamma}{v^{2}}\right) \exp \left(\frac{-\gamma}{v^{2}}\right)
$$
- In practice, engineers are most likely to turn to digital compilations to obtain property data for real substances.