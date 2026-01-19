# Ku/Ka-Band FMCW Radar Front-End  
**From Theoretical System Specification to Hardware-Ready RF Design**

## Overview
This repository documents the end-to-end design of a dual-band Ku/Ka FMCW radar RF front-end, starting from an abstract theoretical block diagram and performance description and progressing through system architecture refinement, component trade studies, detailed RF simulation, and hardware procurement for experimental characterization.

The project emphasizes **system-level RF thinking**, **defensible design decisions**, and **simulation-driven validation**, closely mirroring real-world radar and microwave hardware development workflows.

The initial system concept and constraints were provided as a high-level theoretical description and simplified block diagram for a dual-band FMCW radar operating in the Ku (12–18 GHz) and Ka (32–38 GHz) bands :contentReference[oaicite:0]{index=0}.

---

## Radar System Summary
- **Architecture:** Dual-band FMCW radar (Ku + Ka)
- **Operation Mode:** FMCW with ultra-linear wideband chirps
- **Ku Band:** 12–18 GHz direct chirp generation
- **Ka Band:** 32–38 GHz via frequency upconversion
- **Polarization:** Dual-polarized (VV / HH and cross-pol paths)
- **Focus:** RF front-end design, not DSP or target processing

The system employs a shared chirp generation chain, separate transmit and receive antennas for isolation, and independent Ku- and Ka-band RF chains to evaluate performance tradeoffs across frequency bands.

---

## Project Objectives
- Translate a **theoretical radar block diagram** into a realizable RF architecture
- Develop a **hardware-feasible system partitioning** for Ku and Ka operation
- Perform **iterative component selection** based on RF performance, availability, and integration constraints
- Validate design decisions using **Keysight ADS**:
  - S-parameter simulations
  - Harmonic balance analysis for mixers and LO leakage
- Prepare a **hardware-ready design** suitable for experimental characterization

---

## Repository Structure

Each directory corresponds to a **distinct phase of engineering maturity**, from concept to hardware validation.

---

## Design Flow
1. **Initial System Interpretation**  
   Interpreted the provided theoretical block diagram and textual system description to extract frequency plans, power levels, isolation requirements, and IF constraints :contentReference[oaicite:1]{index=1}.

2. **Architecture Refinement**  
   Developed a more detailed block diagram with explicit gain stages, filtering, LO routing, and Ku/Ka differentiation.

3. **Component Trade Studies**  
   Evaluated candidate LNAs, PAs, mixers, filters, couplers, and switches with respect to:
   - Frequency coverage
   - Noise figure and linearity
   - Isolation and LO leakage
   - Availability and packaging constraints

4. **Simulation and Validation**  
   Used Keysight ADS to simulate:
   - Cascaded RF chain S-parameters
   - Mixer behavior using harmonic balance
   - Expected gain, isolation, and spur performance

5. **Hardware Procurement**  
   Selected X-Microwave-compatible components and generated a complete BOM for assembly and testing.

6. **Planned Characterization**  
   Defined a structured VNA and spectrum-analyzer-based measurement plan to compare measured results against simulations.

---

## Tools & Methods
- **Simulation:** Keysight ADS (S-parameters, harmonic balance)
- **RF Analysis:** Gain, noise, isolation, LO leakage, spur behavior
- **Hardware Platform:** X-Microwave modular RF components
- **Measurement Planning:** VNA-based characterization (planned)

---

## Current Status
- ✔ System architecture defined  
- ✔ Component selection completed  
- ✔ RF simulations completed  
- ✔ Hardware ordered  
- ⏳ Experimental characterization in progress  

Measured results and correlation with simulations will be added once testing is completed.

---

## What This Project Demonstrates
- System-level RF and radar architecture thinking  
- Practical component selection under real-world constraints  
- Simulation-driven design decisions (not datasheet-only design)  
- Understanding of FMCW radar RF challenges (LO leakage, isolation, spur control)  
- Ability to transition from theory → simulation → hardware  

---

## Notes
This repository is intentionally structured to reflect **professional RF design workflows**, not academic homework. Design decisions, tradeoffs, and assumptions are documented explicitly to make the engineering reasoning transparent.

---

## Author
**Colin Duckworth**  
Electrical Engineering — RF / Microwave Systems  
Graduating May 2026
