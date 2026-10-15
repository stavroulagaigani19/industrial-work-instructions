# Work Instruction: WI-ENG-204
**Title:** High-Precision Pressure Transducer Replacement & Recalibration  
**Applies to:** Modular Fluid Delivery Subsystem (Line 2 & Field Units)  
**Document Owner:** Industrial Engineering  
**Classification:** Standard Work Instruction (SWI)  

---

## 1. Safety, Hazard Mitigation & PPE

> ⚠️ **CRITICAL SAFETY DIRECTIVE:** Perform all Lockout/Tagout (LOTO) protocols prior to removing any enclosure covers.

- **Mandatory PPE:** Safety glasses with side shields (ANSI Z87.1), ESD dissipative wrist strap, nitrile gloves.
- **Energy Isolation:** 
  - Electrical: Turn off Main Breaker **MB-02** and apply personal padlock.
  - Pneumatic/Hydraulic: Bleed residual accumulator pressure via ball valve **BV-12** until gauge indicates **0.0 bar**.

---

## 2. Required Tools & Replacement Parts

### Tools & Equipment
- Calibrated digital torque screwdriver (0.2 – 2.0 Nm range)
- 10mm insulated open-end wrench
- Fluke 87V Digital Multimeter
- Lint-free cleanroom wipes & isopropyl alcohol (99%)

### Bill of Materials (BOM)
| Part Number | Description | Qty |
|---|---|---|
| **PT-5502-A** | Ceramic Diaphragm Pressure Transducer (0–10 bar) | 1 |
| **GSK-08-FKM** | Fluorocarbon O-Ring Gasket (Green) | 1 |
| **SCR-M3-SS** | M3x8 Hex Socket Cap Screws | 2 |

---

## 3. Step-by-Step Procedure

### Phase A: Disassembly & Inspection
1. Verify system de-energization using the digital multimeter at test points `TP-A` and `TP-B` (Target: `0.00 VDC`).
2. Disconnect the shielded M12 4-pin quick-disconnect cable from transducer housing. Inspect connector pins for bent pins or corrosion.
3. Using the 10mm open-end wrench, loosen the retaining gland nut counter-clockwise.
4. Carefully extract the depleted sensor body. **Do not touch the ceramic sensor face.**
5. Discard the old O-ring into scrap; never reuse elastomer seals.

### Phase B: Installation
1. Clean the sensor port threads and mating face using an isopropyl wipe.
2. Seat the new O-ring (`GSK-08-FKM`) evenly into the sealing groove.
3. Thread the replacement transducer (`PT-5502-A`) into position hand-tight.
4. Using the torque screwdriver, tighten to exactly **1.2 Nm** in a single continuous turn.
5. Reconnect the M12 fieldbus cable until audible locking click is verified.

### Phase C: Zero-Point Calibration & Quality Gate
1. Restore electrical power while keeping hydraulic line isolated.
2. Allow a 3-minute warm-up stabilization period.
3. Access the local operator interface (HMI) $\rightarrow$ Navigate to `Diagnostics > Sensor Calibration`.
4. Press **Auto-Zero**. Verify output baseline reads:
   - **Nominal:** `4.00 mA ± 0.05 mA` (or `0.00 bar ± 0.02 bar`).
5. Open supply valve **BV-12** and pressurize line to 5.0 bar test pressure. Hold for 60 seconds and visually inspect port for fluid leaks.
6. Record calibration verification sign-off in the station digital run log.
