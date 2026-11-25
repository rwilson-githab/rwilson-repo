# Physical and numerical methods

HARMPI evolves a relativistic magnetized fluid on a black-hole background. This notebook uses the upstream torus setup and changes grid size, spin, adiabatic index, torus radii and integration duration. The alternate field prescription changes the vector-potential initialization at line 412 of init.c. It is an intended MAD candidate, not proof of magnetic arrest.

## Diagnostics
In geometrized units, the Kerr horizon radius is $r_H/M=1+\sqrt{1-a^2}$. The notebook evaluates the closest radial grid index and integrates the mass and magnetic flux using the simulation coordinate cell widths and metric determinant.

- Mass accretion rate: $\dot M=-\int \rho u^r\sqrt{-g}\,dx^2 dx^3$.
- Magnetic flux: $\Phi=\frac12\int |B^r|\sqrt{-g}\,dx^2 dx^3$.
- Normalized magnetic flux: $\phi=\Phi/\sqrt{|\dot M|}$.
- Plasma beta: $\beta=2p_g/b^2$.
- Magnetization: $\sigma=b^2/\rho$.

These formulas follow the submitted notebook; verify azimuthal normalization, units and near-zero accretion handling before quantitative interpretation.
