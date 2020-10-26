---
title: Day 15: Crystalline Solids
description: 
published: true
date: 2020-10-26T02:01:23.961Z
tags: 
editor: markdown
---

# Crystalline Solids
- Solids are materials in which inter-molecular forces hold the atoms and molecules relatively rigidly in place. 
- They generally fall into two classes, crystalline and amorphous. 
- Crystalline solids have a regular, ordered rigid structure. They have precise melting and boiling points. Examples are most metals, diamond, sugar, and graphite. 
- Amorphous solids don’t have a regular geometric shape. Their structure varies randomly in three-dimensional
space and they melt over a range of temperatures.
- Examples are coal, plastic, and rubber. The thermodynamic treatment of these two forms is very different. 
- As a result, amorphous solids are typically treated as a separate subject which is beyond the scope of this course.
- On the other hand, crystalline solids are relatively easy to treat, as we shall see below. 
- If the solid has a crystalline structure then the concept of normal modes of vibration can be used to treat the crystal as a set of independent particles. 
- One can show that the thermodynamic properties are a function of the vibrational spectrum of the crystal. 
- We start by exploring the nature of the vibrational spectrum and two theories, Einstein and Debye, that make simple assumptions about the spectra.
- A crystal can, in many cases, be represented as a set of atoms connected by springs, as shown in two dimensions in figure below. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-172144.png)
- The springs represent the inter-atomic forces holding the atoms in place. Each atom is located in a potential well, as shown in figure below. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-17215.png)
- If the atomic displacement is small, the force can be represented as harmonic, that is $\vec{F} = -k\vec{x}$, where $\vec{x}$ is the atomic displacement and $k$ a spring constant. Thus, $V(x) = k(x-x_0)^2$.
- The development to obtain the partition function is similar to that for a dense gas. However, there are no modes of motion other than vibration. The total energy can be written as
$$U = U_0 + \phi(\vec{r_1}, \vec{r_2}, \dots)$$
- where $U_0$ represents the zero-point energy for the crystal as a whole. The natural frequency of a harmonic oscillator is
$$v_j = \frac{1}{2\pi}\sqrt{\left ( \frac{k_j}{\mu_j}\right ) }$$
- where $k_j$ and $\mu_j$ are an effective force constant and an effective reduced mass. Their values will depend on the details of the crystal structure and there will be a distribution of frequencies based on the normal modes.
- If we assume that the normal modes of motion are independent of each other, then the molecular partition function for vibration is the product of the individual normal mode partition functions:
$$
q_{v i b}=\prod_{j=1}^{3 N-6} q_{v i b, j}
$$
- Taking the zero-point energy into account, the canonical partition function becomes
$$
Q=e^{-\frac{U_{0}}{k T}} \prod_{j=1}^{3 N-6} q_{v i b, j}
$$
- We have derived the molecular partition function for a harmonic oscillator in our examination of ideal gases:
$$
q_{v i b}=\frac{e^{-h v / 2 k T}}{1-e^{-h v / k T}}
$$
- Thus, the total partition function becomes
$$
Q=e^{-\frac{U_{0}}{k T}} \prod_{j=1}^{3 N-6}\left(\frac{e^{-h v_{j} / 2 k T}}{1-e^{-h v_{j} / k T}}\right)
$$
- Taking the negative logarithm of $Q$ (remember that $S[1/T] = −k \ln Q$), we have
$$
-\ln Q=\frac{U_{0}}{k T}+\sum_{j=1}^{3 N} \frac{e^{-h v_{j} / 2 k T}}{1-e^{-h v_{j} / k T}}=\frac{U_{0}}{k T}+\sum_{j=1}^{3 N}\left[\ln \left(1-e^{-h v_{j} / k T}\right)+\frac{h v_{j}}{2 k T}\right]
$$
- In a macroscopic crystal, the normal-mode frequencies are essentially continuously distributed. If we introduce a distribution function $g(\nu )$, and convert the sum to an integral, we get
$$
-\ln Q=\frac{U_{0}}{k T}+\int_{0}^{\infty}\left[\ln \left(1-e^{-h v / k T}\right)+\frac{h v}{2 k T}\right] g(v) d v
$$
- Here, $g(\nu )$ is normalized to the total number of normal-mode frequencies
$$\int_0^{\infty}g(\nu ) d\nu = 3N$$
- We can now calculate the thermodynamic properties. The Helmholtz function is just
$$
F[1 / T]=-\ln Q=\frac{U_{0}}{k T}+\int_{0}^{\infty}\left[\ln \left(1-e^{-h v / k T}\right)+\frac{h v}{2 k T}\right] g(v) d v
$$
- Then the internal energy is
$$
U=U_{0}+\int_{0}^{\infty}\left[\frac{h v e^{-h v / k T}}{1-e^{-h v / k T}}+\frac{h v}{2}\right] g(v) d v
$$
- and the specific heat becomes
$$
c_{v}=k \int_{0}^{\infty}\left[\frac{(h v / k T)^{2} e^{-h v / k T}}{\left(1-e^{-h v / k T}\right)^{2}}\right] g(v) d v
$$
- It remains to determine $g(\nu )$ .
# Einstein Crystal
- Einstein made the very simple assumption that there was only a single normal-mode frequency. If we define the characteristic Einstein temperature as
$$
\Theta_{E} \equiv \frac{h v_{v i b}}{k}
$$
- then the Helmholtz function, the energy, and the specific heat become
$$
\frac{F}{k T}=-\left\{\frac{N U_{0}}{2 k T}+3 N \ln \left(2 \sinh \frac{\theta_{E}}{2 T}\right)\right\}
$$
$$U=\frac{N U_{0}}{2}+\frac{3}{2} N k \theta_{E} \coth \frac{\theta_{E}}{2 T}$$
$$C_{v}=3 N k\left[\frac{\theta_{E} / 2 T}{\sinh \left(\theta_{E} / 2 T\right)}\right]^{2}$$
- The entropy is
$$S=3 N k\left[\frac{\theta_{E}}{2 T} \operatorname{coth} \frac{\theta_{E}}{2 T}-\ln \left(2 \sinh \frac{\theta_{E}}{2 T}\right)\right]$$
- The specific entropy, energy, and specific heat are plotted in below figure as a function of $T/\theta_E$
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-175440.png)
- The limiting values of $C_{\nu}$ are
$$T \rightarrow 0, \quad \frac{C_{v}}{N k} \rightarrow 3\left(\frac{\theta_{E} / T}{e^{\theta_{E} / 2 T}}\right)^{2}$$
$$T \rightarrow \infty, \quad \frac{C_{v}}{N k} \rightarrow 3$$
# Debye Crystal
- The Einstein solid works pretty well, except that inter-particle interactions are ignored.
- Every oscillator is the same. In fact, at significant temperatures, a solid acts more like a multi-body system with $3N−6$ degrees of freedom. 
- Debye assumed that he could determine the distribution using elastic wave analysis and ignoring quantum effects.
- The wave analysis results in a wave velocity distribution that is essentially the same as the translational energy distribution from the particle in a box problem. 
- The bottom line is that
$$
g(\nu) d \nu=\left(\frac{2}{v_{t}^{3}}+\frac{1}{v_{l}^{3}}\right) 4 \pi V \nu^{2} d \nu
$$
- where $v_t$ and $v_l$ are the transverse and longitudinal wave speeds in the solid. Defining an effective wave speed as
$$\frac{3}{\mathrm{v}_{0}^{3}}=\frac{2}{\mathrm{v}_{t}^{3}}+\frac{1}{\mathrm{v}_{l}^{3}}$$
- $g(\nu)$ becomes
$$g(\nu) d \nu=\frac{12 \pi V}{\mathrm{v}_{0}^{3}} \nu^{2} d \nu$$
- Because of the normalization of $g(\nu)$, there is a maximum allowed frequency. This is
$$
\nu_{m}=\left(\frac{3 N}{4 \pi V}\right)^{1 / 3} \mathrm{v}_{0}
$$
- so
$$g(\nu) d \nu=\left(\frac{9 N}{\nu_{m}^{3}}\right) \nu^{2} d \nu, \quad 0 \leq \nu \leq \nu_{m}$$
$$g(\nu) d \nu=0, \quad \nu>\nu_{m}$$
- $\nu_m$ is called the “cutoff” frequency.
- The difference between the Einstein and Debye frequency distributions is illustrated in figure below. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-180618.png)
- In effect, Einstein assumed that $g(\nu)$ was a single-frequency delta function. Plugging all this into the fundamental relation, we obtain
$$
\frac{F}{k T}=-N\left\{\frac{U_{0}}{2 k T}+\frac{9}{8} \frac{\theta_{D}}{T}+3 \ln \left(1-e^{-\theta_{D} / T}\right)-3\left(\frac{T}{\theta_{D}}\right)^{3} \int_{0}^{\theta_{D} / T} \frac{x^{3} d x}{e^{x}-1}\right\}
$$
- where $\theta_D \equiv \frac{h\nu_m}{k}$ is called the Debye temperature. Then
$$\frac{U}{k T}=-N\left\{\frac{U_{0}}{2 k T}+\frac{9}{8} \frac{\theta_{D}}{T}+9\left(\frac{T}{\theta_{D}}\right)^{3} \int_{0}^{\theta_{D} / T} \frac{x^{3} d x}{e^{x}-1}\right\}$$
$$\frac{S}{k}=9 N\left(\frac{T}{\theta_{D}}\right)^{3} \int_{0}^{\theta_{D} / T}\left[\frac{x^{3}}{e^{x}-1}-x^{2} \ln \left(1-e^{-x}\right)\right] d x$$
$$\frac{C_{\nu}}{k}=3 N D\left(\frac{T}{\theta_{D}}\right)$$
- where the “**Debye function**” is defined as
$$
D\left(\frac{T}{\theta_{D}}\right) \equiv 3\left(\frac{T}{\theta_{D}}\right)^{3} \int_{0}^{\theta_{D} / T} \frac{x^{4} e^{x}}{\left(e^{x}-1\right)^{2}} d x
$$
- The limiting values of $C_{\nu}$ for the Debye crystal are
$$T \rightarrow 0, \quad \frac{C_{\nu}}{N k} \rightarrow \frac{12 \pi^{4}}{5}\left(\frac{T}{\theta_{D}}\right)^{2}$$
$$T \rightarrow \infty, \quad \frac{C_{\nu}}{N k} \rightarrow 3$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/10/25/Annotation-2020-10-25-181743.png)
- The specific heat for both the Einstein and Debye models is shown in the above figure, along with data for crystalline silver. 
- Although both models predict the same value at high temperatures, at lower temperatures the Debye model provides a better fit.
- Both the Einstein and Debye temperatures can be inferred from specific heat data or from elastic constants. 
- The Debye temperature tends to decrease with increasing atomic mass. This is because the frequency of a harmonic oscillator is proportional to $\sqrt{k/m}$.
- Typical values of $\theta_D$ are fairly low, usually of the order of room temperature or less. 
- This is due to the relatively low force constants and large atomic masses in monatomic crystals. 
$$
\begin{array}{lllr}
\hline \text { Solid } & \theta_{D}(\mathrm{K}) & \text { Solid } & \theta_{D}(\mathrm{K}) \\
\hline \mathrm{Na} & 150 & \mathrm{Fe} & 420 \\
\mathrm{K} & 100 & \mathrm{Co} & 385 \\
\mathrm{Cu} & 315 & \mathrm{Ni} & 375 \\
\mathrm{Ag} & 215 & \mathrm{Al} & 390 \\
\mathrm{Au} & 170 & \mathrm{Ge} & 290 \\
\mathrm{Be} & 1000 & \mathrm{Sn} & 260 \\
\mathrm{Mg} & 290 & \mathrm{Pb} & 88 \\
\mathrm{Zn} & 250 & \mathrm{Pt} & 225 \\
\mathrm{Cd} & 172 & \mathrm{C} \text { (diamond) } & 1860 \\
\hline
\end{array}
$$
- In general, Debye theory fits fairly well for monatomic crystal solids. It does not work for non-crystal solids, the above table lists Debye temperatures for a number of materials.