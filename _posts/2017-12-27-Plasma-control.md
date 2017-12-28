---
layout: post
title:  "Plasma Control"
author: Roberts
---

## Real-time control solutions for plasma control problems in Tokamak experiments
by Riccardo Vitelli (Dissertation)
### The Vertical Stabilization
#### The vertical Instability problem
* Non-circular, elongated plasmas have naturally considerable advantages regarding confinement, achievement, achievable pressure and space utilization. However elongated plasmas suffer from a natural fast vertical instability which requires closed-loop feedback control, without which no experiment could be carried out.
* The vertical force generated on the plasma is inversely proportional to the distance.
* The inverse of the time in which the plasma hits the superior or inferior wall when not stabilized is called **growth rate**.

* It is possible to estimate the growth rate by using a simplified model of the vertical instability called *rigid displacement model*.
    * In this model the plasma is represented by one or more rigid filaments in which a constant current flows.
    * Those filaments are considered as having a single degree of freedom, i.e. the vertical posiiotn of their current centroid.

----

## Current-oriented modeling of the plasma particle density in tokamaks and application to real-time density profile reconstruction
T.C. Blanken, FED 126 (2018) 87-103

### Introduction
* Since the density profile affects the plasma pressure and fusion power, drives radiation, influences the non-inductive current distribution, determines diagnostics validity (e.g. ECE cut-off), and can trigger detrimental plasma instabilities, real-time monitoring and control of the particle density profile is of great importance for safe, reliable and high-performance operation of large tokamaks such as ITER.

----

## Real-time physics-model-based simulation of the current desntiy profile in tokamak plasmas

[Online at: stacks.iop.org/NF/51/083052 ](http://stacks.iop.org/NF/51/083052)

### Introduction
* Some recent work has employed statistical methods such as **Bayesian** analysis to provide rigorous techiniques to separate diagnostic measurements into a signle estimator for a given quantity [1](http://iopscience.iop.org/article/10.1088/0741-3335/50/8/085002/meta;jsessionid=999D50CF48C1D96788FF2F87CF78691F.c2.iopscience.cld.iop.org). Nevertheless, estimated quantities at a given time instant depend exclusively on diagnostic data gathered at that time point, possibly filtered to remove measurement noise.
* In this paper, a novel paradigm for real-time reconstruction of the plasma state based on first-principle physics models is presented.
  * A physics-based model of internal plasma profile dynamics is solved while the plasma is physically evolving in the tokamak.
  * This real-time simulation provies within the validity boundary of the model, full knowledge of the plasma profiles with spatial and temporal resolution constrained only by the computational power of the hardware on which the simulation is executed, and not by the spatial or temporal resolution of diagnostics.
  * In this framework, the avaiable real-time diagnostic data can be included in a natural way to improve the accuracy of the estimate.
  * This approach is known in the control engineering community as that of a _dynamic state observer_ and it typically used to estimate unmeasured or poorly measured states of a dynamical system.

* While the paradigm is general and can be applied, in principle, to any or all of the mentioned plasma profiles, this paper focuses on the current density profile (or, equivalently, the safety factor ($$q$$) or poloidal flux ($$\psi$$) profile).
    *  The $q$ profile is of prime importance for the plasma performance and macro-stability, since its shape determines the proximity to operational MHD limits, the presence of improved confinement (e.g. hybrid) regimes or transport barriers, and the appearance and location of tearing modes.
    *  The physics of poloidal flux diffusion, which governs the current density profile evolution, is relatively well understood and reliable physics models exist on which to base first-principle simulations.
    *  The $q$ profile happens to be quantity which is particularly difficult to measure with sufficient spatial and temporal accuracy in real-time.

* We propose to perform an interpretative transport simulation in real-time during the plasma discharge.
A considerable amount of additional information obtained from these simulations, including the profiles of poloidal flux, current density, magnetic energy, rotational transform, magnetic shear, internal inductance, poloidal magnetic field, toroidal electric field, bootstrap current, ohimc current density, etc, becomes avaiable in real-time and can be used for feedback control, disruption avoidance, scenario monitoring, and a wealth of other applications.


* Reference [2](http://iopscience.iop.org/article/10.1088/0741-3335/49/7/009/meta) provides the basic idea, which presents a control-oriented current density profile model which would be suitable for real-time implementation.
We show the successful resolution of the plasma poloidal flux transport equation with time steps of the order of **1ms** which is comfortably shorter than the golbal TCV current redistribution time (~150ms for heated plasmas).
_The fact that this could be achieved for the relatively short characteristic time scales of the moderately sized TCV implies that this method can easily be applied to larger tokamaks with longer time scales._

* In order to be applicable to advanced scenarios, this model must include at least plasma resistivity, bootstrap current and auxiliary current drive sources. <font color='blue'>The model we have implemented is based on the partial differential equation (PDE) describing the diffusion of poloidal flux as detailed in [10](http://journals.aps.org/rmp/abstract/10.1103/RevModPhys.48.239) and implemented in the ASTRA code [2](http://iopscience.iop.org/article/10.1088/0741-3335/49/7/009/meta), which the restriction that the shape of the flux surfaces and the toroidal flux they enclose maintained fixed in time</font>.


* Real-time measurements of the plamsa quantities that are required as inputs to th epoloidal flux transport solver. These are (a) total plasma current $$I_p$$ or loop voltage $$V_{loop}$$ and (b) the plasma kinetic profiles, at least $$T_e(\rho)$$ but preferably also $$n_e(\rho)$$ and $$T_i(\rho)$$ for bootstrap current calculations.
  * The plasma curent is avaiable in real-time from a discrete set of magnetic measurements or from a Rogowski coil.
  * The kinetic profiles are inherently more complicated to obtain and the availability of the real-time diagnostics for each profile is different for each individual tokamak. In some case, ECE, Thomson scattering, and/or charge exchange recombination spectroscopy diagnostics may be used in real-time.

----------------------------------------------------------------

## On plasma vertical stabilization at EAST tokamak
by G. De Tommasi

### Abstract
* By exploiting a plasma/circuit linearized model, we show that the plant cannot be strongly stabilized by using the in-veseel coils and a single-input-single-output (SISO) controller that feeds back only the plasma vertical speed $$\dot z_p$$ (i.e. without integral action on $$\dot z_p$$).
* Moreover, a stable muilti-input-single-output (MISO) controller that stabilizes the plant without the need of feeding back the plasma vertical position is presented.
* The proposed solution permits to achieve stabilization of the EAST plant without coupling the vertical stabilization system with the plasma shape controller.


### Introduction
* Reliable and roubst operations of modern tokamaks call for active control of the poloidal component of the magnetic field.
* **The main objectives of magnetic control are the regulation of the plasma current and shapes as well as the vertical stabilization**.
* In particular, the **Vertical Stabilization (VS)** system is essential to operate tokamaks with elongated and vertical unstable plasmas.

----------------------------------------------------------------

## Simulation suite for plasma magnetic control at EAST tokamak
by Raffaele Albanese, Antonio Castaldo


### 1 Plasma modelling
+ A tokamak can be seen as a system consisting of the plasma, the passive structures and the active circuits; the 2D FEM code CREATE-NL is designed to solve numerically the Grad-Shafranov equations, which describe the behavior of such a system under the hypothesis of axial symmetry. The output of the code is a file containing a non-linear plasma equilibrium; then, both CREATE-NL and CREATE-L can be used to obtain a linearized model by means of two different linearization procedures (respectively, numerical and anlytical) in a neighborhood of the equilibrium point.
+ It is worth to mention that, in order to have a good plasma current behaviour, an equivalent voltage ($$V_{loop}$$) has to be imposed on the plasma circuit.
+ In order to have a good estimation of plasma current behavior in the time simulation interval, an equivalent plasma resistance can be obtained by means of experimental flux measurements and making use of Faraday-Newman's law.
+ Isoflux
    + In order to contorl plasma shape, Isoflux control logic aims to take to zero the flux differences between active X-point and some specific points on plasma boundary. (For this reason, a good reconstruction of fluxes on control segments is essential.)
    + Isoflux control logic is also characterized by a direct control of the position of the null-point (either only the active one or both active and inactive, depending on the configuration); furthermore, the knowledge of the flux a the X-point is necessary for the shape control.

----------------------------------------------------------------
## Plasma control issues for an advanced steady state tokamak reactor
by D. Moreau & I. Voitsekhovitch
* In inductively driven tokamak plasmas, the plasma current is controlled by the extrernal loop vlotage through the primary circuit voltage, and a stationary current density profile is established as a result of the diffusion of the electric field imposed at the plasma surface.

## Bootstrap current fraction scaling for a tokamak reactor design study
by Keii Gi, et al
* The bootstrap current is the current parallel to the magnetic field caused by the anisotropy in the electron pressure tensor.

## Implementation of Fast Real-Time Control of Unstable Modes in Fusion Plasma Devices
+ Feedback control with a proportional, integral and derivative (PID) controller is commonly used in the PCS, as a full understanding of the plasma behaviour is not required.



## ITER Plasma Vertical Stabilization
A. Portone, R. Albanese, G. Ambrosino
* In present and future tokamak devices featuring elongated plasmas cross-sections, vertical stabilization must be reliably maintained over a wide range of operating conditions including off-normal event such as emergency shutdown.
* Any failure or poor reliability of the plasma Vertical Stabilization (VS) system will lead inevitably lead to a loss of machine performance or to an increase in Vertical Displacement Events (VDEs) rate and associated thermal and mechanical loads on several key machine components (e.g. blanket modules).
* **In tokamaks plasma vertical stabilization is achieved by combining passive stabilization by the image currents flowing in the surrounding metallic structures with active (feedback) control obtained by powering external coils to produce an n=0 horinontal field**

### Plasma Equilibrium Configurations
* The ITER VS system is designed and assessed on the basis of a broad range of plasma equilibria that are representative of the various opeartion scenarios (e.g. ELMy H-mode, hybrid, etc.) and that are most demanding for vertical control. These conditions are, typically, associated to **MHD equilibria with low kinetic pressure** (e.g. L-mode plasmas), **high separatrix elongation** and **peaked current profiles** since these plasmas maximize the external destabilizing force (high $$k_x$$, high $$l_i$$) and minimize the coupling to the metallic structures that provide passive stabilization (low $$\beta_p$$).
* In particular, the minimum voltage necessary to stabilize a given offset $$z_{p0}$$ scales as $$v_0 \sim z_{p0}I_p \gamma$$







