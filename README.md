# Cools HBM Thermal Clutch

## From Air-Jet Cooling to Direct Solid Conduction

**0.5-second heat pickup · approximately 85% lower cumulative thermal exposure in a 12-layer model · heat-dump time hidden outside the effective bonding takt**

[한국어](README_KR.md) · [中文](README_ZH.md)

![Thermal Clutch concept](assets/thermal_clutch_three_phase.svg)

## The transition

Conventional High Bandwidth Memory (HBM) thermocompression bonding cools the heater and collet through air-jet convection. Cools changes the physical heat-transfer path itself.

During cooling, a cold aluminum nitride (AlN) thermal shuttle is pressed directly against the full rear surface of the heater assembly. Heat is therefore transferred by direct solid conduction instead of low-conductivity gas convection.

> **HBM bonding does not need a stronger air jet. It needs a different heat-transfer path.**

This is not a stronger fan, a larger nozzle, or a more aggressive air pulse. It is a transition from gas-side convection to pressure-assisted solid-to-solid heat pickup.

## Headline performance

| Metric | Conventional TCB | Cools Thermal Clutch |
|---|---:|---:|
| Cooling mechanism | Air jet / convection | Full-area direct solid conduction |
| Cooling time, 300 to 150 °C | about 4 s | about 0.5 s |
| Cumulative equivalent thermal exposure at the lowest pre-bonded joint, 12-layer model | Baseline | approximately 85% lower |
| Heat-dump time added to effective takt | Fully added | 0, hidden during die pick and alignment |
| Additional electrical actuator | Not applicable | 0 |
| Utility requirement | Air-based cooling hardware | Existing pressure and house-vacuum lines |

The 0.5-second value is a modeled design result for the representative dimensions and thermal masses described in the Korean technical brief. The approximately 85% reduction is likewise based on the 12-layer analytical model presented there.

## Three-phase thermal-clutch cycle

1. **Heating and standby**  
   The AlN shuttle is held against the heat-dump manifold by vacuum, leaving an approximately 100 µm vacuum gap above the heater pickup surface. The thermal path is open, so heating power is concentrated at the bond interface.

2. **Cooling pickup**  
   At the end of heating, positive pressure moves the shuttle into full-area contact with the heater rear surface. Heat is rapidly loaded into the shuttle while bonding pressure and planar constraint are maintained.

3. **Hidden heat dump**  
   Vacuum returns the heated shuttle to the heat-dump manifold. The shuttle releases its stored heat while the next die is picked, aligned, and prepared. Heat rejection therefore does not add to the effective bonding takt.

## Why this matters for HBM stacking

As each new die is bonded, heat spreads downward through the stack and reheats joints that were already formed. In an n-layer stack, the lowest joint can experience n-1 repeated thermal exposures.

The Thermal Clutch returns the bonded stack toward a defined starting thermal state before the next bonding step. This directly targets:

- cumulative intermetallic-compound growth;
- prolonged high-temperature dwell;
- remelting and bridging risk;
- thermally induced joint collapse;
- warpage during solidification and stiffness recovery;
- loss of process window as the stack moves from 12 layers toward 16 layers and beyond.

## Productivity is more than faster cooling

The central manufacturing advantage is not merely changing a 4-second cooling step into a 0.5-second cooling step.

The Thermal Clutch separates **heat pickup** from **heat rejection**. Only rapid pickup remains inside the bonding cycle. The slower dump process is moved into a parallel interval that already exists for die handling.

> **The next HBM productivity breakthrough will come from hiding heat rejection outside the bonding takt.**

## Retrofit architecture

The platform is designed as a rear-side bond-head module rather than a new bonder architecture.

Representative retrofit scope:

- one AlN shuttle;
- one pressure space and compact heat-dump manifold;
- two utility connections;
- one valve-control channel;
- no motor, solenoid, piezoelectric stage, or moving electrical harness near the hot zone;
- no change to the core bonding temperature profile, load profile, or underfill concept.

The shuttle is moved by pressure-sign switching using fab utilities such as Clean Dry Air (CDA), nitrogen pressure, and house vacuum.

## Representative design

The source technical brief describes a representative implementation using:

- heater: 16 × 16 × 1.5 mm;
- AlN shuttle: 12 × 12 × 9.9 mm;
- nominal vacuum gap: 100 µm;
- AlN thermal conductivity: approximately 170 W/(m·K);
- shuttle thermal capacity: approximately 3.4 J/K;
- calculated coupled equilibrium temperature: approximately 119 °C;
- example bond peak and reset temperature: about 300 °C and 150 °C.

These dimensions are a representative embodiment, not the full boundary of the platform.

## Applications

- HBM stacking using thermocompression bonding;
- thermocompression non-conductive film (TC-NCF) and molded reflow-molded underfill (MR-MUF) related flows;
- die-to-wafer chiplet attach;
- thermal-budget control in pre-hybrid-bonding processes;
- large-area interposer and package-substrate attachment.

## Patent position

Cools positions the HBM Thermal Clutch as an implementation of its selective dual-surface intermediate heat-transfer platform. The architecture includes selective contact between the heating side and heat-dump side, three-phase one-way heat transport, thermal-state reset between stacking steps, hidden heat dumping, pressure-sign switching, heat-capacity equilibrium-point design, and thickness-to-thermal-penetration-depth matching.

Publication of this repository does not grant any licence, implied right, or permission to practise the disclosed technology.

## Related Cools technology

For large-area package warpage control and four-compute-die-class packaging architecture, see the Cools Large Area Thermal Clutch repository:

- [Cools CoWoS No-Warpage Solution](https://github.com/jhcho9494/Cools_CoWos_No_WarpageSolution)

## Contact

**Dr. Jinhyun Cho — Founder & CEO, Cools Inc.**  
Email: [jhcho@cools.co.kr](mailto:jhcho@cools.co.kr)

© 2026 Cools Inc. All rights reserved.
