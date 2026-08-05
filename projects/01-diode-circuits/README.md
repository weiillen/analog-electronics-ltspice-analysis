# Diode Circuits and Nonlinear Signal Processing

This project studies how diode models affect DC operating points, rectification, ripple, and nonlinear transfer characteristics.

## Included studies

### 1. Diode bias and operating point

`ltspice/q1/Draft1.asc` models two diodes with different saturation currents and performs an operating-point analysis. The preserved file uses:

- `R1 = 130 Ohm`
- `Dmod1: Is = 1e-16 A`
- `Dmod2: Is = 1e-15 A`
- `.op` analysis

The accompanying report compares large-signal and small-signal reasoning and explains why their predictions differ away from the linearization point.

### 2. Full-wave rectifier with capacitor filtering

`ltspice/q2/Draft2.asc` contains a bridge rectifier driven by a 4 V, 100 kHz sinusoid with a 300 kOhm load. The preserved schematic stores the 600 pF case and uses a 30 us transient simulation with a 10 ns maximum timestep.

Reported ripple values:

| Capacitance | Hand calculation | Simulation |
|---:|---:|---:|
| 100 pF | 0.43 V | 0.339 V |
| 600 pF | 0.0722 V | 0.0605 V |

### 3. Nonlinear transfer curves

`ltspice/q3/Draft3-1.asc` and `Draft3-2.asc` implement two diode-resistor networks and sweep the input from -4 V to 4 V using a DC analysis. The report compares hand-derived piecewise behavior with LTspice transfer plots.

## Files

```text
submission/submission.pdf
ltspice/q1/Draft1.asc
ltspice/q2/Draft2.asc
ltspice/q3/Draft3-1.asc
ltspice/q3/Draft3-2.asc
evidence/
```

The circuit and evidence files are preserved unchanged.
