# DC Motor Speed Control with Fault Detection

## Overview
This project simulates a **DC motor** under **PID speed control** and detects mechanical faults automatically.  
The motor is modelled using its physical equations, faults are injected into the model, and detection is based on speed error thresholding.

## Features
- **Dynamic Modelling**: Implements the electrical & mechanical equations of a DC motor.
- **Closed-loop PID Control**: Maintains reference speed under normal operation.
- **Fault Injection**:
  1. Sudden load torque step (t = 5s)
  2. Increased damping/friction (t = 10s)
- **Fault Detection**: Threshold-based detection using absolute speed error.
- **Visualization**: Plots showing speed tracking and detection metric.

## Simulation Model
Motor equations:
- Electrical: L(di/dt) = V - R·i - K·ω
- Mechanical: J(dω/dt) = K·i - b·ω - T_load

Where:
- J: Rotor inertia (kg·m²)
- b: Viscous friction (N·m·s/rad)
- K: Motor constant (N·m/A)
- R: Armature resistance (Ω)
- L: Armature inductance (H)
- V: Control voltage (V)
- i: Armature current (A)
- ω: Angular speed (rad/s)

## Requirements
- Python 3.x
- NumPy
- Matplotlib

Install dependencies:
```bash
pip install numpy matplotlib
