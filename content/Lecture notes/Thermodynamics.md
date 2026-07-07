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
>  The **relaxation time** is the time required for a system to reach the thermal equilibrium.
>  
>  We assume the system is isolated, the energy stays inside of the system and it has unlimited time to reach the thermal equilibrium.

>[!abstract]+ Temperature ($T$)
>The **temperature** is a measure of the tendency of an object to spontaneously give up energy to its surroundings.
>
>When two objects are in thermal contact, the hotter object tends to transfer energy to the colder one.
>

From the [[kinetic theory of gases]], the absolute temperature of a gas is proportional to the average translational kinetic energy of its molecules, the Boltzmann's constant is the conversion factor between these two.

The coldest theoretical temperature is absolute zero ($0 K$, or $-273'15ºC$). At absolute zero a system reaches its lowest possible energy state, even though the systems' random motion in the zero-point energy never vanishes  because of the uncertainty principle (retaining always some kinetic energy, even at the lowest temperature).

> [!abstract]+ Thermal energy
> The **thermal energy** refers to the internal energy present (stored) in a system due to its temperature, hence associated to the random motion of the gas molecules. 

> [!abstract]+ Heat ($Q$)
> The **heat** is any spontaneous flow of energy (transfer), from one object to another, caused by a difference in temperature between the objects.
> 
> The transfer can be realized fundamentally by conduction, convection or/and radiation.
>

> [!abstract]+ Equation of state
> An **equation of state** would be any proposed relation between $P$, $V$ and $T$ (substance's state variables, which only depend on the equilibrium state of the system).
 
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
> Fails at lower temperatures or higher pressures (we must count the intermolecular forces and the molecular size, and use Van der Waals equation).
> 
>> [!example] Internal energy for an ideal gas
> >
>  >$$U=\frac 3 2 k_B\ T$$
>  >
> 

## 3. Entropy and irreversibility

### Entropy

The **entropy** tells us why energy spreads out, why some processes happen on their own, and why others do not.

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
>May be interesting to know Stirling's approximation: $\ln (x!) \approx x \ln (x)-x$ (homework -, exercise -).
>>[!example]- Gibbs entropy (includes non-equilibrium)
>>
>>$$ S=-k_B \sum_i p_i \ln p_i$$
>>
>>with $\sum_i p_i \ln p_i$ as the sum of all possible microstates and their probabilities.

> [!abstract]+ Reversible process
>  A process that operates at equilibrium, where the **entropy** of the total idolated system is **not changing** $\Delta S=0$ (without increasing the heat-temperature ratio).
>  
>  The system **returns to its original state** (although, in practice, a perfect reversible process is not possible, heat cannot fully be converted to work and will always be lost to some degree).
>  
>  $$dS=\frac{\delta Q_{rev}}{T}$$
>  

>[!abstract]+ Irreversible process
>A process that is **not fully capable to return to its inital state**, without expenditure of energy or restoring the environment to its own initial conditions.
>
>It **generates entropy**, due to friction, turbulences, spontaneous expansions...
>
> $$dS>\frac{\delta Q_{rev}}{T}$$

Related to this, we can discuss the heat flow. The **heat flow** increases disorder, hence the **total entropy increases**, moving it toward some more probable, balanced state. The heat flows from a hot to a cold reservoir statistically likely, spreading out energy and increasing entropy, occupying more microstates).

>[!abstract] Dissipation
>Result of an irreversible process in homogeneous thermodynamics systems, due to the conversion of energy into heat ($E_{mec_0}>E_{mec_f}$).
>
>**Heat transfer is dissipative** (entropy varies with temperature) and they also include also the friction and similar forces that lead into decoherency of energy.

(See [[Energy minimum - Entropy maximum principles]]).

### Internal energy

The **internal energy** is the total microscopic energy stored inside a system (the random motion of its particles plus the energy in the forces between them).

>[!example] Internal energy
>
>$$ \Delta U=Q -W$$
>
>with heat $Q$ and the work $W$.

We will revisit this concept more in-depth in section 5, as the *first law of thermodynamics*.


## 4. Ensembles and Boltzmann statistics
### Maxwell-Boltzmann statistics

By assumption, the combined system is isolated, so all microstates are equally probable.

 $$ \frac{P(s1)}{P(s2)}=\frac{\Omega_R (s1)}{\Omega_R(s2)} $$
 
 $Ω(s_i)$ describes the number of microstates available to the reservoir for each state $s_i$, and $P(s_i)$ as the probability that our system is in state $s_i$.

 
 $$ \langle N_i \rangle = \frac{g_i}{e^{-(\epsilon_i - \mu)/kT}}= \frac{N}{Z} g_i c^{-\epsilon_i/kT}$$
 
 with $Z=\sum_i g_i e^{-\epsilon_i / kT}$ as the partition function (see [[Equipartition theorem and partition function]]).
 
### Ensembles

The **ensembles** are a study of thermodynamics concerned with systems which behave "static" (despite the motion of its internal parts) and can be described simply by macroscopically observable variables.

>[!abstract]- Probability density function
>An ensemble is represented by a joint probability density function:
>
>  $$ \rho (p_1, ..., p_n, q_1, ... , q_n)$$
>  
>  defined over the system's phase space, with $n$ general coordinates $q_1, ... , q_n$ and $n$ associated canonical momenta $p_1, ... , p_n$.
>  

A statistical ensemble describes the probability distribution for the state of a system.

Although a mechanical system evolves over time, an **ensemble does not necessarily have to evolve** (it won't evolve if it equally contains all past and future phases of the system, in statistical equilibrium).

>[!abstract]- Microcanonical ensemble (N, V, E)
>
>The **microcanonical ensemble** is used to represent the possible states of a mechanical system which has an exactly specified total energy, and all microstates are equally probable ($P=\frac{1}{\Omega}$). 
>
>It is an isolated system with conservation of energy, and depends on the macroscopic variables N, V and E (total number of particles, volume and total energy in system, respectively). 
>
>![[Microcanonical ensemble.png|450]]

>[!abstract]- Canonical ensemble (N, V, T)
>
>The **canonical ensemble** is a theoretical collection of identical, non-interacting systems, regulated by thermal equilibrium with a heat bath.
>
>It is derived from the microcanonical ensemble, when a small system is part of a much larger, isolated system (microcanonical). In the limit of a large system (thermodynamic limit), the probability distribution of energy takes the form of the exponential function of Boltzmann's distribution ($P=e^{\frac{F-E}{kT}}$, with $F= U-TS$ as the Helmholtz free energy)
>
>The system can exchange energy with the heat bath, the states of the system will differ in total energy, and it depends on the macroscopic variables N, V and T.
>
>![[Canonical ensemble.png|450]]

>[!abstract]- Grand canonical ensemble ($\mu$, V, T)
>The **grand canonical ensemble** represents all possible states of particles maintained in thermodynamic equilibrium (thermal and chemical) with a reservoir. 
>
>The system is open, hence the system can exchange energy and particles with a reservoir. It depends on the macroscopic variables $\mu$, V, T.
>
>![[Grand canonical ensemble.jpg|450]]
>

### Free energy 

The **free energy** determines the spontaneity of processes and the maximum useful work at constant $T$, as the internal energy $U$ doesn't account lose to heat.

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


>[!abstract] Barometric formula
>It shows how the pressure or the density of the air changes with altitude.
>
>$$P=\frac{\rho R^* T}{M}$$
>
>$$P=P_0 e^{-\frac{Mgz}{R^*T}}$$
>
>with $M$ as the molar mass of Earth's air, $R^*$ as the universal gas constant for air ($R^* =8'3144598 \frac{N·m}{mol·K}$) and $z$ as the altitude.
>


### Chemical potential

It is a **form of a potential energy** that can be absorbed or released during a chemical reaction, a phase transition and a change in the number of moles of a species.

- In the chemical equilibrium, the total sum of chemical potential equals zero, due to the free energy being at its minimum.
- Particles tend to move from higher to lower chemical potentials.

$$
\large dU=TdS-PdV+\sum_{i=1}^n \mu_i dN_i
$$

with $\mu_i=(\frac{\partial U}{\partial N_i})_{S,V,N_{j\neq i}}$ as the chemical potential.


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

>[!abstract]- Proportionality $Q$ - $W$
> 
> $$Q=AW$$
> 
> with mechanical equivalent of heat $A=4'186 \frac{J}{cal}$ .

#### Second law of thermodynamics
In a natural thermodynamic process, the sum of the entropies of the interacting thermodynamic systems increases (see *reversible and irreversible processes* in section 3). 

It is bigger or equal to 0 if we consider no heat transfer.

$$\Delta S \geq 0 \; \rightarrow \;  \left\{ \begin{array}{cl} \text{reversible} & ,\ \text{if } \Delta S = 0 \\\text{irreversible} & , \ \text{if }\Delta S > 0 \end{array} \right.$$

An isolated system evolves toward equilibrium by increasing entropy (equilibrium $\Leftrightarrow$ maximum entropy : [[Energy minimum - Entropy maximum principles]]).

#### Third law of thermodynamics
The entropy of a system approaches a constant value as the temperature approaches absolute zero. The entropy of a system at absolute zero is typically close to zero (although, in practice, it is not possible to have 0 kinetic energy in absolute zero (see *temperature* in section 2)).

$$ T=0 \; \Rightarrow \; E_{kin}=0$$

![[Absolute zero.png|200]]


### Thermodynamic potentials

A **thermodynamic potential** is a scalar quantity that represents the thermodynamic state.

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
>>[!example]+ Internal energy
>>
>>$$dU=TdS-PdV+\sum_idN_i$$
>
>
>>[!example]+ Helmholtz free energy
>>
>>$$dF=-SdT-PdV+\sum_idN_i$$
>
>
>>[!example]+ Enthalpy
>>
>>$$dH=TdS-VdP+\sum_idN_i$$
>
>
>>[!example]+ Gibbs free energy
>>
>>$$dG=-SdT+VdP+\sum_idN_i$$
>>


### Fundamental thermodynamic relations

| Potential | Differential  | Partial derivatives                                                                                         |
| --------- | ------------- | ----------------------------------------------------------------------------------------------------------- |
| $U(S,V)$  | $dU=TdS-PdV$  | $$T=\left(\frac{\partial U}{\partial S}\right)_V \; ,\; P=-\left(\frac{\partial U}{\partial V}\right)_S$$   |
| $H(S,P)$  | $dH=TdS+VdP$  | $$T=\left(\frac{\partial H}{\partial S}\right)_P \; ,\; V=\left(\frac{\partial H}{\partial p}\right)_S$$    |
| $F(T,V)$  | $dF=-SdT-PdV$ | $$S=-\left(\frac{\partial F}{\partial T}\right)_V \; , \; P=-\left(\frac{\partial F}{\partial V}\right)_T$$ |
| $G(T,P)$  | $dG=-SdT+VdP$ | $$S=-\left(\frac{\partial G}{\partial T}\right)_P\; , \; V=\left(\frac{\partial G}{\partial p}\right)_T$$   |


## 6. Heat engines and efficiency

### Thermodynamic cycles

A **thermodynamic cycle** is a close sequence of thermodynamic processes involving transfer of heat and work (into and out of the system), while varying the pressure, the temperature and other state variables.

- *Heat engine*: the working substance may convert heat from a warm source into work, disposing the remaining heat to a cold sink.
- *Heat pump*: the cycle may be reversed and we use work to move heat from a cold source and transfer it to a warm sink.

#### (Ideal) Quasistatic cycle
The net variation in the state properties during a thermodynamic cycle is zero ($\Delta E=E_{out}-E_{in}=0$), forming a closed loop on a PV diagram.

![[Thermodynamic processes (basic).png|250]]

The area enclosed by the closed loop is the work done by the process:

$$W=\oint PdV=Q=Q_{in}-Q_{out}$$

- If the cyclic process moves clockwise: positive $W$ (heat engine).
- If the cyclic process moves counterclockwise: negative $W$ (heat pump).
#### Types of thermodynamic processes
- **Isobaric process**: constant pressure $P$.
- **Isochoric process**: constant volume $V$.
- **Isothermal process**: constant temperature $T$.
- **Adiabatic process**: no transfer of heat between the system and its surroundings.
	- Adiabatic wall: does not allow heat flow.
	- Diathermic wall: allows heat flow

A good way to visualize these processes are with PV diagrams, which can be different for different thermodynamic processes, but we will see an example with the Carnot cycle.

### Carnot cycle

The Carnot cycle is a theoretical construct of a "perfect" engine and defines the theoretical limit on efficiency (which will be commented later on).

>[!multi-column] Quasistatic cycle for the Carnot engine
>>[!abstract] Visualization of the Carnot cycle
>>
>> ![[Carnot engine visualization.png|300]]
>
>>[!abstract] PV-diagram for the Carnot cycle
>>
>>![[PV-diagram Carnot cycle.png|300]]

(See [[Carnot cycle diagram explanation]]).

### Engine efficiency

The **engine efficiency** is the ratio of useful work output to total heat energy input.

>[!example] Efficiency
>$$ \eta= \frac{W}{Q_H}$$
>
>with work $W$ and heat energy entering the system $Q_H$.
>
>From the first law of thermodynamics: $0 \leq \eta <1$.

- **Thermal efficiency**: percentage of fuel heat energy converted to mechanical work.
- **Combustion efficiency**: efficiency of converting fuel into heat (often 100% in good conditions).

Electric motors have a higher efficiency than heat engines or internal combustion engines. They use electromagnetism and bypass losses associated with the fuel combustion and thermodynamics.

>[!abstract] Carnot's theorem
> Every reversible heat engine operating between a pair of heat reservoirs is equally efficient (it'll depend only on the temperatures of the hot and cold reservoirs), due to the second law of thermodynamics.
> 
> $$\eta=1-\frac{T_C}{T_H}$$
> 
> with temperature in the cold reservoir $T_C$ and in the hot reservoir $T_H$.
>
>![[Heat engine.png|350]]

#### Refrigerator and heat pump
A heat engine run in reverse is a **refrigerator and heat pump**, the work is done to move the heat from the cold-temperature source to the hot-temperature sink. 

When the liquid refrigerant at a low temperature and low pressure passes through the outdoor heat exchanger, ambient heat causes the liquid to change to gas, the gas is then compressed using an electric pump; the compression increases the temperature of the gas.

![[Vapor-compresion refrigeration.png|350]]

Coefficient of performance: equivalent to the engine efficiency, when the COP is high, the efficiency is also high.

$$COP=\frac{|Q_{provided}|}{W_{required}}$$


## 7. Thermal conduction and heat capacity

### Heat transfer

The fundamental modes of the heat transfer: 
#### Advection/Convection
The transport of a fluid/gas from one location to another, and dependent on the motion of that fluid/gas. It is the most efficient way of heat transfer

#### Conduction
The transfer of energy between objects that are in physical contact. Thermal conductivity is the property of a material to conduct heat which is described by Fourier's Law for heat conduction. 

>[!abstract]- Rayleigh-Bénard convection
>  The fluid develops a regular pattern of convection cells known as **Bénard cells**.
>  
>  ![[Rayleigh-Bénard convection.png|300]]
>  
>   Gravity acts trying to pull the cooler, denser liquid from the top to the bottom. This gravitational force is opposed by the viscous damping force in the fluid.

The **thermal conduction** is the transfer of heat by microscopic collisions of particles within a body. The conduction takes place in all phases of matter.

#### Radiation
The transfer of energy by the emission of electromagnetic radiation, generated by the thermal motion of charged particles in matter. All matter with a temperature greater than absolute zero emits thermal radiation.

When $T>0$ : the interatomic collisions cause kinetic energy of the atoms or molecules to change, this results in charge-acceleration and/or dipole oscillation, producing EM radiation.

(See [[Black-body radiation]]).

### Thermal energy

The **thermal energy** is a part of the total kinetic energy of an object or sample of matter that results in the system temperature, as a consequence of absorbing heat.

Some of the thermal energy is stored in atomic vibration and stored equally partitioned ([[Equipartition theorem and partition function]]) between potential energy and kinetic energy of atomic vibration.

#### Heat capacity

The **heat capacity** is the thermal energy of a system $U$ at a given $T$ is related proportionally to its heat capacity $C(T)$:

$$\large U_{thermal}=C(T)·T$$


We treat the vibrations of the atomic lattice (heat) as [[Phonons]] in a box. Debye model treats atomic vibrations as phonons in a box of length L using: $\lambda_n=\frac{2L}n$ , and the energy of a phonon is

$$E_n=h \nu_n= \frac{h \ c_s}{\lambda_n}=\frac{h\ c_s\ n}{2L}$$   

>[!abstract]- Dulong-Petit law
> The heat capacity of a mole of many solid elements is about 3R
> 
> $$\frac C N =3R$$
> 
> with $C$ for the total heat capacity, number of moles $N$ and the universal gas constant $R$.

>[!example] Heat capacities
>
> We can use the heat capacity to relate the thermodynamic relations we have seen previously ($dU=\delta Q- \delta W$ and $dU=\delta Q -PdV$, among others):
>
>$$C(T)=\frac{\delta Q}{\delta T}$$
>
>>[!abstract]- Constant volume
>>
>>$$\left( \frac{\partial U}{\partial T} \right)_V=\left( \frac{\partial Q}{\partial T} \right)_V=C_V= T \left( \frac{\partial S}{\partial T} \right)_V$$
>
>
>>[!abstract]- Constant pressure
>>
>> $$\left( \frac{\partial H}{\partial T} \right)_P=\left( \frac{\partial Q}{\partial T} \right)_P=C_P=T\left( \frac{\partial S}{\partial T} \right)_P$$
>>
>> with $H=U+PV \rightarrow dH=\delta Q+VdP$ as the enthalpy of the system.
>

>[!abstract] Relations between heat capacities
> 
>$$C_P-C_V=VT\frac{\alpha^2}{\beta_T}$$
>
>$$\frac{C_P}{C_V}=\frac{\beta_T}{\beta_S}$$
>
>>[!abstract]+ Coefficients
>>
>> · Thermal expansion coefficient: $\alpha=\frac 1 V \left(\frac{\partial V}{\partial T}\right)_P$
> >
>> · Isothermal compressibility: $\beta_T=-\frac 1 V \left(\frac{\partial V}{\partial P}\right)_T$
>> 
>> · Isentropic compressibility: $\beta_S=-\frac 1 V \left(\frac{\partial V}{\partial P}\right)_S$

### Thermal expansion

The thermal expansion is related to the asymmetric (anharmonic) shape of the interatomic potential. If the interatomic potential is symmetric (harmonic), the average value of interatomic separation does not change, hence there is no thermal expansion.

![[Interatomic potential.png|500]]


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


## 8. Phase transitions and real gases

### Phase transitions

A phase of a thermodynamic system and the states of matter have uniform defined physical properties. Everywhere inside the material, the particles behave in the same way and have the same overall structure.

During a **phase transition** properties of the medium change, often discontinuously, as a result of the change of some external condition, such as temperature $T$, pressure $P$, among others.

>[!abstract] Phase diagram of a substance
>![[Phase transition diagram.png|350]]
>
 > · The dotted lines represent the anomalous behavior of the substance.
 > 
 > · The **triple point** of a substance is the temperature and pressure at which the three phases (gas, liquid, and solid) of the substance coexist in thermodynamic equilibrium. 
 > 
 > · The **critical point** is the end point of a phase equilibrium curve.
 > 
 > · The **end point** of the pressure-temperature curve that designates conditions under which a liquid and its vapor can coexist.

(See [[Fundamental states of matter]]).

#### Thermodynamic surfaces
The **thermodynamic surfaces** are three-dimensional diagrams that describe every equilibrium point of a pure substance.

>[!multi-column] Types of thermodynamic surfaces
>>[!abstract] Pressure - volume - temperature (P-V-T) surfaces
>>
>> ![[P-V-T surface.png|300]]
>
>>[!abstract] Temperature - entropy - pressure (T-S-P) surfaces
>>
>> ![[T-P-E surface.png|300]]
>> 

>[!abstract] Latent heat
>The latent heat is the heat released or absorbed by a thermodynamic system during a constant-temperature process.

>[!multi-column] Classification
>>[!info]- Ehrenfest classification
>>
>> · *First-order phase transitions*: discontinuity in the first derivative of the free energy w.r.t some thermodynamic variable (i.e. the solid, liquid and gas transitions).
>> 
>> · *Second-order phase transitions*: continuous in the first derivative, but with discontinuity in the second derivative of the free energy (i.e. ferromagnetic phase transition).
>
>
>>[!info]- Modern classification
>>
>> · *First-order phase transitions*: involve a latent heat (i.e. melting of ice or boiling of water).
>>
>> · *Second-order phase transitions (also called continuous phase transitions)*: a divergent susceptibility (quantification for the change of an extensive property under variation of an intensive property), and a power-law decay of correlations near criticality.

>[!example] Van der Waals equation
> $$(P+\frac{an^2}{V^2})(V-nb^2)=nRT$$
> 
>with $a$ and $b$ as constants, they correct pressure and volume, respectively. 
>
>This equation works as a corrected model for real gases (adding new terms for molecular size and intermolecular attractions), mainly used when the critical temperature $T_c$ is reached, or liquid and low-pressure gaseous states.


## 9. Brownian motors and entropic forces

(See [[Perpetual motion machine]]).

### Brownian motor

The **Brownian motors** are nanoscale or molecular machines that can extract useful work from chemical potentials under large thermal fluctuations.
- On nanoscale, the thermal noise makes moving in a specific direction difficult.
- In systems with symmetry-breaking, thermal Brownian motion can be guided so that, instead of moving randomly in every direction, the particles tend to move in one preferred direction (the randomness of the system changes).

A Brownian motor needs:
- The presence of some amount of noise.
- Some sort of symmetry-breaking supplemented by temporal periodicity.
- Thermal non-equilibrium with at least two temperature levels.

The relevant state variables ($x(t)$ and $T(t)$) of a Brownian motor are loosely coupled (distinction from micro sized conventional mechanical engines).


### Rubber elasticity

Following the basic equations for the entropy $S$ and $F$, we model a driving force $f$ of entropy "pulling" the polymer intro an unstretched conformation.

In the **entropic elasticity**, we use an entropic force very similar to the pressure experienced by the walls of a box containing an ideal gas. In the canonical ensemble, this entropic force is defined as:

$$F(X_0)=T \nabla_X S(X)|_{X_0}$$ 
with macrostate $X$ and present macrostate $X_0$.

(See [[Entropic elasticity of DNA]]).

>[!info] See [[Equipartition theorem and partition function]].


### Fluctuation-Dissipation theorem

Two things happen simultaneously
- Fluctuations: random molecular collisions.
- Dissipation (friction): slowing down.

These two effects are not independent, this explains why a system remains at thermal equilibrium. 

When the friction is stronger and without stronger random collisions, everything would eventually stop. 

And, if the fluctuations were stronger without more friction, the particle would continuously heat up.

It also follows the equipartition theorem.

-------------------------------------

[[Examples in thermodynamics]]