# Chapter 1 : Special relativity
## 1. Introduction

The main motivation was the conflict between Galilean mechanics and electromagnetism. Galilei-transformations failed for very large velocities, allowing simple addition of velocities between inertial frames, due to the Maxwell's equations implying a fixed speed of light, they started thinking about the "ether" (which existence was refuted by the [Michelson-Morley experiment](https://en.wikipedia.org/wiki/Michelson%E2%80%93Morley_experiment)).

### Short review to inertial frames
We use frames of reference as a coordinate system to describe motion.

Then we have two types of frames:
- Inertial frames: the system moves at a constant velocity.
- Non-inertial frames: the system is accelerating (for both translational or rotational acceleration). We usually describe them adding inertial forces, like the Coriolis force or the centrifugal force.
### Postulates of the theory of special relativity
1. All inertial systems are equivalent for all physical laws.
2. The velocity of light in the vacuum has the same value in all inertial systems (independent of the motion of the observer or the light source).


## 2. Lorentz transformations

To preserve the invariance of the speed of light, we must replace the Galilean transformation ($x'=x-vt$ and $t'=t$) with the Lorentz transformation.

The Lorentz transformations are based in the Lorentz factor, which determines how important relativistic effects are.

>[!example] Lorentz factor
>$$\gamma=\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}$$

- When $\large v\ll c$,  $\large \gamma  \approx 1$. Hence, it will be subject to classical mechanics effects.
- When $\large v \rightarrow c$, $\large \gamma \rightarrow \infty$. Where the relativistic effects become more important, meaning that the objects require infinite energy to accelerate further.

To change from the inertial frame $S$ (stationary) to $S'$ (moving with velocity $v$ along the x-axis) with the same origin $t=t'=0$, we have:

$$ 
x'=\gamma (x-vt)\ , \qquad t'=\gamma (t-\frac{vx}{c^2})
$$

With $y'=y$ and $z'=z$. To transform back to $S$ from $S'$, we apply:

$$ x=\gamma (x'+vt') \; , \qquad t=\gamma (t'+\frac{vx'}{c^2})$$

You can see they all converge to Galilei transformations when $v \ll c \Rightarrow \gamma \approx 1$. 


## 3. Simultaneity

For each observer, the simultaneity of two events at different spatial points depends on the coordinate system in which the events are described. 

To show that two events are simultaneous or not, we use Minkowski spacetime diagrams.

### Spacetime diagrams

![[Spacetime diagram.png]]
>[!multi-column] Description of spacetime diagrams
>> [!note]- First diagram: observer at rest
>>>A light pulse is emitted from the midpoint $B$ of a stationary object. Since the distances $AB$ and $BC$ are equal and light propagates with the same speed $C$ in both directions, the pulses reach the ends $A$ and $C$ simultaneously. This is represented by the events $A_1$​ and $C_1$​ lying on the same horizontal line $T=T_1$. Therefore, an observer at rest with the object concludes that both events occur at the same time.
>
>>[!note]-  2nd diagram: Moving Observer
>>>For an observer moving relative to the object, the same physical events are described in a different reference frame. The object's world-tube becomes tilted, and the lines of simultaneity are no longer horizontal. The red line represents $t'=\text{const.}$, i.e., events that are simultaneous in the moving frame. Since $A'_1$ and $C'_1$​ do not lie on the same simultaneity line, the moving observer concludes that the light reaches one end before the other. 
>>

The worldline for a moving object is a diagonal (for constant velocity), which creates a light line when $v=c$. the combination of all light lines form the light cone, all worldlines should be contained inside of it, any world line outside of the light cone is not possible, because it will mean that $v>c$. Hence, if we represent the light line with a slope=1, the world lines must have a slope smaller than 1. The angle $\alpha_1$ and $\alpha_2$ correspond to $\alpha=\arctan \frac{v}{c}$.

>[!multi-column] Lightcone
>>![[Lightcone.png|250]]
>>
>>
>> · In a 3D spacetime diagram ($x,y,ct$) the surfaces $x^2+y^2=c^2t^2$ form a cone named light-cone, where past and future are inside of it.
>>
>> · Two events can be causally connected if both points lie in one of the light cones. Signals and interactions can be interchanged between objects in these points.


### Spacetime interval
In special relativity the distances are no longer the same due to the problem of simultaneity and the Lorentz contraction (mentioned later).

Space and time are not invariant, due to the length contraction and the time dilation, respectively. Hence, we get the spacetime interval ($\Delta s$), which is the measure of separation between two events. It is invariant in special relativity and defined as:
$$ \large\Delta s^2=c^2\Delta t^2-\Delta x^2- \Delta y^2 - \Delta z^2 $$
It works as an analogy to the distance (in 4D) and is equal in all inertial systems.
- When $s^2=0$ : we obtain the world line $x=\pm ct$, for a light pulse.
- When $s^2>0$ : we obtain a world line with accessible events with $v<c$.
- When $s^2<0$ : we obtain non-accessible events (for $v>c$), forming a hyperbola infinitely approaching to the light line.

![[Spacetime interval representation.png|300]]


## 4. Lorentz length contraction

The lengths in $S'$ are not equal to the lengths in $S$, due to the difference in the scale lengths caused by different simultaneity for the measurements of the endpoints, making $L'$ seem shorter than $L$ (length of the object at rest). 

The Lorentz transformations acts in the lengths in a similar way as we have seen previously: 
$$ L'= \gamma L$$

Lorentz contractions are symmetric and do not depend on the sign of the velocity.


## 5. Time dilatation

>[!abstract] $\Delta t$ in different systems
>For $O$ in $S$: $\Delta t= t_2-t_1 \qquad \qquad$
>
>For $O^`$ in $S'$: $\Delta t'=t'_2 - t'_1= \gamma \Delta t$

We can see that $\Delta t'>\Delta t$ for $\gamma >1$. Meaning that moving clocks run slower, similar to what happens in the length contraction. 

$$ \Delta t'= \gamma \Delta t$$

(See [[Twin paradox]])


## 6. Energy in special relativity

The relativistic kinetic energy is defined as:

$$ E_k=\frac{mc^2}{\sqrt{1-\frac{v^2}{c^2}}}-mc^2=(\gamma -1)mc^2$$

with $m= \frac{m_0}{\sqrt{1-\frac{v^2}{c^2}}}=\gamma \ m_0$  , the relativistic mass, which increases due to its kinetic energy. The speed limit is at the lightspeed, when $\gamma \rightarrow 0$, requiring infinite force to accelerate further.  


In special relativity, the energy is a component of a unified "energy-momentum 4-vector", conserved across all inertial reference frames. They have differences in mass, velocity and energy with the Newtonian mechanics.

Mass can be converted into energy:
- Total energy of a moving body: $E_{total}=E_{rest}+E_{k_{relativistic}}=\gamma \ m c^2$. The energy increases as an object approaches speed of light.
- Rest energy: $E_{rest}=mc^2$ . In Newtonian mechanics, $E_{rest}=0$.

(See [[Nuclear reactions]])