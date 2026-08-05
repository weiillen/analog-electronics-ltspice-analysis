# MOSFET Common-Source and Common-Drain Amplifiers

This project designs two NMOS amplifier stages and compares small-signal calculations with LTspice transient results while accounting for channel-length modulation.

## Device model

Both original schematics use:

```text
.model NMOS NMOS(vto=0.6 kp=400u lambda=200m)
```

The body terminals are connected according to the original designs, and transient analyses use a 200 us stop time with a 1 ns maximum timestep.

## Common-source amplifier

`ltspice/q1/Draft7.asc` preserves the submitted design:

- `VDD = 1.8 V`
- `VG = 0.72 V`
- `RD = 95 kOhm`
- `M1: W = 0.5 um, L = 0.18 um`

The report records:

| Quantity | Result |
|---|---:|
| `VDS` of M1 | 0.903 V |
| Simulated gain | 12.98 V/V |
| Hand-calculated gain | 12.67 V/V |

## Common-drain amplifier

`ltspice/q2/Draft8.asc` preserves the two-transistor source-follower design:

- `VDD = 1.8 V`
- `VG = 1.55 V`
- `VBIAS = 0.90 V`
- `M1: W = 3.33 um, L = 0.18 um`
- `M2: W = 0.862 um, L = 0.18 um`

The report records:

| Method | Voltage gain |
|---|---:|
| LTspice simulation | 0.975 V/V |
| Hand calculation | 0.971 V/V |

## Files

```text
submission/submission.pdf
ltspice/q1/Draft7.asc
ltspice/q2/Draft8.asc
evidence/
```

The original files are unchanged; this documentation only explains the preserved work.
