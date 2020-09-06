---
title: Day 11: Ideal Gas Mixtures
description: 
published: true
date: 2020-09-06T10:41:41.191Z
tags: 
editor: markdown
---

# Ideal Gas Mixtures
- Let's explore the properties of mixtures of ideal gases. 
- It is trivial exercise for non-reacting gas mixtures of known composition. 
- For reacting mixtures, a maximization or minimization process is required, depending on the choice of representation.
## Non-reacting Mixtures
 - Let's briefly summarize the important relations for non-reacting mixtures.
 - The prediction of the properties of ideal gas mixtures are based on **Dalton’s law of additive pressures** and **Amagat’s law of additive volumes**. 
 - Dalton’s law states that the pressure of a gas mixture is equal to the sum of the pressures that each component would exert if it were alone at the mixture temperature and volume. 
 - Amagat’s law states that the volume of a mixture is equal to the sum of the volumes each component would occupy if it were alone at the mixture temperature and pressure. 
 - One can derive these results directly by evaluating the partition function for the mixture.
- - -
- For the Gibbs representation in which temperature, pressure and mass, mole number, or molecular number are the independent variables, the following simple constraints over all $r$ species thus hold for the extensive properties.
$$\begin{array}{l}
U=\sum_{j}^{r} U_{j}=\sum_{j}^{r} u_{j} N_{j} \\
H=\sum_{j}^{r} H_{j}=\sum_{j}^{r} h_{j} N_{j} \\
S=\sum_{j}^{r} S_{j}=\sum_{j}^{r} s_{j} N_{j}
\end{array}$$
- Similarly for the normalized or specific properties
$$\begin{aligned}
u & = \sum_{j}^{r} x_{j} u_{j} \\
h &=\sum_{j}^{r} x_{j} h_{j} \\
s &=\sum_{j}^{r} x_{j} s_{j} \\
c_{v} &=\sum_{j}^{r} x_{j} c_{v j}
\end{aligned}$$
- where $x_j$ is the mole fraction for specie $j$, defined as $x_j = \frac{N_j}{N_{\text{tot}}}$
- We have seen that internal energy and enthalpy are a function only of temperature. 
- Thus, in these summations, $h_j$ and $u_j$ are evaluated at the mixture temperature. 
- In the Gibbs representation, however, entropy is a function of both temperature and pressure. 
- The $s_j$ must be evaluated at the mixture temperature and the partial pressure, or
$$s(T, p)=\sum_{j}^{r} x_{j} s_{j}\left(T, p_{j}\right)$$
- It is common to rewrite this expression in terms of the mole fraction and total pressure. The Gibbs representation expression for the entropy is
$$s_2 - s_1 = c_p \ln \frac{T_2}{T_1} - R \ln \frac{p_2}{p_1}$$
- For application to a mixture, this relation is used to relate the entropy at the partial pressure to that at the total pressure. Thus,
$$s_j(T, p_j) = s_j(T, p) + R \ln x_j$$

### Changes in Properties on Mixing
- When a mixture undergoes a state change, calculating the change in properties is straightforward
$$\begin{aligned}
\Delta u_{m i x} &=\sum_{j}^{r} x_{j} \Delta u_{j} \\
\Delta h_{m i x} &=\sum_{j}^{r} x_{j} \Delta h_{j} \\
\Delta s_{m i x} &=\sum_{j}^{r} x_{j} \Delta s_{j}
\end{aligned}$$
- However, when the ideal gases are mixed, special care must be taken with the entropy because of its pressure dependence $\Delta s_j = s_j(T_2, p_2) − s_j(T_1, p_1)$
- Consider the divided volume as shown below, where sides A and B of the volume are at the same temperature and pressure, but contain difference species. 
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/25/Annotation-2020-08-25-155853.jpg)
- The barrier between the two sides is then removed and the gases allowed to mix. The change of entropy for the systems becomes
$$\Delta s=-x_{A} R_{A} \ln \left(\frac{p_{A}}{p}\right)-x_{B} R_{B} \ln \left(\frac{p_{B}}{p}\right)$$
- Since both $p_A$ and $p_B$ are less than $p$, this means there is an entropy increase because of mixing.

## Reacting Mixtures
### General Case
- The most straightforward way to find the equilibrium state of a reacting mixture is to **minimize the appropriate thermodynamic potential**. 
- For example, if the $p$ and $T$ are to be controlled, then we could minimize the Gibbs function $G(T, p,N_1, \ldots ,N_c)$ where $r$ is the total number of compounds being considered. If $T$ and $V$ are held constant, then minimize the Helmholtz function $F(T, V,N_1, \ldots ,N_c)$
- So, their derivates will be:
$$\begin{array}{l}
d G=-S d T+V d p+\sum_{j}^{r} \mu_{j} d N_{j}\\
d F=-S d T-p d V+\sum_{j}^{r} \mu_{j} d N_{j} 
\end{array}$$
- where $j$ is the species index. In either case, we hold the independent parameters constant except for the $N_j$ and set the total derivative equal to zero. Thus $\sum_{j}^{r} \mu_{j} d N_{j} = 0$
- The minimization is subject to a set of constraints, namely that atoms, the basic building blocks of molecules, be conserved and that no mole numbers be negative. We can write
$$b_k = \sum_{j}^{r} n_{kj} N_j$$
- where $n_{kj}$ is the number of $k$-type atoms in $j$-type molecules. Thus, $b_k$ is the total number of $k$-type atoms in the mixture. (The form of the no negative mole number requirement depends on the specific numerical method to be used.)
- The temperature, pressure, or volume and number dependency is contained in the equation of state for the $\mu_j$. The ideal gas expression for the chemical potential can be understood by recalling that $G \equiv U − TS + pV$
- By Euler’s relation
$$U = TS - pV + \sum_{i = 1}^{r} \mu_i N_i$$
- Thus, $G = \mu_1 N_1 + \mu_2 N_2 + \ldots + \mu_c N_c$. The chemical potential can be thought of as the specific Gibbs function, since $g = \frac{G}{N}$.
- In an ideal gas mixture, specific or partial properties are evaluated at the given temperature and partial pressure of the component in question, or
$$G=\sum_{j}^{r} \mu_{j}\left(T, p_{j}\right) N_{j}$$
- However, we need a relationship for the $\mu_j$ that is explicit in $p_j$ or $x_j$. Noting that $g = h − Ts = h(T) − Ts(T, p)$, we can write
$$\mu_j(T, p_j) = g_j(T, p_j) = g_j(T, p) + RT \ln x_j$$
- The minimization function thus becomes
$$G=\sum_{j}^{r}\left[g_{j}(T, p)+R T \ln x_{j}\right]$$
- There are a number of numerical methods to minimize a function subject to constraints. Let us use the Matlab function `fmincon` to solve the problem of equilibrium between gaseous water, hydrogen, and oxygen. However, to proceed requires knowing the Gibbs function $g_j(T, p)$.

### Properties for Equilibrium and 1st Law Calculations
- A concerted effort to compile properties was one goal of the JANNAF (Joint Army and Navy NASA Air Force) Interagency Propulsion Committee. 
- JANNAF was formed in 1946 to consolidate rocket propulsion research under one organization. 
- It still functions as the US national resource for worldwide information, data, and analysis on chemical, electrical, and nuclear propulsion for missile, space, and gun propulsion systems. 
- Much of the property work has been carried out by NIST, the National Institute of Standards and Technology.
- The property values compiled under the JANNAF program were published as the [NIST–JANNAF  Thermochemical Tables](https://janaf.nist.gov/)
- $C^0_p, S^0, [G^0 - H^0]/T, H − H^0 (T_r), \Delta_f H^0, \Delta_f G^0, \text{ and }\log K_f$. (The NIST notation for $K_p$ is $K_f$ , where the subscript $f$ stands for formation.)
- $C^0_p$ is the constant-pressure ideal gas specific heat. 
- $S^0$ is the absolute entropy evaluated at the standard reference pressure of $1 \mathrm{bar}$, going to zero at $0 \mathrm{K}$. 
- The term $H − H^0(T_r)$ refers to the change in enthalpy with respect to the standard reference temperature, $298.15 \mathrm{K}$.
- To obtain the entropy at some pressure other than $1 \mathrm{bar}$, use the relation
$$S(T, p)=s^{\circ}-R \ln \frac{p}{p_{r e f}}$$
- The JANNAF tables also list the heat of formation $\Delta_f H^0$. This is the enthalpy required to form the compound from elements in their standard state at constant temperature and pressure. 
- Thus, oxygen and hydrogen, for example, would be in the diatomic form $O_2$ and $H_2$, while carbon would be in the atomic form $C$. 
- The value of $\Delta_f H^0$ is negative when energy is released, as a compound is formed from its elements. 
- To convert $\Delta_f H^0$ between the gas and liquid phases, add the heat of vaporization:
$$\Delta_{f} H_{298.15}^{\circ}(g a s)=\Delta_{f} H_{298.15}^{\circ}(\text {liq})+h_{f g, 298.15}$$
- $\Delta_f G^0$ is called the Gibbs free energy of formation. It is zero for elements in their equilibrium form, but not for compounds. 
- $\Delta_f G^0$ used in a numerical Gibbs free energy minimization. (The term $[G^0 - H^0]/T$ was included in the tables when hand calculations were more common. See the introduction to the JANNAF tables for more information.)
- Also listed in the tables are the logarithms of the equilibrium constants, $\log_{10} K_f$ , for formation of the compound from elements in their standard state. $\log_{10} K_f$ is zero for elements in their standard state, but nonzero for compounds.
- For computational work, it is most convenient to have the properties in the form of algebraic relations. It has been shown that this can be done by fitting properties to polynomial functions. For many application programs, these polynomials are
$$\begin{array}{c}
\frac{C_{p}^{0}}{R}=a_{1}+a_{2} T+a_{3} T^{2}+a_{4} T^{3}+a_{5} T^{4} \\
\frac{H^{\circ}}{R T}=a_{1}+\frac{a_{2}}{2} T+\frac{a_{3}}{3} T^{2}+\frac{a_{4}}{4} T^{3}+\frac{a_{5}}{5} T^{4}+\frac{a_{6}}{6} T^{5} \\
\frac{S^{0}}{R T}=a_{1} \ln T+a_{2} T+\frac{a_{3}}{2} T^{2}+\frac{a_{4}}{3} T^{3}+\frac{a_{5}}{4} T^{4}+a_7
\end{array}$$
> ### Example:
> Consider one mole of water vapor, $H_2O$. If it is heated to a high enough temperature, then it can dissociate into $O_2$ and $H_2$. Here we solve the equilibrium problem at $3000 \mathrm{K}$ numerically using Matlab.
> ```matlab
> clear
> clc
> R = 0.0083144598; % kJ /mol /K
> T = 3000; % K
> % Species names
> species = { 'H2O' 'O2' 'H2' };
> % Delta_fG^0 for included species at given T
> % from JANNAF Tables
> DfG0H2O = -77.163;
> DfG0O2 = 0 ;
> DfG0H2 = 0 ;
> g0 = [ DfG0H2O DfG0O2 DfG0H2 ] ; % kJ /mol
> % Number of k type atoms in j molecule
> nkj = [1 2 0 % oxygen
>        2 0 2]; % hydrogen
> % Initial conditions − number of atoms
> bk = [1 % oxygen atoms
>      2]; % hydrogen atoms
> % Lower bounds on mole numbers
> lb = [0 0 0 ] ; % no mole numbers less than zero allowed
> % Initial guesses for moles of each molecule
> nj0 = [1e-3 1e-3 1e-3];
> % Run minimization
> gfun = @(nj) sum( nj .* ( g0 / (R*T) + log ( nj / sum( nj ) ) ) ) ;
> options = optimset ( 'Algorithm' , 'sqp' ) ;
> [ nj fval ] = fmincon ( gfun , nj0 , [ ] , [ ] , nkj , bk , lb , [ ] , [ ] , options ) ;
> % Mole fractions
> molfrac = ( nj / sum( nj ) )';
> fprintf ( '# Species Nj x j \n ' )
> for i =1: numel ( nj )
> fprintf ( '%5d%10s%10.3g%10.3g \n ' , i , species { i } , nj ( i ) , molfrac ( i ) )
> end
> ```
> #### Output:
> Mole fractions predicted by Matlab script 
> | H2O   | O2     | H2    |
> |-------|--------|-------|
> | 0.794 | 0.0687 | 0.137 |


### The Equilibrium Constant
- The discussion above provides a methodology for calculating the equilibrium composition of a reacting gas mixture. However, it is best suited to numerical calculations. 
- For the case of one or two reactions, the equilibrium constant approach may be more useful.
- - - 
- We start by recalling that the equilibrium condition requires minimizing the Gibbs free energy $dG_{\text{mix}} = 0$ which, for a mixture of ideal gases, is
$$d G_{m i x}=0=\sum_{j}^{r} d N_{j} g_{j}(T, p)=\sum_{j}^{r} N_{j} \ln \left[g_{j}(T, p)+R T \ln \left(p_{j} / p\right)\right]$$
- Consider the reaction $aA + bB + \ldots \rightleftharpoons eE + fF + \ldots$
- The change in the number of moles of each specie is directly proportional to its stoichiometric coefficient ($a, b,$ etc.) times a progress of reaction variable $\alpha$
$$\begin{array}{l}
d N_{A}=-\alpha a \\
d N_{B}=-\alpha b \\
\vdots \\
d N_{E}=+\alpha e \\
d N_{F}=+\alpha f
\end{array}$$
- If we substitute this into the equation for$dG_{\text{mix}}$, we obtain $\Delta G_T = −RT \ln K_p$
$$\begin{array}{c}
\Delta G_{T}=\left(e g_{E}+f g_{F}+\cdots-a g_{A}-b g_{B}-\cdots\right) \\
K_{p}=\frac{\left(p_{E} / p\right)^{e}\left(p_{F} / p\right)^{f} \cdots}{\left(p_{A} / p\right)^{a}\left(p_{B} / p\right)^{b} \ldots}
\end{array}$$
- with $K_p$ being the Equilibrium Constant
- It is common to define the Gibbs free energy of formation,  $\Delta_f G^0$, as the value of  $\Delta G$ at a reference pressure, typically the standard state pressure of $1 \mathrm{bar} = 0.1 \mathrm{MPa}$. 
- This makes it a function of temperature only. Then one can still use the above relations as long as the equilibrium constant is written
$$K_{p}=\frac{\left(p_{E} / p_{\text {ref}}\right)^{e}\left(p_{F} / p_{\text {ref}}\right)^{f} \cdots}{\left(p_{A} / p_{\text {ref}}\right)^{a}\left(p_{B} / p_{\text {ref}}\right)^{b} \cdots}$$
- where $p_{\text{ref}}$ is the standard state pressure. Noting that $p_j = x_jp = \frac{N_j}{N_{\text{tot}}}p$
- we can write
$$K_{p}=\frac{N_{E}^{e} N_{F}^{f} \cdots}{N_{A}^{a} N_{B}^{b} \cdots}  \left(\frac{P}{N_{t o t}}\right)^{e+f+\cdots-a-b-\ldots}$$
- Both $\Delta_f G^0$ and $\log_{10} K_p$ are tabulated in the JANNAF tables. They are related by
$$\Delta_f G^0(T) = −RT \ln K_p(T)$$
- using the ideal gas relation. The molar concentration can be written (where the bracketed notation is common when discussing chemical reactions)
$$\left[C_{j}\right]=x_{j} \frac{p}{R T}=\frac{p_{j}}{R T}$$
- so we can define an equilibrium constant based on molar concentrations
$$\begin{array}{c}
K_{p}=K_{c}\left(\frac{R T}{p}\right)^{e+f+\cdots-a-b-\ldots} \\
K_{c}=\frac{[E]^{e}[F]^{f} \cdots}{[A]^{a}[B]^{b} \ldots}
\end{array}$$

### The Principle of Detailed Balance
- Now consider the reaction
$$A+B \underset{k_{b}}{\stackrel{k_{f}}{\rightleftarrows}} C+D$$
- where $k_f$ and $k_b$ are called reaction rate coefficients. 
- Suppose we wish to explore the time behavior of this reaction when starting from a non-equilibrium state, say all $A$ and $B$ but no $C$ and $D$. 
- It can be shown that the rate of destruction of $A$ can be written as
$$\frac{d[A]}{d t}=-k_{f}[A][B]+k_{b}[C][D]$$
- The reaction rate coefficients contain information about the nature of reacting collisions between molecules and are typically only a function of temperature. 
- The concentration terms reflect the dependence on the frequency of collisions on concentration and thus pressure. 
- If the mixture is in equilibrium, then the concentrations should be unchanging. Thus,
$$0=-k_{f}[A][B]+k_{b}[C][D]$$
$$\frac{[C][D]}{[A][B]}=\frac{k_{f}(T)}{k_{b}(T)}=K_{c}(T)$$
- This leads to the incredibly important principle of detailed balance. 
- If the $k$’s are a function of molecular structure and the translational energy is in equilibrium, then this relation should hold even when the mixture is not in chemical equilibrium. 
- Using above equations, only one of the two reaction rate coefficients is independently required, assuming the equilibrium constant is available.