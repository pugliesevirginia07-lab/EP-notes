# Chapter 2 : Thermodynamics

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
>> $$P(X=x)= \begin{pmatrix} n \\X \end{pmatrix}p^X(1-p)^{n-K}$$
>>
>>With the combinatorial $\frac{n!}{X!(n-X)!}$ We can also get the probability for an interval of successes ($X\leq x$ or $X\geq x$). 
>
>
>> [!abstract]- Gaussian distribution
>> When we have a large $n$ ($n, \ np, \ nq \gg 1$, with $q=(1-p)$), the binomial distribution approximates to a Gaussian:
>>  $$ P(X)=\frac{1}{\sqrt{2 \pi np}}e^{-\frac{(X-np)^2}{2npq}}$$
>>  
>> $$ P(x)=\frac{1}{\sqrt{2\pi \sigma^2}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
>> With mean $\mu$ and variance $\sigma^2$.
>> 
>> ![[Pasted image 20260622234102.png|200]]

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
>>$$W(t+\Delta t)-W(t) \sim N(0, \Delta t)$$
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
>![[Pasted image 20260623005944.png]]
>>[!abstract]- Normal diffusion
>> It corresponds to a Brownian motion, with $\alpha =1$.
>> 
>> $$\langle r^2(t)\rangle=2Dt$$ 
>
>> [!abstract]- Subdiffusion
>> The particles spread slower than Brownian motion, with $\alpha<1$.
>> 
>
>>[!abstract]- Superdiffusion
>> The particles spreads faster than Brownian motion, with $\alpha>1$.
>
>>[!abstract]- Corralled motion
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
>>[!example]+ Fick's first law
>>
>> Flux goes from regions of high concentration to regions of low concentration.
>> 
>> $$J=-D \frac{\partial{\phi}}{\partial{x}}$$
>> 
>> with diffusion coefficient $D$ and concentration $\phi$.
>
>
>>[!example]+ Fick's second law
>> Shows how diffusion causes the concentration field to change with time $t$.
>> 
>> $$\frac{\partial\phi}{\partial t}=D\frac{\partial^2\phi}{\partial x^2}$$
>> 

The diffusion coefficient $D$ measures how quickly the particles spread, for large $D$, the particles spread rapidly, and vice versa.

>[!example] Einstein-Stokes equation
>
> $$D=\frac{k_BT}{6\pi\eta R}$$
> with viscosity coefficient $\eta$ and particle radius' $R$.
>
> The momentum relaxation time would correspond to 
> $$\tau =\frac{m}{\gamma}$$
> · For $t \ll \tau$: the particles still have some initial velocity, they follow a corralled motion.
> · For $t \gg \tau$: the motion becomes diffusive (Brownian motion).

### Microstates, macrostates and phase space

- A **microstate** describes a system specifying the properties of each individual particle.
- A **macrostate** is the probability distribution of possible states across a certain statistical ensemble of all microstates. Described in terms of macroscopic quantities (such as $P$ or $V$). Two systems with the same values of macroscopic parameters are thermodynamically indistinguishable. A macrostate tells us nothing about a state of an individual particle, each macrostate contains a large number of microstates.

- A **phase space** is a space where all possible states of a system are represented, each possible state corresponds to one unique point. Every degree of freedom of the system is represented as an axis of a multidimensional space, such as in the phase space trajectory (relating position and velocity).

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

From the [[kinetic theory of gases]], the absolute temperature of a gas is proportional to the average translational kinetic energy of its molecules, the Boltzmann's constant is the conversion factor between these two.

The coldest theoretical temperature is absolute zero ($0 K$, or $-273'15ºC$). At absolute zero a system reaches its lowest possible energy state. Systems' random motion in the zero-point energy never vanishes  because of the uncertainty principle (retaining always some kinetic energy, even at the lowest temperature).

> [!abstract]+ Thermal energy
> The thermal energy refers to the internal energy present in a system due to its temperature, hence associated to the random motion of the gas molecules. 

> [!abstract]+ Heat ($Q$)
> Heat is any spontaneous flow of energy, from one object to another, caused by a difference in temperature between the objects.
> 
> The transfer can be realized fundamentally by conduction, convection or/and radiation.
>

> [!abstract]+ Equation of state
> An equation of state would be any proposed relation between $P$, $V$ and $T$ (substance's state variables, which only depend on the equilibrium state of the system).

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

> [!abstract] Reversible process
>  (CONTINUE FROM HERE)

(179-182, 196-206, 245-246)
Reversibility of processes 
Reversible process
Irreversible process
Dissipation (also in diap. 245 and 246!!)

Entropy (Gibbs, includes non-equilibrium) definition 
$$S=k_B \; ln (\Omega)$$
(Thermodynamic definition for entropy in terms of heat and temperature)
$$dS=\frac{\delta Q_{rev}}{T}$$
Heat flow increases disorder, hence increases total entropy, moving it toward some more probable state.

## 4. Ensembles and Boltzmann statistics
(diap 208-235+ lecture 7)
Ensembles
Microcanonical ensemble
(Probability density function?)
Maxwell-Boltzmann statistics
Canonical ensemble
Partition function
Barometric formula (exponential atmosphere)
Grand canonical ensemble
Free energy (Gibbs, Helmholtz)
(Chemical potential? )

(Little section of quantum statistics??(Lecture 7))

## 5. Laws of thermodynamics
(lecture 7+238-244)
Laws of thermodynamics
- $T_1=T_2 \quad \quad T_2=T_3$
- $E=constant$
- $\Delta S \geq 0$ 
- $T=0 \rightarrow E_{kin}=0$

Thermodynamic potential (internal energy, Helmholtz free energy, enthalpy, Gibbs free energy and grand potential)
Principle of minimal energy
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
Fluctuation-dissipation theorem




[[Interesting experiments in thermodynamics]]
