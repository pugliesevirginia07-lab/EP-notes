
The **equipartition theorem** connects the microscopic motion of molecules with the macroscopic properties measured in thermodynamics.

The **equipartition theorem** states that when a system has reached thermal equilibrium, energy is shared equally among all the independent ways in which the particles can store the energy, provided that those energy terms are quadratic. 

Each of these energy terms contributes the same average amount of thermal energy:

$$\frac 1 2 k_B \ T \quad\text{ per molecule.}$$

This average energy is a statistical mean, meaning that individual particles constantly gain and lose energy through collisions, but the average over particles or time is fixed.

### Thermal and kinetic energy

- The **kinetic energy** is the energy associated with the motion of a particle.
- The **thermal energy** is the average energy associates with the random motion of all the particles in a system.

The thermal energy often includes kinetic energy, and it can also include potential energy associated with molecular vibrations (with quadratic potential energy terms, like the elastic potential energy).

### Degrees of freedom

A degree of freedom is an independent way in which a particle or molecule can store energy.

For the equipartition theorem, only quadratic degrees of freedom count, where the energy depends on the square of the variable.

>[!example] Average energy
>
>If a particle has $f$ quadratic degrees of freedom, the average thermalenergy is:
>
>$$ \left\langle E \right\rangle = \frac f 2 k_B \ T$$ 
>
>For a system with $N$ particles, the total thermal (internal) energy is:
>
>$$U=\frac f 2 N\ k_B \ T$$

A **monoatomic ideal gas** can translate in three spatial directions (x, y, z), hence the degrees of freedom would be $f=3$, with average energy:

$$\left\langle  E \right\rangle=\frac 3 2 k_B \ T$$

 this energy is entirely kinetic.

In **rotating molecules** (like a diatomic ideal gas, with $f=5$), the degrees of freedom in rotational motion are stored in the same way as in translational motion. The energy is shared equally among translation, rotation, and any other quadratic motions.

In **vibrating molecules**, the vibrations occur as normal modes, which are independent, these involve stretching and bending motions. 
- $3N -6$ modes for non-linear molecules.
- $3N-5$ modes for linear molecules.

### Conditions

The equipartition theorem holds only for systems that are in **thermal equilibrium** and **ergodic** (all the states are equally probable).

The energy must be able to flow freely between the different degrees of freedom. If some degrees of freedom cannot exchange energy efficiently, the equipartition theorem no longer gives the correct prediction.

### Applications

The equipartition theorem helps to derive **Brownian motion** with average kinetic energy fixed by: $\frac 3 2 k_B \ T$ .

It also agrees with the Maxwell-Boltzmann distribution $\frac 1 2 m \left\langle  v^2 \right\rangle= \frac 1 2 k_B \ T$ .

### Partition function

Instead of tracking every particle individually, we assign a probability to every possible microscopic state, and the **partition function** keeps track of all those probabilities.

Each microstate has some energy $E_i$ and the probability of finding the system in state $i$ is proportional to $e^{-E_i/(k_B T)}$, the Boltzmann factor. The low-energy states are more likely than the high-energy states.

>[!example] The partition function
>
>$$Z=\sum_i e^{-E_i/(k_B T)}$$
>
>The partition function is the total of the probabilities to find each state in the system. This function partitions (normalizes) the probabilities, so the total is up to one.
>
>$$P_i=\frac{e^{-E_i/(k_B T)}} Z$$
>
>Now the probabilities sum to 1.

It is useful to calculate the average thermodynamic quantities.