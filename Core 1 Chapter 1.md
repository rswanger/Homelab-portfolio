---

tags: [comptia-aplus, core1, chapter1, hardware]

exam: 220-1201

status: reviewed

---

  

# Chapter 1 — Motherboards, Processors & Memory

  

## Motherboard Form Factors

  

| Form Factor | Size (approx) | Notes |

|---|---|---|

| ATX | 12" x 9.6" | Standard full-size desktop board |

| microATX | 9.6" x 9.6" | Shares top-left mounting holes with ATX |

| Mini-ITX | 6.7" x 6.7" | Compact builds, single expansion slot |

| E-ATX | Larger than ATX | High-end workstations/servers, more slots |

| Nano-ITX | Smaller than Mini-ITX | Embedded systems |

  

## System Board Components

  

- **Chipset** — manages communication between CPU and other components

  - **Northbridge** (legacy) — handled CPU ↔ RAM ↔ PCIe/AGP (high-speed)

  - **Southbridge** (legacy) — handled USB, audio, SATA, legacy ports (slower)

  - Most Northbridge functions now built into the CPU itself

- **I/O Shield** — metal plate for rear port cutout; provides EMI shielding + alignment. Install *before* mounting motherboard.

- **CMOS / BIOS battery** — CR2032 coin cell, maintains BIOS settings + system clock when powered off

- **CMOS reset** — jumper or button near battery; shorts pins to clear BIOS settings (incl. forgotten passwords)

- **Expansion slots** — PCIe x1/x4/x8/x16

  - A smaller card (x1) CAN physically fit in a larger slot (x16) — runs at its own native speed

  - A larger card generally CANNOT fit in a smaller physical slot

  

## CPU Architecture

  

- **Cores/Threads** — physical cores vs. logical threads (hyperthreading/SMT)

- **Cache hierarchy**:

  - **L1** — smallest, fastest, closest to core, often split instruction/data

  - **L2** — larger, slightly slower, often per-core

  - **L3** — largest, slowest of the three, typically shared across all cores

  - Rule: further from core = larger but slower

- **Sockets** — must match CPU and motherboard (e.g., LGA for Intel, AM5 for AMD)

  

## CPU Characteristics

  

- **Clock speed** — base frequency (GHz)

- **TDP (Thermal Design Power)** — guideline for cooling solution sizing; reflects heat output under *typical sustained* load

  - NOT a hard power ceiling — boost/turbo can exceed TDP briefly

  - Insufficient PSU wattage for TDP under load → system throttles clock speed even with good cooling

- **Integrated GPU** — built into CPU die, no discrete graphics card needed for basic display

  

## Memory (RAM)

  

### Types

- **DDR3** — 240-pin DIMM, 1.5V

- **DDR4** — 288-pin DIMM, 1.2V

- **DDR5** — 288-pin DIMM, 1.1V, higher bandwidth

- **SODIMM** — laptop form factor (smaller, fewer pins)

  

### Key Concepts

- **ECC RAM** — extra parity chip detects/corrects single-bit errors; used in servers/workstations

  - Requires CPU + motherboard that support ECC

  - Often slightly slower due to error-checking overhead

- **Dual/Quad Channel** — increases memory bandwidth

  - Match RAM into **same-colored slots** on the motherboard to enable dual-channel

  - Adjacent slots are often *different* channels — don't assume adjacent = paired

  - Requires matched sticks (capacity, speed, timings) ideally

  

## Cooling Systems

  

- **Thermal paste** — fills microscopic air gaps between CPU and heatsink for better heat transfer (NOT insulation, NOT adhesive)

  - Thin, even layer or small pea-sized dot — too much is a common mistake

- **Case fans / CPU cooling** — air vs. liquid (AIO) cooling

- **Cooling other components** — chipset heatsinks, VRM cooling on high-end boards

  

---

  

## 🎯 Exam Traps / Easy to Miss

- microATX shares ATX's top-left mounting holes — useful for compatibility

- TDP ≠ max power draw; it's a cooling design target

- PCIe x1 card in x16 slot = works fine, just runs at x1 speed (common "gotcha")

- I/O shield must go in BEFORE the motherboard — easy to forget

- ECC is about error correction, NOT speed — don't confuse with performance RAM