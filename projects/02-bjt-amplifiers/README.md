# BJT Amplifier Design and Bias Verification

This project designs and validates a common-emitter amplifier and a common-collector amplifier using a specified NPN model.

## Device model

Both original schematics use:

```text
.model NPN NPN(Is=5e-16 Bf=100)
```

Transient analyses use a 200 us stop time and a 1 ns maximum timestep.

## Common-emitter amplifier

`ltspice/q1/draft1.asc` preserves the submitted design:

- `VCC = 2.5 V`
- `RC = 30 kOhm`
- input source `SINE(0.653 0.5m 10k)`

The report checks the active-mode condition and records:

| Method | Voltage gain |
|---|---:|
| Hand calculation | 46.15 V/V |
| LTspice simulation | 53.44 V/V |

## Common-collector amplifier

`ltspice/q2/draft2.asc` preserves the emitter-follower design:

- `VCC = 3 V`
- `RE = 22 kOhm`
- input source `SINE(1.191 0.5m 10k)`

The report records approximately `0.955 V/V` for both hand calculation and simulation and verifies active-mode operation.

## Files

```text
submission/submission.pdf
ltspice/q1/draft1.asc
ltspice/q2/draft2.asc
evidence/
```

The original files are unchanged; the README only documents their contents.
