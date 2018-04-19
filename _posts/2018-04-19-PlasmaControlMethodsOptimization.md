### Control Methods for the Optimization of Plasma Scenarios in a Tokamak

by [Jacques Blum](jacques.blum@unice.fr), et al.

#### Abstract
This paper presents the modelling of the evolution of plasma equilibrium in the presence of external poloidal field circuits and passive structures. The optimization of plasma scenarios is formulated as an optimal control problem where the equations for the evolution of the plasma equilibrium are contraints. The procedure determines the voltages applied to the external circuits that minimize a certain cost-function representing the distance to a desired plasma augmented by an energetic cost of the electrical system. A sequential quadratic programming method is used to solve the minimization of the cost-function and an application to the optimization of a discharge for ITER is shown.

#### Keywords:
Plasma equilibrium, Optimization, Tokamak, Magnetohydrodynamics, Optimal control

#### Introduction
The magnetic filed has two components (as show in Fig. 1)

+ a toroidal field created by toroidal field coils, that is necessary for the stability of the plasma,
+ a poloidal field in the section of the torus created by poloidal field coils and by the plasma itself.

The plasma current is obtained by induction from currents in these poloidal field coils. The tokamak thus appears as a transformer whose plasma is the secondary. **The currents in the external coils play another role, that of creating and controlling the equilibrium of the plasma**. The <font color=red> goal</font> of this paper is to provide a model for the evolution in time of the equilibrium of the plasma and to derive control methods in order to optimize a typical scenario of a discharge of the plasma in a tokamak.

![Fig_1](../img/tokamak_schematic.jpg)

