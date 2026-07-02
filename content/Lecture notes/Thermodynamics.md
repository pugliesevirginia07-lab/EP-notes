# Chapter 2 : Thermodynamics

See [[Differentials]] and [[Thermodynamic variables]].
## 1. Central limit theorem and Brownian motion and diffusion

### Introduction

- **Thermodynamics** studies macroscopic properties (temperature, pressure, volume, energy...).
- **Statistical physics** explains thermodynamics quantities from the microscopic behavior of particles, it studies probability distributions.
- **Soft matter** is a subfield of condensed matter physics which studies systems easily deformed by thermal fluctuations.

>[!multi-column] Review in distributions
>
>>[!abstract]- Binomial distribution
>>
>> We define $X$ as the number of successes in $n$ trials, and $p$ as the success probability. Then we can get the probability $P$ for a given $X$:
>> 
>> $$P(X=x)= \begin{pmatrix} n \\X \end{pmatrix}p^X(1-p)^{n-K}$$
>>
>>With the combinatorial $\frac{n!}{X!(n-X)!}$ We can also get the probability for an interval of successes ($X\leq x$ or $X\geq x$). 
>
>
>> [!abstract]- Gaussian distribution
>> 
>> When we have a large $n$ ($n, \ np, \ nq \gg 1$, with $q=(1-p)$), the binomial distribution approximates to a Gaussian:
>> 
>>  $$ P(X)=\frac{1}{\sqrt{2 \pi np}}e^{-\frac{(X-np)^2}{2npq}}$$
>>  
>> $$ P(x)=\frac{1}{\sqrt{2\pi \sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
>> 
>> With mean $\mu$ and variance $\sigma^2$.
>> 
>> ![[Gaussian distribution.png|200]]

### Central Limit Theorem and Brownian motion

The **Central Limit Theorem (CLT)** states that the sum of many independent random variables tends toward a Gaussian distribution, regardless of the original distribution.

If we have $\Delta x=\sum_i \delta x_i$, then for large $N$ we get an $\Delta x$ normally distributed.

The **Brownian motion** is the random motion of particles due to their kinetic energy, colliding between them. Each collision is a small random displacement, but the total displacement is the sum of many random distributions that approximate to a Gaussian in the end.

>[!abstract]- Wiener process
> The Wiener process is the mathematical model of ideal Brownian motion. 
>   
>   
>>[!note] Properties
>>1. Starts at 0:  $W_0=0$.
>>2. Independent increments with gaussian distribution:
>>
>>$$W(t+\Delta t)-W(t) \sim N(0, \Delta t)$$
>>
>> 3. Continuous but not differentiable.
>
> Mean: 
> $$\left\langle W(t) \right\rangle=0$$
>  
>  Variance: 
>  $$\text{Var}(W(t))=t \rightarrow \text{Var}(W(t))=\left\langle W^2(t) \right\rangle$$

The **mean squared displacement (MSD)** measures the average of the square of the position if you repeat the Brownian motion experiment many times, telling you how far the particle is from the origin.

$$\text{MSD}=\langle(\Delta x)^2\rangle$$
- For a Wiener process: 
$$\langle W^2(t)\rangle=t$$ 
- For a physical Brownian particle: 
$$\langle x^2(t)\rangle=2Dt$$
	with diffusion coefficient $D$.

>[!note] Types of motion from the MSD
>In general, $\langle r^2(t)\rangle \propto t^\alpha$ .
>
>![[Types of MSD.png]]
>>[!abstract]- Normal diffusion
>>
>> It corresponds to a Brownian motion, with $\alpha =1$.
>> 
>> $$\langle r^2(t)\rangle=2Dt$$ 
>
>> [!abstract]- Subdiffusion
>> 
>> The particles spread slower than Brownian motion, with $\alpha<1$.
>> 
>
>>[!abstract]- Superdiffusion
>>
>> The particles spreads faster than Brownian motion, with $\alpha>1$.
>
>>[!abstract]- Corralled motion
>>
>> The particles move with constant velocity, with $\alpha=2$.
>>
>>$$\langle r^2(t)\rangle=v^2t^2$$
>

The simplest equation describing Brownian motion is the **Langevin equation**:
$$m \frac{dv}{dt}=-\gamma v+\xi(t)$$
With mass $m$, friction term $-\gamma v$, representing the viscous drag, and random force $\xi (t)$, representing the molecular collisions. It can also contain a noise term. 

### Diffusion

The **diffusion** is the spontaneous spreading of particles, where the molecules in a gas or fluid move from a higher concentration to a lower concentration. It results in an eventual equalization of gas/fluid in the space and it is only reversible through external work.

>[!multi-column] Fick's laws of diffusion
>>[!example]- Fick's first law
>>
>> Flux goes from regions of high concentration to regions of low concentration.
>> 
>> $$J=-D \frac{\partial{\phi}}{\partial{x}}$$
>> 
>> with diffusion coefficient $D$ and concentration $\phi$.
>
>
>>[!example]- Fick's second law
>>
>> Shows how diffusion causes the concentration field to change with time $t$.
>> 
>> $$\frac{\partial\phi}{\partial t}=D\frac{\partial^2\phi}{\partial x^2}$$
>> 

The diffusion coefficient $D$ measures how quickly the particles spread, for large $D$, the particles spread rapidly, and vice versa.

>[!example] Einstein-Stokes equation
>
> $$D=\frac{k_BT}{6\pi\eta R}$$
> 
> with viscosity coefficient $\eta$ and particle radius' $R$.
>
> The momentum relaxation time would correspond to 
> $$\tau =\frac{m}{\gamma}$$
> 
> · For $t \ll \tau$: the particles still have some initial velocity, they follow a corralled motion.
> 
> · For $t \gg \tau$: the motion becomes diffusive (Brownian motion).

### Microstates, macrostates and phase space

- A **microstate** describes a system specifying the properties of each individual particle.
- A **macrostate** is the probability distribution of possible states across a certain statistical ensemble of all microstates. Described in terms of macroscopic quantities (such as $P$ or $V$). Two systems with the same values of macroscopic parameters are thermodynamically indistinguishable. A macrostate tells us nothing about a state of an individual particle, each macrostate contains a large number of microstates.

- A **phase space** is a space where all possible states of a system are represented, each possible state corresponds to one unique point. Every degree of freedom of the system is represented as an axis of a multidimensional space, such as in the phase space trajectory (relating position and velocity).

>[!example] Microstates for each macrostate
>
>$$ \Omega (n)=\begin{pmatrix}N\\n\end{pmatrix}=\frac{N!}{n!(N-n)!}$$
>
>with $n$ as the number of microstates in $N$ number of macrostates. The set of all possible configurations of the system as a phase space is $2^N$.

>[!abstract]- Ergodic hypothesis
> An isolated system in an equilibrium state, evolving in time, will pass through all the accessible microstates at the same recurrence rate, hence all accessible microstates are equally probable (fundamental assumption of statistical mechanics).
> 
> This would explain why a spontaneous compression of a gas is not impossible, but too improbable to ever occur, due to the amount of different microstates in all particles.

## 2. Heat, temperature and ideal gas law

> [!abstract]+ Thermal equilibrium
> After two objects have been in contact long enough, they reach a thermal equilibrium, when they have the same temperature. There is no heat flow between both of the systems.
> 
>  The relaxation time is the time required for a system to reach the thermal equilibrium.
>  
>  We assume the system is isolated, the energy stays inside of the system and it has unlimited time to reach the thermal equilibrium.

>[!abstract]+ Temperature ($T$)
>The temperature is a measure of the tendency of an object to spontaneously give up energy to its surroundings.
>
>When two objects are in thermal contact, the hotter object tends to transfer energy to the colder one.
>

From the [[kinetic theory of gases]], the absolute temperature of a gas is proportional to the average translational kinetic energy of its molecules, the Boltzmann's constant is the conversion factor between these two.

The coldest theoretical temperature is absolute zero ($0 K$, or $-273'15ºC$). At absolute zero a system reaches its lowest possible energy state. Systems' random motion in the zero-point energy never vanishes  because of the uncertainty principle (retaining always some kinetic energy, even at the lowest temperature).

> [!abstract]+ Thermal energy
> The thermal energy refers to the internal energy present (stored) in a system due to its temperature, hence associated to the random motion of the gas molecules. 

> [!abstract]+ Heat ($Q$)
> Heat is any spontaneous flow of energy (transfer), from one object to another, caused by a difference in temperature between the objects.
> 
> The transfer can be realized fundamentally by conduction, convection or/and radiation.
>

> [!abstract]+ Equation of state
> An equation of state would be any proposed relation between $P$, $V$ and $T$ (substance's state variables, which only depend on the equilibrium state of the system).
 
> [!example] Ideal gas law
> $$\large PV=nRT$$
> 
> with $P$ as pressure, $V$ as volume, $n$ as number of moles, $R=8.31 \frac{J}{mol·K}$ and $T$ as temperature.
>> [!note]- Assumptions
>> 
>> · Molecules are point particles
>> 
>> · There are no intermolecular forces
>> 
>> · All collisions are elastic
>> 
>> · Large intermolecular spacing
>> 
>> · Low density
>
> Fails at lower temperatures or higher pressures (we must count the intermolecular forces and the molecular size).


## 3. Entropy and irreversibility

### Entropy

Entropy tells us why energy spreads out, why some processes happen on their own, and why others do not.

We can define entropy as:
- The measure of the number of microstates in a macrostate (number of ways in which a system may be arranged).
- The amount of additional information needed to specify the exact physical state of a system.

It depends only on the final and initial state (path independent).

>[!example] Entropy
>
>$$\large S=-k_B\ln\Omega$$
>
>with $k_B$ as the Boltzmann's constant with $k_B=1'38065·10^{23} \; \frac{J}{K}$ and $\Omega=\begin{pmatrix} N\\n \end{pmatrix}$ as the number of microstates $n$ in each macrostate $N$ (combinatorics). 
>
>May be interesting to know Stirling's approximation: $\ln (x!) \approx x \ln (x)-x$
>>[!example]- Gibbs entropy (includes non-equilibrium)
>>
>>$$ S=-k_B \sum_i p_i \ln p_i$$
>>
>>with $\sum_i p_i \ln p_i$ as the sum of all possible microstates and their probabilities.


> [!abstract] Reversible process
>  A process that operates at equilibrium, where the entropy of the total idolated system is not changing $\Delta S=0$ (without increasing the heat-temperature ratio).
>  
>  The system returns to its original state (although, in practice, a perfect reversible process is not possible, heat cannot fully be converted to work and will always be lost to some degree).
>  
>  $$dS=\frac{\delta Q_{rev}}{T}$$
>  

>[!abstract] Irreversible process
>A process that is not fully capable to return to its inital state, without expenditure of energy or restoring the environment to its own initial conditions.
>
>It generates entropy, due to friction, turbulences, spontaneous expansions...
>
> $$dS>\frac{\delta Q_{rev}}{T}$$

Related to this, we can discuss the heat flow. The heat flow increases disorder, hence the total entropy increases, moving it toward some more probable, balanced state. The heat flows from a hot to a cold reservoir statistically likely, spreading out energy and increasing entropy, occupying more microstates).

>[!abstract] Dissipation
>Result of an irreversible process in homogeneous thermodynamics systems, due to the conversion of energy into heat ($E_{mec_0}>E_{mec_f}$).
>
>Heat transfer is dissipative (entropy varies with temperature) and they also include also the friction and similar forces that lead into decoherency of energy.

### Internal energy

The internal energy is the total microscopic energy stored inside a system (the random motion of its particles plus the energy in the forces between them).

$$ \Delta U=Q -W$$

with heat $Q$ and the work $W$.

We will revisit this concept more in-depth in section 5, as the **first law of thermodynamics*.

## 4. Ensembles and Boltzmann statistics
### Maxwell-Boltzmann statistics

By assumption, the combined system is isolated, so all microstates are equally probable.

 $$ \frac{P(s1)}{P(s2)}=\frac{\Omega_R (s1)}{\Omega_R(s2)} $$
 
 $Ω(s_i)$ describes the number of microstates available to the reservoir for each state $s_i$, and $P(s_i)$ as the probability that our system is in state $s_i$.



(Partition function?)!!!!!


 
 $$ \langle N_i \rangle = \frac{g_i}{e^{-(\epsilon_i - \mu)/kT}}= \frac{N}{Z} g_i c^{-\epsilon_i/kT}$$
 
 with $Z=\sum_i g_i e^{-\epsilon_i / kT}$ as the partition function.
 
### Ensembles

The ensembles are a study of thermodynamics concerned with systems which behave "static" (despite the motion of its internal parts) and can be described simply by macroscopically observable variables.

>[!abstract]- Probability density function
>An ensemble is represented by a joint probability density function:
>
>  $$ \rho (p_1, ..., p_n, q_1, ... , q_n)$$
>  
>  defined over the system's phase space, with $n$ general coordinates $q_1, ... , q_n$ and $n$ associated canonical momenta $p_1, ... , p_n$.
>  

A statistical ensemble describes the probability distribution for the state of a system.

Although a mechanical system evolves over time, an ensemble does not necessarily have to evolve (it won't evolve if it equally contains all past and future phases of the system, in statistical equilibrium).

>[!abstract]- Microcanonical ensemble (N, V, E)
>
The *microcanonical ensemble* is used to represent the possible states of a mechanical system which has an exactly specified total energy, and all microstates are equally probable ($P=\frac{1}{\Omega}$). 
>
>It is an isolated system with conservation of energy, and depends on the macroscopic variables N, V and E (total number of particles, volume and total energy in system, respectively). 
>
>![[Screenshot 2026-07-02 222905.png|450]]

>[!abstract]- Canonical ensemble (N, V, T)
>
The *canonical ensemble* is a theoretical collection of identical, non-interacting systems, regulated by thermal equilibrium with a heat bath.
>
>It is derived from the microcanonical ensemble, when a small system is part of a much larger, isolated system (microcanonical). In the limit of a large system (thermodynamic limit), the probability distribution of energy takes the form of the exponential function of Boltzmann's distribution ($P=e^{\frac{F-E}{kT}}$, with $F= U-TS$ as the Helmholtz free energy)
>
>The system can exchange energy with the heat bath, the states of the system will differ in total energy, and it depends on the macroscopic variables N, V and T.
>
>![[Screenshot 2026-07-02 222845.png|450]]

>[!abstract]- Grand canonical ensemble ($\mu$, V, T)
The *grand canonical ensemble* represents all possible states of particles maintained in thermodynamic equilibrium (thermal and chemical) with a reservoir. 
>
>The system is open, hence the system can exchange energy and particles with a reservoir. It depends on the macroscopic variables $\mu$, V, T.
>
>![[Screenshot 2026-07-02 222845 1.png|450]]
>

### Free energy 

The free energy determines the spontaneity of processes and the maximum useful work at constant $T$, as the internal energy $U$ doesn't account lose to heat.

>[!multi-column] Free energy
> 
> >[!example]+ Helmholtz free energy (constant V)
> >  
> >  $$ F=U-TS$$
> > 
> 
> >[!example]+ Gibbs free energy (constant P)
> >
> > $$G=H-TS$$
> > 
> > with $H=U+PV$


>[!example]- Barometric formula
>It shows how the pressure or the density of the air changes with altitude.
>
>$$P=\frac{\rho R^* T}{M}$$
>$$P=P_0 e^{-\frac{Mgz}{R^*T}}$$
>
>with $M$ as the molar mass of Earth's air, $R^*$ as the universal gas constant for air ($R^* =8'3144598 \frac{N·m}{mol·K}$) and $z$ as the altitude.
>


### Chemical potential

Form of a potential energy that can be absorbed or released during a chemical reaction, a phase transition and a change in the number of moles of a species.

- In the chemical equilibrium, the total sum of chemical potential equals zero, due to the free energy being at its minimum.
- Particles tend to move from higher to lower chemical potentials.

$$
\large dU=TdS-PdV+\sum_{i=1}^n \mu_i dN_i
$$

with $\mu_i=(\frac{\partial U}{\partial N_i})_{S,V,N_{j\neq i}}$ .



///
(Partition function, little section of quantum statistics??(Lecture 7)-- look at homeworks to decide)

## 5. Laws of thermodynamics

### Laws of thermodynamics

#### Zeroth law of thermodynamics
If two systems are in thermal equilibrium independently with a third system, they must be in thermal equilibrium with each other. 

$$T_1=T_2 \; , \;T_2=T_3 \; \Rightarrow \; T_1=T_3$$

It justifies the use of suitable thermodynamic systems as thermometers.

#### First law of thermodynamics
When energy passes, as work, as heat, or with matter, into or out from a system, its internal energy changes in accord with the law of conservation of energy.  

$$U= \text{const}\; \Leftrightarrow \; W_1+Q_1=W_2+Q_2$$
with $W$ as the work *on* the system and heat $Q$.

$$\Delta U=Q-W$$

with heat $Q$ and $W$ as the work *done by the system*.

>[!example]+ Internal energy for infinitesimal processes
>We can also express it for infinitesimal processes as:
>
>$$ dU=\delta Q+\delta W=\begin{bmatrix} \delta Q=TdS\\\delta W=PdV\end{bmatrix}=TdS-PdV$$
>
>To this formula we can also add the expression $\sum_i \mu_i dN_i$ for a closed system in which the particles are of different types $i$, with $\mu_i$ as the chemical potential for type-$i$ particles and $dN_i$ as the small increase in the amount of type-$i$ particles.

>[!abstract]- Proportionality Q - W
> 
> $$Q=AW$$
> 
> with mechanical equivalent of heat $A=4'186 \frac{J}{cal}$ .

#### Second law of thermodynamics
In a natural thermodynamic process, the sum of the entropies of the interacting thermodynamic systems increases (see **reversible and irreversible processes** in section 3). 

$$\Delta S \geq 0 \; \rightarrow \;  \left\{ \begin{array}{cl}
\text{reversible} & , \ \text{if } \Delta S = 0 \\
\text{irreversible} & , \ \text{if }\Delta S > 0
\end{array} \right.$$

An isolated system evolves toward equilibrium by increasing entropy (equilibrium $\Leftrightarrow$ maximum entropy).

#### Third law of thermodynamics
The entropy of a system approaches a constant value as the temperature approaches absolute zero. The entropy of a system at absolute zero is typically close to zero.

$$ T=0 \; \Rightarrow \; E_{kin}=0$$

![[Screenshot 2026-07-03 003944.png|200]]


### Thermodynamic potentials

A thermodynamic potential is a scalar quantity that represents the thermodynamic state.

| Potential             | Definition                       | Natural variables |
| --------------------- | -------------------------------- | ----------------- |
| Internal energy       | $U=\int (TdS-PdV)$               | S, V, N           |
| Helmholtz free energy | $F=U-TS$                         | T, V, N           |
| Enthalpy              | $H=U+PV$                         | S, P, N           |
| Gibbs free energy     | $G=U+PV-TS$                      | T,P, N            |
#### Principle of minimal energy
For closed systems:
- $S$=const, $\text{external parameters}$=const $\Rightarrow$ $U$ minimal at equilibrium.
- $T$=const, $\text{external parameters}$=const $\Rightarrow$ $F$ minimal at equilibrium.
- $P$=const, $\text{external parameters}$=const $\Rightarrow$ $H$ minimal at equilibrium.
- $T$=const, $P$=const, $\text{external parameters}$=const $\Rightarrow$ $G$ minimal at equilibrium.

#### Fundamental thermodynamic relations
> [!multi-column] Infinitesimal expressions for thermodynamic potentials
>>[!example]- Internal energy
>>
>>$$dU=TdS-PdV+\sum_idN_i$$
>
>
>>[!example]- Helmholtz free energy
>>
>>$$dF=-SdT-PdV+\sum_idN_i$$
>
>
>>[!example]- Enthalpy
>>
>>$$dH=TdS-VdP+\sum_idN_i$$
>
>
>>[!example]- Gibbs free energy
>>
>>$$dG=-SdT+VdP+\sum_idN_i$$
>>



////
(243-244)
Fundamental thermodynamic relation

## 6. Heat engines and efficiency
(diap 250-309)
Thermodynamic cycles
Thermodynamic processes
Carnot cycle
(Temperature-entropy diagram?)
Engine efficiency (thermal efficiency)
Carnot's theorem
Stirling cycle
Refrigerator and heat pump

## 7. Thermal conduction and heat capacity
(diap 311-326 (lecture9), lecture 10 )
Heat transfer
	Advection
	Convection
	Conduction: Fourier's law (law of heat conduction)
	Radiation (thermal, black-body)
Thermal energy
Heat capacity (also in many slides after equipartition th.)
Equipartition theorem
Thermal expansion
Dulong-Petit law

## 8. Phase transitions and real gases
(lecture 10, lecture 11)
Phase transitions
Thermodynamic surfaces
Classification
Latent heat

>[!example] Van der Waals equation
> $$(P+\frac{an^2}{V^2})(V-nb^2)=nRT$$
> 
>with $a$ and $b$ as constants, they correct pressure and volume, respectively. 
>
>This equation works as a corrected model for real gases (adding new terms for molecular size and intermolecular attractions).

(little more explanation on Van der Waals eq., graphic representation?)

## 9. Brownian motors and entropic forces
(Lecture 11, lecture 12)
Feynman's thermal ratchet
Brownian motor
Entropic elasticity
Entropical forces

(more equipartition theorem??)
	Energies
	Harmonic oscillator
	Brownian motion
	Maxwell-Boltzmann distribution ([[Kinetic theory of gases]])
	General formulation
Bending stiffness

> [!multi-column] Expansion coefficients
>
>
>>[!example]+ Thermal expansion coefficient
>>
>>$$\beta = \frac{\frac{\Delta V}{V}}{\Delta T}$$
>
>>[!example]+ Linear thermal expansion coefficient
>>
 >>$$\alpha = \frac{\frac{\Delta L}{L}}{\Delta T}$$

Fluctuation-dissipation theorem




[[Interesting experiments in thermodynamics]]
