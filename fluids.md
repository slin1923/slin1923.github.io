---
layout: default
title: Fluids
---

<font size="5">Index</font>
- [Incompressible Flow](#incompressible-flow)
  - [Hydrostatics](#hydrostatics)
  - [Forces on a plate](#forces-on-a-plate)
  - [Bernoulli's Equation](#bernoullis-equation)
  - [Potential Flow Theory](#potential-flow-theory)
  - [Navier-Stoke's](#navier-stokes)
  - [](#)
- [Compressible Flow](#compressible-flow)
  - [Conservation Equations](#conservation-equations)
  - [Shocks vs Expansion Fans](#shocks-vs-expansion-fans)
    - [Rankine-Hugoniot Normal Shock Relations](#rankine-hugoniot-normal-shock-relations)
    - [Strong vs Weak Shocks](#strong-vs-weak-shocks)
  - [Burger's Wave Equation](#burgers-wave-equation)
  - [Rayleigh Flow](#rayleigh-flow)
  - [Fanno Flow](#fanno-flow)
- [Propulsion](#propulsion)
  - [Propulsion Equation](#propulsion-equation)


# Incompressible Flow

## Hydrostatics

## Forces on a plate

## Bernoulli's Equation

## Potential Flow Theory

## Navier-Stoke's 

##

# Compressible Flow

## Conservation Equations

## Shocks vs Expansion Fans

Shocks form adiabatic discontinuities that ALWAYS take an upstream relative supersonic Mach number $M^- > 0$ and **decelerates** it to a downstream subsonic Mach number $M^+ <0$. It is useful to think of shocks as walls.  Whereas in incompressible flow, we deal with all values of $P$, $T$, $u$, etc as a continuum through space, a shock is modeled as a boundary where these values can discontinuously jump. 

Expansion fans are the inverse of shocks.  Expansion fans are not discontinuities, but rather isentropic gradients that take an upstream relative subsonic Mach number $M^- <0$ and **accelerates** it to a downstream supersonic Mach number $M^+ >0$.  

### Rankine-Hugoniot Normal Shock Relations

A useful Rankine-Hugoniot relation online calculator developed by the Virginia Tech Aerospace Dept exists [here](https://devenport.aoe.vt.edu/aoe3114/calc.html): 

For a normal shock (1D problem), the Rankine Hugoniot relations tell us how thermodynamic values jump across the shock discontinuity. Notice that all you need is the upstream Mach number $M_1$ and specific heat ratio $\gamma$ and the entire relationship between the upstream and downstream states are defined.   

$$ M_2^2 = \frac{2 + (\gamma-1)M_1^2}{2\gamma M_1^2 - (\gamma-1)}$$

$$\frac{\rho_2}{\rho_1} = \frac{u_1}{u_2} = \frac{(\gamma+1)M_1^2}{2 + (\gamma-1)M_1^2}$$

$$ \frac{P_2}{P_1} = 1 + \frac{2\gamma}{\gamma + 1}(M_1^2-1)$$

$$ \frac{T_2}{T_1} = \frac{P_2}{P_1}\frac{\rho_1}{\rho_2} = [1 + \frac{2\gamma}{\gamma + 1}(M_1^2-1)][\frac{2 + (\gamma-1)M_1^2}{(\gamma+1)M_1^2}]$$

$$\Delta s = s_1 - s_2 = c_p \ln(\frac{T_2}{T_1}) - R\ln(\frac{P_2}{P_1})$$

Note that there are a few caveats/things to remember regarding the usage of the R-H relations. 

- All speed values $M$s and $u$s need to be converted to the shock frame if your shock is moving.  
- Calculated ratios are static-value ratios.  Please see thermodyanmics on the difference between static and stagnation values. 
### Strong vs Weak Shocks

## Burger's Wave Equation

## Rayleigh Flow

## Fanno Flow

# Propulsion

The general equation for thrust (of any propulsion system air or fuel-breathing) is 

$$ T = \dot{m_a}(U_e - U_0) + (P_e - P_0)A_e + \dot{m_f}U_e$$

Notice that the three terms here are essentially 

- momentum change of air mass
- exit pressure differential
- momentum change of fuel mass


## Propulsion Equation


