# RTL-to-GDS-8bit-Counter-Using-Cadence

A complete RTL-to-GDSII implementation of an 8-bit synchronous counter using the Cadence ASIC design toolchain. The project demonstrates the full digital ASIC flow from Verilog RTL and functional verification to synthesis, physical design, and final GDSII generation.

---

# Project Overview

This project demonstrates a complete ASIC RTL-to-GDSII implementation flow of an 8-bit synchronous counter using industry-standard Cadence EDA tools:

RTL Simulation – Cadence Incisive

Logic Synthesis – Cadence Genus

Physical Design – Cadence Innovus

The design is implemented from:

**RTL Design** → **Functional Verification** → **SDC Constraints** → **Synthesis** → **Physical Design** → **Routing** → **GDSII Generation**

---

# About the 8-Bit Counter

The design implements a synchronous 8-bit binary up-counter that:

Counts from 0 to 255 (8-bit range)

Increments on every positive clock edge

Supports reset functionality

Demonstrates sequential digital design principles

## Key Design Concepts

D Flip-Flop based register implementation

Synchronous sequential logic

Clock-driven state transitions

Binary increment logic

Reset handling

Timing constraints and analysis

---

# Folder Structure

```text
├── rtl/
│   └── counter.v
│
├── testbench/
│   └── counter_test.v
│
├── constraints/
│   └── constraints_sdc.sdc
│
├── scripts/
│   └── rcscript.tcl
│
├── gds/
│   └── counter.gds
│
├── results/
│   └── images/
│
└── README.md
```
---
# Detailed Design Flow
## 1️⃣ RTL Design

File: counter.v

Synthesizable Verilog code

8-bit register-based counter

Clean and modular coding style

Designed for ASIC synthesis compatibility

---

## 2️⃣ Functional Verification

File: counter_test.v

Testbench developed to validate:

Clock behavior

Reset functionality

Increment operation

Verified correct counting sequence

Waveform validation performed in Incisive

---

## 3️⃣ Timing Constraints

File: constraints_sdc.sdc

Includes:

Clock definition (create_clock)

Input/output delays (if defined)

Timing environment setup

Enables proper static timing analysis

This demonstrates understanding of:

Clock period selection

Timing budgeting

STA-driven synthesis

---

## 4️⃣ Logic Synthesis

Performed in Cadence Genus

Outputs generated:

Gate-level netlist

Area report

Timing report

Power estimation

Concepts applied:

Technology library mapping

Timing-driven optimization

Area vs performance trade-off

Slack analysis

---

## 5️⃣ Physical Design Flow

Implemented in Cadence Innovus

Using:

Netlist from Genus

SDC constraints

RC script (rcscript.tcl)

Physical Design Steps Performed

Floorplanning

Power planning

Standard cell placement

Clock Tree Synthesis (CTS)

Routing

Timing closure

GDSII generation

---

## 7️⃣ Final Layout & GDS

File: counter.gds

Final routed layout

DRC-clean implementation

Fabrication-ready design database

---


