---
title: Day 04: Microscopic Thermodynamics
description: 
published: true
date: 2020-09-04T08:19:13.819Z
tags: 
editor: markdown
---

# Microscopic Thermodynamics
## The Role of Statistics in Thermodynamics
- Even if we ignore the fact that the behavior of individual atoms and molecules is governed by **quantum mechanics**, it would be impossible to simultaneously solve the enormous number of equations of motion involved to describe the evolution of a macroscopic system to equilibrium. 
- Clearly, an alternative approach is required and fortunately, nature has been kind in devising the laws of averaging in ways that allow for great simplification.
### Gendakenexperiment:
- Suppose $N$ atoms are placed in a box of fixed volume $V$, which is then closed and adiabatic. 
- $N$ is chosen small enough so that the system is always in the gas phase. 
- The kinetic energy $\epsilon$ of each particle is the same and nonzero, and when the particles are put in the box they are all placed in one corner.
- Only kinetic energy is considered and for simplicity, we will assume that the trajectory of each particle is described by **Newton’s Law**. 
- How will this system evolve?
- For mathematicians, this leads to a chaotic state.
- We call the final state the equilibrium state.
### Now What?
- We know from quantum mechanics that, in the absence of applied forces, the dynamic state of an atom or molecule will relax to a fixed quantum state. 
- The atom or molecule arrives at that state as a result of interactions with other particles.
- The number of system quantum states that can satisfy a given set of macroscopic constraints is enormous, approximately $e^N$ where $N$ is the number of particles.
- The system quantum state is constantly changing. No individual allowed system quantum state is physically preferred over any other state. (This is called **equal a priori** probability.)
### Double Approaches to Consider
- If equilibrium quantum states are so much more probable than non-equilibrium ones, then one way to proceed is to look at the relative probability of each allowed system quantum state, and characterize equilibrium with the most probable one. Indeed, that is the approach we will follow. 
- The only remaining question is how to find that state.
- There are **two historical approaches**. 
- **The first** makes the equal a priori assumption discussed above. It involves watching a single system and finding the most probable of all the allowed states. 
- The difficulty with this approach is that it has no physical analog, it being physically impossible for all allowed states to appear in a single system.
- **The second approach** we will take is that followed by Gibbs. 
- It involves to imagine a very large number of identical macroscopic systems. Gibbs called this collection an ensemble, and each individual system a member of the ensemble. 
- If the number of ensemble members is large enough (which it can be, since we are imagining the ensemble), then at any instant in time all allowed quantum states will appear.
### Distributions Madness:
![enter image description here](https://theskillcraft.com/img-host/images/2020/08/27/distrib.png)
- Suppose we are able to find the most probable system quantum state for a given set of independent properties. 
- How would we characterize the state and what could we do with it? 
- Recall that the quantum state of a macroscopic system is specified by the distribution of microscopic quantum states.
- Suppose we index all possible system quantum states with the index $j$. Then, if $n_j$ is the number of ensemble members that exist in system quantum state $j$, and $n$ is the number of ensemble members, we can calculate the mechanical parameters $U, V,\text{ and }N_i$.
$$\langle A \rangle = \frac{1}{n}\sum_{j} n_j A_j$$
- The bracket indicates average or expectation value, and 
  + $j$ = ensemble member quantum state index
  + $A_j = U_j$, $V_j$, or Nij
  + $n_j$ = number of ensemble members in quantum state $j$
  + $n$ = total number of ensemble members
## The Postulates of Microscopic Thermodynamics
- The postulates we will invoke were first stated by Gibbs in 1902. In the foreword of his book he stated,
> The only error into which one can fall, is the want of agreement between the premises and the conclusions, and this, with care, one may hope, in the main, to avoid.
- His formulation forms the backbone of modern statistical thermodynamics.
### Postulate 1:
- The macroscopic value of a mechanical–thermodynamic property of a system in equilibrium is characterized by the expected value computed from the most probable distribution of ensemble members among the allowed ensemble member quantum states.
### Postulate 2:
- The most probable distribution of ensemble members among ensemble member quantum states is that distribution for which the number of possible quantum states of the ensemble and reservoir is a maximum.
### Purport for the Postulates:
- Postulate 1 states that 
$$\langle A\rangle=\frac{1}{n} \sum_{j} n_{j}^{*} A_{j}=\sum_{j} p_{j} A_{j}$$
where $p_j = n^∗_j /n$ is the normalized probability distribution and $*$ indicates that we are using the most probable distribution of $n_j$’s or $p_j$’s.
- Postulate II describes how to determine the most probable distribution. 
- To apply the postulate we must obtain an expression for the number of allowed quantum states as a function of the $n_j$. 
- Then, find the $n_j$ that maximizes this function.
- *For an ensemble involving a reservoir*, the members are in some quantum state, the reservoir in another. 
- If $\Omega$ is the number of states available to the members, and $\Omega_R$ the number available to the reservoir, then the total number available to the entire ensemble including the reservoir is
$$\Omega_{TOT} = \Omega_{R} \Omega$$
- This is the joint probability of two independent random processes.
- It will turn out that we don’t need $\Omega_{R}$. We will need, however, an expression for $\Omega$ in terms of $n_j$. The question is: How many ways (permutations) can $n$ members in a given distribution (combinations) of quantum states be arranged? From basic probability mathematics,
$$\Omega = \frac{n!}{\prod_{j} n_j !}$$
> If we have $k$ quantum states, then we have
> $$\Omega = \frac{n!}{n_1 ! n_2 ! \cdots n_k !}$$

$$\Omega_{TOT} = \Omega_{R} \frac{n!}{\prod_{j} n_j !}$$
- We wish to maximize this function, subject to any appropriate constraints. It will turn out to be easier if we maximize the natural log of the function, applying **Sterling’s approximation**
$$\ln(x! ) = x \ln x − x, \text{ if } x >> 1$$

> ### A Quick Python Script to understand the Growth Rate for Factorials
> ```python
> n = 100
> def facto(r):
>   if r is 0 or r is 1:
>     return 1
>   else:
>     return r * facto(r-1)
> k = 1
> while k is not n:
>   print(facto(k))
>   k = k + 1
>```
> The Output for the program is:
> ```
> 1
> 2
> 6
> ...
> A 155 digit number for 99!
> ```
- Taking the logarithm of $\Omega_{TOT}$ and applying the approximation, we obtain
$$\ln \Omega_{T O T}=\ln \Omega_{R}+n \ln n-\sum_{j} n_{j} \ln n_{j}$$

## The Partition Function and its Alternative Formulations
- To proceed further, we need to make a decision about what type of ensemble to use. 
- The possible choices are shown in Table below:
$$\begin{array}{lll}
\hline \text { Gibbs' name } & \text { Independent parameters } & \text { Fundamental relation } \\
\hline \text { Micro-canonical } & U, V, N_{i} & S\left(U, V, N_{i}\right) \\
\text { Canonical } & 1 / T, V, N_{i} & S[1 / T] \\
& U, V,-\mu_{i} / T & S\left[-\mu_{i} / T\right] \\
\text { Grand Canonical } & 1 / T, V,-\mu_{i} / T & S\left[1 / T, V,-\mu_{i} / T\right] \\
& U, p / T, N_{i} & S\left[U, p / T, N_{i}\right] \\
& 1 / T, p / T, N_{i} & S\left[1 / T, p / T, N_{i}\right] \\
& U, p / T,-\mu_{i} / T & S\left[U, p / T,-\mu_{i} / T\right] \\
& 1 / T, p / T,-\mu_{i} / T & S\left[1 / T, p / T,-\mu_{i} / T\right] \\
\hline
\end{array}$$
- Let us start with Grand Canonical Ensemble:
- Thus, only the volume of the ensemble members is fixed, and we will need constraints on energy and number of particles. 
- We also need to recognize that there is a constraint on the sum of all the $n_j$ which must equal $n$. Thus, the constraints become
> $$n=\sum_{j} n_{j}$$
> $$U_{T O T}=U_{R}+\sum_{j} n_{j} U_{j}$$
> $$N_{i T O T}=N_{i R}+\sum_{j} n_{j} N_{i j}$$
- We will use Lagrange’s method of undetermined multipliers to maximize $\Omega_{TOT}$ subject to the constraints.
- We start by taking the total derivative of $\ln \Omega_{TOT}$ and setting it to zero:
$$d \ln \Omega_{T O T}=\frac{\partial \ln \Omega_{R}}{\partial U_{R}} d U_{R}+\sum_{i} \frac{\partial \ln \Omega_{R}}{\partial N_{i R}} d N_{i R}-\sum_{j}\left(1+\ln n_{j}\right) d n_{j}=0$$
- Since $n, U_{TOT} ,\text{ and }N_{iTOT}$ are constants, by differentiation we obtain
> $$0=\sum_{j} d n_{j}$$
> $$0=d U_{R}+\sum_{j} U_{j} d n_{j}$$
> $$0=d N_{i R}+\sum_{j} N_{i j} d n_{j}$$
- Since these derivatives are each equal to zero, there is no reason why each cannot be multiplied by a constant factor, nor why they can’t be added to or subtracted from the expression for $d \ln \Omega_{T O T}$ . 
- Historically, the multipliers chosen are $\alpha − 1, \beta,\text{ and }\gamma_i$ and they are subtracted
$$\begin{aligned}
\left[\beta-\frac{\partial \ln \Omega_{R}}{\partial U_{R}}\right] d U_{R} &+\sum_{i}\left[\gamma_{i}-\frac{\partial \ln \Omega_{R}}{\partial N_{i R}}\right] d N_{i R} \\
&+\sum_{j}\left(\ln n_{j}+\alpha+\beta U_{j}+\sum_{i} \gamma_{i} N_{i j}\right) d n_{j}=0
\end{aligned}$$
- Since $U_R, n_{iR},\text{ and }n_j$ are independent variables, the coefficients of their derivatives must each be zero. 
- Thus
$$\beta=\left(\frac{\partial \ln \Omega_{R}}{\partial U_{R}}\right)_{N_{i R}, V}$$
$$\gamma_{i}=\left(\frac{\partial \ln \Omega_{R}}{\partial N_{i R}}\right)_{U_{R}, N_{k R, k \neq i} V}$$
$$\alpha=-\ln n_{j}-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}$$
- The most probable distribution, the $n^∗_j$ ’s, can be found from the equation for $\alpha$:
$$n_{j}^{*}=\exp \left(-\alpha-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}\right)$$
- If we sum over $n^∗_j$ , then
$$\mathrm{e}^{\alpha}=\frac{\sum_{j} e^{-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}}}{n}$$
- Now, we have the probability $p_{j}$ as:
$$p_{j}=\frac{n_{j}^{*}}{n}=\frac{e^{-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}}}{\sum_{j} e^{-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}}}$$
- The denominator of this expression plays a very important role in thermodynamics. It is called the **partition function**, in this case the **grand partition function**
$$Q_{G}\left(\beta, \gamma_{i}\right) \equiv \sum_{j} e^{-\beta U_{j}-\sum_{i} \gamma_{i} N_{i j}}$$
- The physical significance of the partition function is that it determines how ensemble members are distributed, or partitioned, over the allowed quantum states. 
- Also, note that $\alpha$ has dropped out of the expression for both $p_j$ and $Q_G$.
- The Lagrange multipliers, $\beta$ and $\gamma_i$, are associated with $U_j$ and $N_{ij}$, respectively. It would not be too surprising if they turned out to be related to $1/T$ and $−\mu_i/T$. 
- the product $\beta U_j$ must be unitless, as must $\gamma_iN_{ij}$. 
$$\beta =\frac{1}{k_B T}$$
$$\gamma_{i} =\frac{-\mu_{i}}{k_B T}$$
- By carrying out an analysis similar to that above for all the possible representations, we would find that in each case, the probability distribution can be represented in the form
$$p_{j}=\frac{e^{-f_{j}}}{\sum_{j} e^{-f_{j}}}$$
- The natural logarithm of the partition function times Boltzmann’s constant is the **fundamental relation in the form of entropy** or its associated **Massieu function**
$$S [\cdots] = k \ln Q$$
## Thermodynamic Properties
$$\begin{array}{llll}
\hline & \text { Independent } & & \text { Fundamental } \\
\text { Gibbs' name } & \text { parameters } & \text { Partition function } & \text { relation } \\
\hline \text { Microcanonical } & U, V, N_{i} & Q=\Omega & S\left(U, V, N_{i}\right) \\
\text { Canonical } & 1 / T, V, N_{i} & Q=\sum_{j} \exp \left(-\frac{U_{j}}{k T}\right) & S[1 / T] \\
& U, V,-\mu_{i} / T & Q=\sum_{j} \exp \left(\sum_{i} \frac{\mu_{i}}{k T} N_{i j}\right) & S\left[-\mu_{i} / T\right]\\
\text { Grand Canonical } & 1 / T, V,-\mu_{i} / T & Q=\sum_{j} \exp \left(-\frac{U_{j}}{k T}+\sum_{i} \frac{\mu_{i}}{k T} N_{i j}\right) & S\left[1 / T, V,-\mu_{i} / T\right] \\
& U, p / T, N_{i} & Q=\sum_{j} \exp \left(-\frac{P}{k T} V_{j}\right) & S\left[U, p / T, N_{i}\right] \\
& 1 / T, p / T, N_{i} & Q=\sum_{j} \exp \left(-\frac{U_{j}}{k T}-\frac{P}{k T} V_{j}\right) & S\left[1 / T, p / T, N_{i}\right] \\
& U, p / T,-\mu_{i} / T & Q=\sum_{j} \exp \left(-\frac{P}{k T} V_{j}+\sum_{i} \frac{\mu_{i}}{k T} N_{i j}\right) & S\left[U, p / T,-\mu_{i} / T\right] \\
& 1 / T, p / T,-\mu_{i} / T & Q= 
 & S\left[1 / T, p / T,-\mu_{i} / T\right] \\
 & & \sum_{j} \exp \left(-\frac{U_{j}}{k T}-\frac{P}{k T} V_{j}+\sum_{i} \frac{\mu_{i}}{k T} N_{i j}\right) & \\
\hline
\end{array}$$
- It remains to interpret the multipliers and relate what we have learned to the fundamental relation. 
- Assume that we are working with the canonical representation, so that
$$Q=\sum_{j} \exp \left(-\beta U_{j}\right)$$
and 
$$p_{j}=\frac{e^{-\beta U_{j}}}{Q}$$
- Apply the first postulate to calculate the energy
$$\langle U \rangle = \sum_j p_j U_j$$
- Take a derivative
$$dU = \sum_j U_jdp_j + \sum_j p_jdU_j$$
- The two terms in RHS equate to:
- $$\sum_{j} U_{j} d p_{j}=-\frac{1}{\beta} d\left(\sum_{j} p_{j} \ln p_{j}\right)$$
- and pressure $P$ is defined as
- $$P=\sum_{j} p_{j} P_{j}=-\sum_{j} p_{j} \frac{\partial U_{j}}{\partial V}$$
- Utilizing these results, we have
$$d U=-\frac{1}{\beta} d\left(\sum_{j} p_{j} \ln p_{j}\right)-P d V$$
- Comparing this equation with
$$dU = TdS − PdV$$
- We have here
$$S=-k \sum_{j} p_{j} \ln p_{j}$$
- If we substitute the expression for $p_j$ into this result for $S$, then
$$S = \frac{1}{T}U + k \ln Q$$
- Compare this with the definition of $S[1/T]$
$$S\left[\frac{1}{T}\right]=S-\frac{1}{T} U$$
- We get the famous relation engraved in the grave of Boltzmann:
$$S\left[\frac{1}{T}\right] = k_B \ln Q$$
- These results apply for any representation!!
- The function
$$\mathcal{I} = - \sum_{j} p_{j} \ln p_{j}$$
is called **Information** in Information Theory.
- $\mathcal{I}$ is maximized when all the $p_j$ are equal or all states are equally probable.
### Interpreting Entropy:
- One way to interpret the importance of entropy is to study the effect of quasi-static work or heat transfer on the entropy.
- $$\langle U \rangle = \sum_j p_j U_j$$
- $$dU = \sum_j U_jdp_j + \sum_j p_jdU_j$$
- $$d U=\sum_{j} U_{j} d p_{j}-P d V$$
- Comparing this to the 1st Law
$$dU = \delta W + \delta Q$$
- If we assume that the work is reversible, then we can make the associations
- $\delta Q = \sum_j U_jdp_j$
- $\delta W = \sum_j p_jdU_j$
- For work to occur, only the $U_j$’s are required to change, not the $p_j$’s. If this occurs, then the entropy is constant and we call the work isentropic. However, for there to be heat transfer, the $p_j$’s must change, and thus the entropy changes.
## Fluctuations
$$\sigma^{2}(A) \equiv\left\langle(A-\langle A\rangle)^{2}\right\rangle$$
$$\sigma^{2}(A)=\sum_{j} p_{j} A^{2}-\langle A\rangle^{2}$$
- Since we know the $p_j$, we can calculate the variance. 
- Consider, for example, the variance of energy in the canonical representation:
$$\sigma^{2}(U)=\sum_{j} p_{j} U_{j}^{2}-\langle U\rangle^{2}$$
- This can be written as
$$\sigma^{2}(U)=\frac{\sum_{j} U_{j}^{2} e^{-\beta U_{j}}}{\sum_{j} e^{-\beta U_{j}}}-\left\{\frac{\sum_{j} U_{j} e^{-\beta U_{j}}}{\sum_{j} e^{-\beta U_{j}}}\right\}^{2}$$
or
$$\sigma^{2}(U)=-\left\{\frac{\partial}{\partial \beta} \frac{\sum_{j} U_{j} e^{-\beta U_{j}}}{\sum_{j} e^{-\beta U_{j}}}\right\}=\left(\frac{\partial^{2} \ln Q}{\partial \beta^{2}}\right)$$
- But if we observe closely, we can infer that
$$\langle U\rangle=-\frac{\partial \ln Q}{\partial \beta}$$
so that
$$\sigma^{2}(U)=-\left(\frac{\partial^{2} U}{\partial \beta^{2}}\right)_{V, N}=\frac{1}{k T^{2}}\left(\frac{\partial^{2} U}{\partial T^{2}}\right)_{V, N}$$
- For an ideal gas the caloric equation of state is
$$U = c_vNT$$
so that
$$\sigma^2(U) = c_vNkT^2$$
and
$$\frac{\sigma(U)}{U}=\sqrt{\frac{k}{c_{v} N}}$$
- This development can be generalized for any mechanical property that is allowed to fluctuate in any representation
$$\sigma^{2}(A)=\frac{\partial^{2} \ln Q}{\partial a^{2}}$$
- where $a$ is the associated multiplier for $A$, that is $\beta, \pi,\text{ or }\gamma_i$. ($\pi$ is the usual symbol for $p/k_BT$.)