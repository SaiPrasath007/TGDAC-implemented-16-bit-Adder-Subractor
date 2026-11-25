# TGDAC-Implemented 16-Bit Adder-Subtractor (180nm CMOS)
Schematic-level design and Spectre simulation of a 16-bit hybrid DTGAC/CMOS adder-subtractor in **180 nm GPDK** (`VDD = 1.8 V`, Cadence Virtuoso / MMSIM121).
## Key Schematic Performance Metrics
* **Worst-Case Propagation Delay ($t_{\text{pd}}$):** `111.2 ps` (`111.2e-12 s`, measured at `0.9 V` threshold in ViVA)
* **Average Power ($P_{\text{avg}}$):** `59.67 µW` (`abs(average(IT("/V33/PLUS"))) * 1.8` at `1.8 V`)
* **Schematic Transistor Count:** `442` MOS transistors (`bsim3v3 442` from Spectre circuit inventory; schematic-only, no layout view yet)
* **Power-Delay Product (FoM / PDP):** `6.635 fJ` (`59.67 µW × 111.2 ps`)
## Repository Structure
* `netlist/input.scs` — Spectre schematic netlist
* `docs/` — Report notes, equations, and CMOS benchmark comparisons
* `waveforms/` — ViVA waveform and table screenshots
