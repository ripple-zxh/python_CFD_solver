# 2D Incompressible Flow Simulation (Navier–Stokes)

🌐 Language: English 

---

## Overview

This project implements a simple 2D incompressible flow solver using the finite difference method.
It solves the Navier–Stokes equations on a structured grid.

The example corresponds to a classic **lid-driven cavity flow** problem.

---

## Features

* Finite difference discretization
* Pressure Poisson equation solver
* Explicit time stepping
* Velocity + pressure visualization

---

## Requirements

* Python 3.x
* NumPy
* Matplotlib

Install dependencies:

```bash
pip install numpy matplotlib
```

---

## Example Code

```python
# 2D incompressible Navier-Stokes solver
import numpy as np
import matplotlib.pyplot as plt

Lx, Ly = 50.0, 50.0
nx, ny = 50, 50
dx = Lx / (nx - 1)
dy = Ly / (ny - 1)

dt = 0.1
rho = 1000.0
miu = 0.001
nu = miu / rho

u = np.zeros((nx, ny))
v = np.zeros((nx, ny))
p = np.zeros((nx, ny))
```

*(Full code omitted for brevity — see source file)*

---

## Output

* Pressure field (contour plot)
* Velocity field (quiver)

---

## Notes

* Time step (`dt`) must be small for stability
* This is an educational implementation, not optimized
* Uses central differences (can be unstable at high Reynolds numbers)

---

## License

MIT License
