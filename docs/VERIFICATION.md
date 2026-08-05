# Verification record

## Integrity checks

Every preserved artifact was copied and then checked using SHA-256. All entries in `ORIGINAL_FILE_MANIFEST.tsv` have `byte_identical = true`.

## Static inspection

The repository contains eight original LTspice schematic files:

- four diode-circuit files;
- two BJT-amplifier files; and
- two MOSFET-amplifier files.

The files retain their original directives and model parameters, including:

- diode saturation-current models and `.op`, `.dc`, and `.tran` analyses;
- `.model NPN NPN(Is=5e-16 Bf=100)` for the BJT designs; and
- `.model NMOS NMOS(vto=0.6 kp=400u lambda=200m)` for the MOSFET designs.

## Runtime verification boundary

LTspice was not installed in the packaging environment, so simulations were not rerun. The preserved submission PDFs and screenshots provide the original run evidence and reported measurements.
