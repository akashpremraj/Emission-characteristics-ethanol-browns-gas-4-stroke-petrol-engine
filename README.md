# Emission Characteristics of Ethanol Blended with Brown’s Gas in a 4-Stroke Petrol Engine — Third Year Project

**Author:** Akash P Raj (USN: 4SN16ME012)  
**Department:** Mechanical Engineering, Srinivas Institute of Technology, Mangaluru  
**Guide:** Prof. Sudheendra H N (Assistant Professor)  
**Duration:** June 11 – July 15, 2018 (1 month)

---

## 📖 Project Overview
I investigated the **emission characteristics and performance** of a 4-stroke spark-ignition (petrol) engine when supplied with **ethanol** blended with **Brown’s gas (HHO)**. The work included a petrol-only baseline, integration of an on-board **HHO generator**, and comparative trials with **ethanol + HHO** enrichment to observe impacts on **CO, HC, NOx** trends, mileage behavior, and combustion stability.

> **Goal:** Evaluate whether partial HHO inclusion with ethanol enrichment can promote more complete combustion and reduce harmful exhaust constituents while maintaining drivability.

---

## 🧪 Experimental Setup (Summary)
- **Test platform:** Single-cylinder, 4-stroke SI motorcycle engine (Bajaj Avenger 180 DTS-i platform)  
- **Baseline:** Petrol-only, stock configuration  
- **HHO system:** Plate-type electrolyzer (battery-powered), bubbler/flashback arrestor, metered upstream of carb/throttle  
- **Ethanol enrichment:** Ethanol vapor carried with H₂/O₂ stream (representative enrichment ≈ **30% ethanol : 70% H₂** within the enrichment flow)  
- **Observations:** Qualitative CO/HC/NOx trends, mileage trend, engine smoothness, and oil cleanliness

---

## 🏍️ Bike Specifications (Table 4.1)
| Attribute          | Value                           |
|-------------------|----------------------------------|
| Model             | Bajaj Avenger 180 DTS-i          |
| Year              | 2007                              |
| Category          | Cruiser                           |
| Displacement      | 180.00 cc (10.98 cu in)          |
| Engine Type       | Single-cylinder, four-stroke      |
| Max Power         | 16.50 HP @ 8000 rpm              |
| Max Torque        | 15.22 Nm                          |
| Valves/Cylinder   | 1                                 |
| Fuel System       | Injection                         |
| Fuel Control      | Overhead Cams (OHC)              |
| Fuel Capacity     | 14.00 L                           |
| Reserve Tank      | 3.40 L (0.90 gal)                 |
| Starter           | Electric & kick                   |

---

## 🔧 Methodology (Steps)
1) Test petrol-only baseline (no HHO).  
2) Fabricate HHO generator.  
3) Install HHO system and connect to battery.  
4) Route generated H₂ to intake/carb.  
5) Mix ethanol vapor with H₂ (**≈30% ethanol : 70% H₂** in enrichment flow).  
6) Feed enrichment to intake.  
7) Run trials and note emission & efficiency trends.  
8) Record the most economical ethanol:H₂ enrichment ratio.

---

## 🧮 Design Notes & Calculations

### 1) Electrolysis & Combustion (facts)
- **Electrolysis:** `2 H₂O → 2 H₂ + O₂`  
- **Combustion:**  `2 H₂ + O₂ → 2 H₂O`  
- **Hydrogen flammability range in air:** ~**4%–95%** (vol.)  
- **Typical ignition temperature (stoichiometric H₂/O₂ mix):** ~**570 °C**  
- **Spark ignition energy (stoich H₂/O₂):** ~**20 µJ**

> These inform safe metering and why small H₂ additions can stabilize ignition and reduce incomplete combustion.

---

It’s Faraday’s law in math form.
Current 
𝐼
I tells you how many electrons/second you’re pushing. Making one H₂ molecule needs 2 electrons, so the H₂ mole rate is 
𝑛
˙
𝐻
2
=
𝐼
/
(
2
𝐹
)
n
˙
H
2
	​
=I/(2F) where 
𝐹
F (Faraday’s constant) converts coulombs → moles of electrons.

From moles to liters.
One mole of gas is ~22.414 L at STP. Multiply by that and by 60 (seconds→minutes) to get LPM:

𝑉
˙
𝐻
2
(
LPM
)
=
𝐼
2
𝐹
×
22.414
×
60
V
˙
H
2
	
(LPM)=
2F
I
	​
×22.414×60

The “dot” over 
𝑛
n means a rate (per second).
It’s standard notation in engineering: 
𝑛
˙
n
˙
 = moles per second.

The 0.00697 factor is just those constants multiplied together (at STP and 100% efficiency), giving a handy rule:

H₂ LPM
≈
0.00697
×
𝐼
(
A
)
H₂ LPM≈0.00697×I(A)

(At ~25 °C, replace 22.414 with 24.465 L/mol, so the factor ≈ 0.00761.)

Efficiency term 
𝜂
𝐹
η
F
	​

 is there because real cells aren’t 100% efficient; you can scale the ideal result by your estimated efficiency.

Why LaTeX in the README?
GitHub Pages/Markdown supports math blocks, so this renders cleanly and looks professional. If you prefer, we can use a plain-text version.

---

### 3) Electrical Load & Alternator Check (template)
**Cell power draw:** \(P=V\times I\).  
Example at **12 V, 10 A** → \(P\approx120\ \mathrm{W}\).  
Ensure alternator/regulator can supply **P_cell + vehicle loads** without excessive voltage drop. Use a fused line and relay.

---

### 4) Enrichment Mixing (ethanol : H₂ in enrichment gas)

Representative enrichment (by volume in enrichment stream): **30% ethanol : 70% H₂**.

| Stream              | Vol. Share | Notes                                  |
|---------------------|:----------:|----------------------------------------|
| Hydrogen (H₂)       |    70%     | From electrolyzer                      |
| Ethanol vapor       |    30%     | Metered/evaporated into intake         |
| *Carrier air/O₂*    |   small    | From intake; ensure safe backflow check|

> Keep total enrichment rate conservative; verify idle stability and throttle response after each change.

---

### 5) Gasoline Flammability Context
- **Gasoline flammability range:** ~**1.4%–7.6% (vol.)** vapor in air.  
- Excess vapor → **unburned HC**, **CO**, and smoke rise; H₂ enrichment can assist ignition near lean conditions.

---

## ✅ Advantages
- Potential **CO/HC reduction** trends from more complete combustion  
- Possible **mileage improvement** at light/medium loads due to stabilized flame speed  
- Low-mass add-on; reversible integration to intake  
- **Ethanol** is cleaner and renewable; partially offsets fossil fuel use

## ⚠️ Disadvantages / Limitations
- Benefits are **operating-point dependent**; may diminish at high load or rich mixtures  
- Electrolyzer imposes **electrical load**; efficiency/maintenance depend on water/electrolyte quality  
- Requires careful metering and safety checks (bubbler/flashback protection)  
- Without full instrumentation, results are **trend-based**, not certification-grade

## 🔭 Scope for Future Work
- Closed-loop HHO flow control linked to load/speed (MAP/TPS feedback)  
- Improved ethanol vaporization control and cold-start strategy  
- Certified **5-gas analyzer** + chassis-dyno A/B testing for quantified results  
- ECU/jetting calibration tailored for ethanol/HHO assisted operation

---

## 📅 One-Month Timeline (June 11 – July 15, 2018)
- **Week 1:** Problem statement, safety plan, literature survey, petrol baseline checks  
- **Week 2:** HHO electrolyzer fabrication, bench tests; intake plumbing & safety devices  
- **Week 3:** Ethanol vapor enrichment setup; blended operation trials; data logging  
- **Week 4:** Consolidation of observations; documentation; images/diagrams; final report

---

## 📚 References
1. TS De Silva, L. Senevirathne, T. D. Warnasooriya — *HHO Generator — An Approach to Increase Fuel Efficiency in Spark Ignition Engines.*  
2. Daniel M. Madyira, Wayne G. Harding — *Effect of HHO on Four Stroke Petrol Engine Performance.*  
3. Dhananjay Babariya, Jay Oza, Bhavin Hirani, Gaurang Akbari — *An Experimental Analysis of S.I Engine Performance with HHO as a Fuel.*  
4. Ammar A. Al-Rousan — *Reduction of Fuel Consumption in Gasoline Engines by Introducing HHO Gas into Intake Manifold.*  
5. Website: **www.ejaet.com**  
6. Website: **www.viva-technology.org**  
7. Website: **www.kscst.iisc.ernet.in**  
