---
title: Day 12: Photon and Electron Gases
description: 
published: true
date: 2020-09-07T11:34:35.715Z
tags: 
editor: markdown
---

# Photon and Electron Gas
- It is an interesting fact that both equilibrium radiation fields and electrons in metals can be treated as non-interacting ideal gases.
- Let us see how they came to be and how we can use the results derived so far.
## The Photon Gas
- We have discussed the idea that electromagnetic radiation can, under certain circumstances, be thought of as being composed of photons, or quanta, that display particlelike characteristics. 
- It would be useful if we could treat an electromagnetic field in an enclosure as a collection of monatomic particles and predict its equilibrium behavior using the principles of statistical mechanics. 
- This is because many bodies emit radiation with a spectral distribution similar to that of an equilibrium field. 
- A body that does so is said to be a “black body” and the radiation from the surface is completely characterized by the temperature. 
- Indeed, in carrying out radiation heat transfer calculations, one usually expresses the properties of surfaces in terms of how closely they resemble a black body.
- We can treat a collection of photons contained in an enclosure as an ideal monatomic gas except for two restrictions:
  + Photons are bosons and Bose–Einstein statistics must be used. However, photons do not interact with each other, so no approximation is made by neglecting interparticle forces.
  + Photons can be absorbed and emitted by the walls of the container, so that no constraint can be placed on the number of photons even in the grand canonical representation.
- Recall that for a dilute assembly of bosons, the distribution of particles over the allowed energy states is
$$N_{k}=\frac{g_{k}}{e^{\gamma+\varepsilon_{k} / k T}-1}$$
- However, this expression was derived including the constraint on $N$ that is now removed and $\gamma = - \mu/k_B T = 0$. Thus,
$$N_{k}=\frac{g_{k}}{e^{\varepsilon_{k} / k T}-1}$$
- If we assume that the differences between energy levels are so small that energy varies continuously, we can write
$$dN=\frac{dg}{e^{\varepsilon_{k} / k T}-1}$$
- where $dg$ is the degeneracy for the energy increment $\epsilon$ to $\epsilon + d\epsilon$ . As we derived in our discussion of translational energy, the degeneracy is
$$dg = 2 \left ( \frac{4 \pi n^2 dn}{8} \right )$$
- where the factor of 2 arises because an electromagnetic field can be polarized in two independent directions.
- For a molecular gas, we related $dn$ to $d\epsilon$ using Newtonian physics, namely that
$$\epsilon = \frac{mc^2}{2} \text{ or } p^2 = 2m\epsilon$$
- However, photons are relativistic, and de Broglie’s relation (where here $c$ is the speed of light). So, $p = \frac{\epsilon}{c}$ must be used. So, we have
$$\epsilon = \frac{h^2 c^2}{4 V^{2/3}} n^2 \text{ and } dg = \frac{8 \pi V}{h^3 c^3} \epsilon^2 d\epsilon$$
- Substituting this into the expression for $dN$ and noting that $\epsilon = h\nu$
$$\frac{d N}{V}=\frac{8 \pi}{c^{3}} \frac{\nu^{2}}{\left(e^{h \nu / k T}-1\right)} d \nu$$
- This is the number of photons (per unit volume) in the frequency range $\nu$ to $\nu +d\nu$. We seek the spectral energy density $u_{\nu}$:
$$u_{\nu}d\nu = hu_{\nu} \frac{dN}{V} \text{ hence } u_{\nu} = \frac{8 \pi h \nu^3}{c^3} \frac{1}{e^{h\nu / k_B T} -1}$$
- This is Planck’s Law.
- The limits for high and low frequency can be readily obtained:
$$u_{\nu} \cong \frac{8 \pi h \nu^{3}}{c^{3}} e^{-h \nu / k_B T} \text{ and } u_{\nu} \cong \frac{8 \pi \nu^{2} k_B T}{c^{3}}$$
- which is respectively Wein's Formula and Rayleigh-Jeans Law we are familiar with.
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/07/Annotation-2020-09-07-110451.png)
- The wavelength of maximum energy or intensity is known as Wien’s displacement law. It can be obtained by taking the derivative of Planck’s Law and setting it to zero. The result is $\lambda = \frac{b}{T}$
- The total energy per unit volume is
$$u=\int_{0}^{\infty} u_{\nu} d \nu=\frac{8 \pi h}{c^{3}} \int_{0}^{\infty} \frac{\nu^{3}}{\left(e^{-h \nu / k T}-1\right)} d \nu=\frac{8 \pi^{5}}{15} \frac{(k_B T)^{4}}{(h c)^{3}}$$
- We could have obtained this relation by first evaluating the partition function, thereby obtaining the fundamental relation. Energy is then one of the equations of state in the grand canonical representation. For a boson and with $\gamma = 0$:
$$\ln Q=\sum_{k} \ln \frac{1}{\left(1-e^{-\beta \varepsilon_{k}}\right)} \cong \int_{0}^{\infty} g(v) \ln \frac{1}{\left(1-e^{-h v / k T}\right)} d v=\frac{8 \pi^{5} V}{45(h c / k T)^{3}}$$
- Therefore, the fundamental relation becomes
$$S[1 / T, 0]=\frac{8 k \pi^{5} V}{45(h c / k T)^{3}}=\frac{p V}{T}$$
- The energy we have already derived. The pressure is
$$\left.p=\frac{\partial S[1 / T]}{\partial V}\right)_{V}=\frac{8 \pi^{5}}{45(h c)^{3}}(k T)^{4}$$
- To obtain the number of photons requires differentiating with respect to $\mu$ before setting $d\mu = 0$
$$\left.N=-\frac{\partial S[1 / T,-\mu / T]}{\partial \mu / T}\right)_{1 / T, V}=\frac{\pi^{2}}{6} \frac{16 \pi V}{(h c / k T)^{3}}$$
- The entropy for the photon gas is
$$S=\frac{32 k \pi^{5} V}{45(h c / k T)^{3}}$$
- Finally, we can also derive the important Stefan–Boltzmann relation used in heat transfer. 
- For an ideal gas, the flux of particles across any given plane is $n\bar{c}/4$. 
- This relation was derived by integration of the Maxwellian velocity distribution function. 
- By analogy, we can show that the energy flux of photons (energy per unit time and area) is
$$q=\frac{2 \pi^{5} k^{4}}{15 h^{3} c^{2}} T^{4}=\sigma T^{4}$$

## The Electron Gas
- Metals are excellent conductors of heat and electricity. It is observed that electrical current in a metal involves the flow of electrons, but not ions. 
- A simple model proposed by Paul Drude in 1900 assumed that when the atoms of a metallic element are brought together to form a metal, the valence electrons become detached and are free to move within the metal lattice. 
- If we assume that the electrons do not interact with one another, then they collectively must act like a monatomic ideal gas.
- If free electrons do act like an ideal gas, each one would contribute $3/2k_B T$ to the total energy, so if $N_0$ is the number of free electrons, then $U = N_0 \frac{3}{2}k_B T$
- The specific heat per electron would then be $c_v =  \frac{3}{2}k_B$
- The number density of free electrons depends on the specific metallic atom. 
- However, for many metals, there is about one free valence electron per atom.
- The Drude model is not very accurate and a fully quantum analysis is more appropriate. 
- Electrons must satisfy the Pauli exclusion principle. 
- Therefore, they will fill the metal lattice in increasing energy order. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/07/Annotation-2020-09-07-121604.png)
- Even at absolute zero, not all the electrons will have zero energy. 
- The maximum electron energy at $0 \mathrm{K}$ is called $\mu_0$, the Fermi energy. The quantum state number distribution for a fermion is
$$N_k = \frac{1}{e^{(\epsilon_k - \mu)/k_B T}+1}$$
- and in the continuum limit the single-electron energy distribution is
$$f(\epsilon) = \frac{1}{e^{(\epsilon - \mu)/k_B T}+1}$$
![enter image description here](https://theskillcraft.com/img-host/images/2020/09/07/Annotation-2020-09-07-122723.png)
- The number of states with energy between $\epsilon$ to $\epsilon + d\epsilon$  is the degeneracy
$$d g=4 \pi V\left(\frac{2 m_{e}}{h^{2}}\right)^{3 / 2} \sqrt{\varepsilon} d \varepsilon$$
- The factor of 4 arises because electrons can each have two spin states. Thus, the equivalent expression for particles in a box must be multiplied by 2. Then
$$N(\varepsilon) d \varepsilon=\left[4 \pi V\left(\frac{2 m_{e}}{h^{2}}\right)^{3 / 2}\right] \frac{\sqrt{\varepsilon}}{\mathrm{e}^{(\varepsilon-\mu) / k T}+1} d \varepsilon$$
- Integrating the energy distribution at $0 \mathrm{K}$, the number of free electrons equals
$$N=4 \pi \frac{8 \pi}{3}\left(\frac{2 m_{e}}{h^{2}}\right)^{3 / 2} V \int_{0}^{\mu_{0}} \varepsilon^{1 / 2} d \varepsilon=4 \pi \frac{8 \pi}{3}\left(\frac{2 m_{e}}{h^{2}}\right)^{3 / 2} V\left(\mu_{0}\right)^{3 / 2}$$
- Solving for Fermi Energy, we get
$$\mu_{0}=\frac{h^{2}}{2 m_{e}}\left(\frac{3}{8 \pi}\right)^{2 / 3}\left(\frac{N}{V}\right)^{2 / 3}$$
- Values of the Fermi energy are typically in the range of $1–5 \mathrm{eV}$. We can define a Fermi temperature as $T_F = \mu_0/k_B$ and since $1 \mathrm{eV} = 11,600 \mathrm{K}$, the Fermi temperatures are typically very large. 
- As a consequence, electron gases behave as though they are at a very low temperature. The total electron energy at absolute zero is
$$U_{0}=\int_{0}^{\infty} \epsilon d N(\epsilon)=\frac{\pi}{2}\left(\frac{8 m_{e} V^{2 / 3}}{h^{2}}\right)^{3 / 2} \int_{0}^{\epsilon_{0}} \epsilon^{3 / 2} d \epsilon=\frac{3}{5} N \mu_{0}$$
- We can easily determine the fundamental relation at $0 \mathrm{K}$. It is simply the ideal gas result in the Helmholtz representation
$$F_{0}=N U(0)+\frac{3}{40} N \frac{h^{2}}{m_{e}}\left(\frac{3 N}{\pi V}\right)^{2 / 3}$$
- At higher temperature things would be simplified if the Maxwell–Boltzmann limit applied. However, for copper at its normal melting point, for example,
$$\left(\frac{2 \pi m_{e} k T}{h^{2}}\right)^{3 / 2} \frac{V}{N} \approx 1.42 \times 10^{-3}<<1$$
- Therefore, the full Fermi–Dirac treatment must be followed and a series expansion approach taken:
$$F=F_{0}\left[1-\frac{5 \pi^{2}}{12}\left(\frac{T}{T_{F}}\right)^{2}+\cdots\right] \text{ and } U=U_{0}\left[1+\frac{5 \pi^{2}}{12}\left(\frac{T}{T_{F}}\right)^{2}-\cdots\right]$$
- where $F_0$ and $U_0$ are reference values of $F$ and $U$, respectively.
- Since in all practical cases $T << T_F$, the specific heat per electron becomes
$$c_{v} \cong \frac{\pi^{2}}{2} k \frac{T}{T_{F}}$$
- This is far less than the ideal gas value of $(3/2)k_B T$.

> ### Specific Heat of Metals
> Standard Form of Specific Heat of Metals look like:
> $$c_v = \alpha T^3 + \gamma T$$