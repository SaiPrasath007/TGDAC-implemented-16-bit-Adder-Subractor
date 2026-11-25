# 16-Bit CMOS Adder-Subtractor — Schematic Metrics & CMOS Comparison

## Measured Schematic Results (180nm GPDK, VDD = 1.8 V, Schematic-Only)
* **Worst-Case Propagation Delay ($t_{\text{pd}}$):** `111.2 ps` (`111.2e-12 s`, `0.9 V` threshold in ViVA)
* **Average Power ($P_{\text{avg}}$):** `59.67 µW` (`abs(average(IT("/V33/PLUS"))) * 1.8`)
* **Schematic Transistor Count:** `442` (`bsim3v3 442`, no physical layout or parasitic extraction yet)
* **Power-Delay Product (FoM / PDP):** `6.635 fJ` (`59.67 µW × 111.2 ps`)

## Equations
* `t_pd = t_out(0.9V) - t_in(0.9V)`
* `P_avg = |average(I_DD(t))| * V_DD`
* `Area_active = sum(W_i * L_i)` in `um^2` (schematic transistor count = `442`)
* `PDP = P_avg * t_pd`

## 16-Bit CMOS Benchmark Summary (180nm Node)
| Architecture | Node / Supply | Transistors | Delay | Power | PDP (FoM) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Hybrid DTGAC Adder-Subtractor (Yours)** | 180nm, 1.8 V (Schematic) | 442 | 111.2 ps | 59.67 µW | 6.635 fJ |
| Proposed SQRT CSLAS | CMOS, 180nm | 559 | 336 ps | 219 µW | 73.6 fJ |
| Proposed Linear CSLAS | CMOS, 180nm | 384 | 632 ps | 298 µW | 188.3 fJ |
| Conventional SQRT CSLAS | CMOS, 180nm | 682 | 572 ps | 532 µW | 304.3 fJ |
| Conventional Linear CSLAS | CMOS, 180nm | 762 | 756 ps | 490 µW | 370.4 fJ |
