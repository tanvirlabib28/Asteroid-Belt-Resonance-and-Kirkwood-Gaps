# Asteroid Belt Resonance and Kirkwood Gaps


A numerical simulation demonstrating how mean-motion resonances with Jupiter create the **Kirkwood gaps** in the asteroid belt.

### Overview

The asteroid belt between Mars and Jupiter is not uniform — it contains distinct gaps at specific orbital distances where asteroids are in resonance with Jupiter (e.g., 3:1, 2:1, 5:3, 3:2). This project simulates the dynamical evolution of 800 massless test particles over 20,000 years to reproduce these gaps through gravitational perturbations from Jupiter.

### Key Features

- **Physics Model**: Circular restricted three-body problem (Sun + Jupiter + test asteroids)
- **Integration Method**: 4th-order Runge-Kutta (RK4) with Δt = 0.01 years
- **Simulation Duration**: 20,000 years (~1.7 million Jupiter orbits)
- **Resonance Analysis**: Diagnostic resonance angle (θ = 3λ_ast - 2λ_Jup) to identify resonant vs. non-resonant behavior
- **Visualization**:
  - Initial vs. final asteroid positions
  - Semi-major axis evolution over time
  - Final semi-major axis histogram showing clear Kirkwood gaps
  - Resonance angle time series

### Technologies

- **Python**
- **NumPy** (vectorized computations)
- **Matplotlib** (visualization)
- **tqdm** (progress bar)

### Results

The simulation successfully reproduces the classic Kirkwood gaps at the expected resonance locations:
- **3:1** (~3.97 AU)
- **2:1** (~3.28 AU)
- **5:3** (~3.05 AU)
- **3:2** (~2.50 AU)

Asteroids near resonances show chaotic diffusion and large eccentricity increases, eventually leading to removal from the belt, while non-resonant orbits remain stable.

### Repository Contents

- `main.ipynb` / `simulation.py` — Main simulation code
- Plots:
  - Asteroid positions (initial vs final)
  - Semi-major axis time evolution
  - Final a-histogram with resonance markers
  - Resonance angle diagnostic

### Performance

- ~2 million integration steps
- Runs in approximately 2–5 minutes on a standard laptop

---

### How to Run

```bash
pip install numpy matplotlib tqdm
python simulation.py
