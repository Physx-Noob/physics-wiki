---
title: Day 2: Fundamentals of Macroscopic Thermodynamics
description: 
published: true
date: 2020-08-26T14:44:36.160Z
tags: 
editor: undefined
---

# Fundamentals of Macroscopic Thermodynamics

## Postulates of Macroscopic (Classical) Thermodynamics
### Postulate 1:

 There exist certain states (called equilibrium states) of simple systems that, macroscopically, are characterized completely by the internal energy $U$, the volume $V$, and the mole numbers $N_1,N_2, \cdots ,N_r$ of the chemical components, where $r$ is the number of chemical components.
 - independent from history of the system
 - this implies that all atomic states must be allowed

### Postulate 2:

There exists a function called the entropy, $S$, of the extensive properties of any composite system, defined for all equilibrium states and having the following property: The values assumed by the extensive properties are those that maximize the entropy over the manifold of constrained equilibrium states.

- $S= S(U, V, N_{i})$
- this is the fundamental equation in Thermodynamics
- To derive fundamental relation from first principles requires application of thermodynamics
- this postulate tells us the entropy be maximum at equilibrium

### Postulate 3:
The entropy of a composite system is additive over the constituent subsystems.
The entropy is continuous and differentiable and is a monotonically
increasing function of energy. 
- $S = \sum_{j} S_j$ => Additivity
- $S_j = S_j(U_j, V_j, N_{ij})$ => Subsystem $j$
- $S(\lambda U, \lambda V, \lambda N_{i}) = \lambda S(U, V, N_{i})$ => homogeneous and first order function of extensive properties
- $\frac{\partial S}{\partial U}_{V, N_i} > 0$ => monotonic property
- $U = U(S, V, N_i)$ monotonic property, continuity and differentiability

For a single component system $j = 1$, so
- $S(U, V, N_{i}) = N S(\frac{U}{N}, \frac{V}{N}, 1)$
- defining normalized properties: $u \equiv \frac{U}{N}, v \equiv \frac{V}{N}, s \equiv \frac{S}{N}$
- $s = s(u,v)$
### Postulate 4:
The entropy of any system vanishes in the state for which $\frac{\partial U}{\partial S} _{V, N_i} = 0$ 

- Third Law of Thermodynamics
- Nernst Postulate
- $S \to 0$ as $T \to 0$

## Simple Forms of the Fundamental Relation
- Contains all the necessary information about the equilibrium behavior of specific
substances
### Van der Waals Substance
$$V(r) = - \frac{dF}{dr}$$
![the interaction energy between atoms as a function of distance](https://theskillcraft.com/img-host/images/2020/08/25/Capture.png)
$$S = NR \left \{ \left ( \frac{V}{V_0} - b \right ) \left( \frac{U}{U_0} + a \frac{V_0}{V}\right ) ^c \right \}$$
where $a, b, \text{ and } c$ are parameters of the relationship and $R$ is the universal gas constant

### Ideal Gas
$$S = S_0 + NR \left \{ \ln \left ( \frac{U}{U_0} \right ) ^c  + \ln \left ( \frac{V}{V_0} \right ) - (c + 1) \ln \left ( \frac{N}{N_0} \right ) \right \}$$

- $V$ and $U$ become large compared to $b$ and $a/v$
- for a monatomic gas $c = 3/2$
- The ideal gas fundamental relation does not satisfy the fourth postulate

## Equilibrium and the Intensive Properties
- To solve the fundamental problem we follow the dictate of the second postulate.
- for the composite system we are analyzing we calculate the entropy of each subsystem as a function of the extensive properties.

$$dS = \frac{\partial S}{\partial U} dU + \frac{\partial S}{\partial V} dV+ \frac{\partial S}{\partial N_j} dN_j$$

- The partial derivatives, which we have not yet interpreted, are functions of the extensive properties. 
- However, they are in a normalized form, being essentially ratios of extensive properties.
- As we shall see, they relate directly to the intensive properties we are familiar with.
### Thermal Equilibrium: The Meaning of Temperature
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/25/Annotation-2020-08-25-155853.jpg)
- from second postulate $S = S_A + S_B \implies dS = dS_A +dS_B$
- or $dS = \frac{\partial S}{\partial U} dU_A + \frac{\partial S}{\partial U} dU_B$
- total energy of system is conserved $\implies U = U_A + U_B$
- further $\implies dU = 0 = dU_A + dU_B$
- $$dS = \left \{ \frac{\partial S}{\partial U}_A - \frac{\partial S}{\partial U} _B \right \} dU_A$$
- at equilibrium $dS \to 0 \implies \frac{dS}{dU}_A = \frac{dS}{dU}_B$
Now the thermodynamic property we associate with heat transfer and thermal equilibrium is temperature.
- $$T = \frac{\partial U}{\partial S}_{V, N_i}$$
- Equilibrium requirement becomes $T_A = T_B$
### Mechanical Equilibrium: Meaning of Pressure
- Replace same barrier with a diathermal piston
- $$dS = \frac{\partial S}{\partial U}_A dU_A + \frac{\partial S}{\partial V}_A dV_A + \frac{\partial S}{\partial U}_B dU_B + \frac{\partial S}{\partial V}_B dV_B$$
- $V = V_A + V_B =$ const
- $dS = 0 = dV_A + dV_B$
- $$dS = \left \{ \frac{\partial S}{\partial U}_A - \frac{\partial S}{\partial U} _B \right \} dU_A + \left \{ \frac{\partial S}{\partial V}_A - \frac{\partial S}{\partial V} _B \right \} dV_A$$
- $$\frac{\partial S}{\partial U}_A = \frac{\partial S}{\partial U}_B \text{ and } \frac{\partial S}{\partial V}_A = \frac{\partial S}{\partial V}_B$$
The thermodynamic pressure is defined as:
- $$\frac{p}{T} = \frac{\partial S}{\partial V} _ {U, N_i}$$
- therefore the full equilibrium requirement becomes
- $$T_A = T_B \text{ and } p_A = p_B$$
### Matter Flow and Chemical Equilibrium: The Meaning of Chemical Potential
- let's say the fixed diathermal wall becomes permeable to some chemical components
- $$dS = \frac{\partial S}{\partial U}_A dU_A + \frac{\partial S}{\partial N_1}_A dN_1A + \frac{\partial S}{\partial U}_B dU_B + \frac{\partial S}{\partial N_1}_B dN_1B$$
- following the same steps we get:
- $$\frac{\mu_1}{T} = -\frac{\partial S}{\partial N_1}_{U, V, N_{i \neq 1}}$$
- $$T_A = T_B \text{ and } \mu_A = \mu_B$$
## Representation and the Equations of State
- $$dS = \frac{1}{T}dU + \frac{p}{T}dV - \sum_{i = 1} ^r \frac{\mu_i}{T} dN_i$$
- we could also write $U = U(S, V, N_i)$
- $$dU = TdS - pdV + \sum_{i = 1} ^r \mu_i dN_i$$
- in both representations, the coefficients are intensive parameters
- these intensive parameters can be separately calculated as a function of independent properties from a fundamental relation
- Such a relation is called Equation of State.
- In Energy representation, equation of state can take form as follows:
- $$T = T(S, V, N_i)$$
- $$p = p(S, V, N_i)$$
- $$\mu_i = \mu_i(S, V, N_i)$$

## The Euler Equation and the Gibbs–Duhem Relation
- There are two very useful general relationships that can be derived directly using the properties of the fundamental relation. 
- Called the Euler equation and the Gibbs–Duhem relation, they relate the extensive and intensive properties in particularly direct ways.
- $$U(\lambda S, \lambda V, \lambda N_i ) = \lambda U(S, V, N_i)$$
- $$\frac{\partial U}{\partial (\lambda S)} \frac{\partial (\lambda S)}{\partial \lambda} + \frac{\partial U}{\partial (\lambda V)} \frac{\partial (\lambda V)}{\partial \lambda} + \sum_{i = 1} ^r \frac{\partial U}{\partial (\lambda N_i)} \frac{\partial (\lambda N_i)}{\partial \lambda} = U$$
- $$\frac{\partial U}{\partial S} S + \frac{\partial U}{\partial V} V + \sum_{i = 1}^r \frac{\partial U}{\partial N_i}N_i = U$$
- $$U = TS - pV + \sum_{i = 1}^{r} \mu_i N_i$$
- This is called **Euler Equation**. In Entropy Representation, we have
- $$S = \frac{1}{T}U + \frac{p}{T}V - \sum_{i = 1} ^r \frac{\mu_i}{T} N_i$$
- The **Gibbs–Duhem relation** can be derived as follows
- $$dU = TdS + SdT -pdV - Vdp + \sum_{i = 1}^r d\mu_i N_i + \sum_{i = 1}^r \mu_i dN_i$$
- $$dU = TdS - pdV + \sum_{i = 1} ^r \mu_i dN_i$$
- subtracting the two, we get the result
- $$SdT -Vdp + \sum_{i = 1}^r d\mu_i N_i  = 0$$
- The Gibbs–Duhem relation shows that not all the intensive parameters are independent of each other. 
- The actual number of independent intensive parameters is called the **thermodynamic degrees of freedom**. 
- A simple system of $r$ components thus has $r + 1$ degrees of freedom. 
- As we shall see, this corresponds directly to **Gibbs’ phase rule**.