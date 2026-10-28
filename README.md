# 🚀 RocketPy EuRoC Simulation

Flight simulation of a liquid-propellant sounding rocket built for the
[EuRoC](https://euroc.pt/) competition (9000 m apogee category), made with
[RocketPy](https://docs.rocketpy.org/).

Everything lives in one notebook: [`liquid_motor.ipynb`](liquid_motor.ipynb).

## What's inside

- **Liquid engine** – N₂O / ethanol, Isp 220 s, 20 s burn with a boost → sustain
  thrust profile (3500 N → 650 N) and a smooth ignition ramp.
- **Tanks** – cylindrical tanks with spherical caps (`MassFlowRateBasedTank`),
  mass flow tied to the thrust curve.
- **Rocket** – airframe, 1 kg CanSat payload, von Kármán nose cone,
  trapezoidal fins, boattail, rail buttons, drag curves (power on / off).
- **Recovery** – drogue at apogee and main parachute at 400 m AGL
  (EuRoC limit: ≤ 450 m).
- **Environment** – launch site in Portugal, GFS forecast atmosphere.
- **Flight analysis** – trajectory, kinematics, forces, energy, stability margin,
  thrust-to-weight, apogee and impact conditions.
- **Experiment** – how the hull (structure) mass affects apogee, rail exit speed
  and landing speed, compared against EuRoC requirements
  (30 m/s rail exit, ≤ 9 m/s landing, 9000 m target).

## Getting started

```bash
pip install rocketpy numpy pandas matplotlib jupyter
jupyter notebook liquid_motor.ipynb
```

> The forecast atmosphere (`GFS`) is downloaded on the fly, so an internet
> connection is required. Use `standard_atmosphere` for offline runs.

## Tech stack

Python · RocketPy · NumPy · pandas · Matplotlib · Jupyter
