---

tags: [comptia-aplus, core1, chapter2, hardware]

exam: 220-1201

status: reviewed

---

  

# Chapter 2 — Expansion Cards, Storage Devices & Power Supplies

  

## Expansion Cards

  

- **Video cards** — dedicated GPU, own VRAM, PCIe x16 typical

- **Multimedia** — sound cards, capture cards

- **Network Interface Cards (NIC)** — PCIe x1 cards are common, cheap fix for failed onboard NIC

  - Best practice: don't replace whole motherboard for a single failed component if a card solves it

- **I/O cards** — additional USB, serial, etc.

- **Adapter configuration** — driver installation, resource allocation (legacy IRQ concepts still tested)

  

## Storage Devices

  

### Hard Disk Drives (HDD)

- **RPM** = rotational speed of platters → affects seek/access time, NOT capacity

  - Common values: 5400 RPM (laptops, quieter/cooler), 7200 RPM (desktop standard), 10K-15K RPM (enterprise)

- Capacity depends on platter density/count — unrelated to RPM

  

### Solid State Drives (SSD)

- **SATA SSD** — same protocol/speed ceiling as SATA HDDs (~600 MB/s), can be 2.5" or M.2 form factor

- **NVMe SSD** — uses PCIe protocol via M.2 slot (or PCIe card) — much faster than SATA

  - ⚠️ M.2 connector shape can be SATA OR NVMe — same look, different protocol/speed

- **TRIM command** — tells SSD which blocks are free so it can garbage-collect proactively

  - Prevents write-speed degradation as drive fills up

  - Do NOT defrag SSDs — unnecessary wear, no seek-time benefit

  

### RAID Levels

  

| RAID | Min Drives | Usable Capacity | Fault Tolerance |

|---|---|---|---|

| RAID 0 | 2 | 100% (striping) | None |

| RAID 1 | 2 | 50% (mirroring) | 1 drive |

| RAID 5 | 3 | (n-1)/n — one drive's worth lost to parity | 1 drive |

| RAID 6 | 4 | (n-2)/n — two drives' worth lost to dual parity | 2 drives |

| RAID 10 | 4 (even #) | 50% (mirrored + striped) | 1 per mirrored pair (not 2 in same pair) |

  

- RAID 5 = best redundancy-to-overhead ratio for general use (improves as drives increase)

- RAID 10 = fast AND redundant, but ~50% overhead and needs even drive count

- RAID 10 "can survive 2 failures" is only true if they're in **different** mirrored pairs

  

## Power Supplies (PSU)

  

### Connectors

  

| Connector | Purpose |

|---|---|

| 24-pin ATX | Main motherboard power |

| 4-pin / 8-pin EPS12V | Dedicated CPU power (separate from 24-pin) |

| 6-pin / 8-pin PCIe | Supplemental GPU power (slot itself supplies up to 75W) |

| SATA power (15-pin, flat) | Storage devices, some peripherals |

| Molex (4-pin) | Legacy drives/fans |

  

- High-end GPUs may need multiple 8-pin connectors or newer 12VHPWR/12V-2x6 connector

- Some boards have BOTH 4-pin and 8-pin EPS12V — high-power CPUs may want both populated

  

### Efficiency Ratings (80 Plus)

- Measures **AC→DC conversion efficiency** at various load levels (20%/50%/100%)

- Tiers: Bronze < Silver < Gold < Platinum < Titanium

- Gold ≈ 87-90%+ efficient — NOT about gold-plated connectors, NOT a warranty term

- Higher efficiency = less wasted heat = lower electric bill, especially for 24/7 lab servers

  

### Fans / Headers

- Motherboard fan headers have amperage limits (~1A typical)

- Y-splitters OK as long as combined draw stays under header rating

- SATA-to-fan adapters bypass motherboard fan control (no PWM speed control from board)

  

---

  

## 🎯 Exam Traps / Easy to Miss

- RPM affects speed/access time, NOT storage capacity

- M.2 slot ≠ NVMe automatically — could be SATA M.2

- TRIM = SSD performance maintenance; defrag = SSD performance HARM

- RAID 10 fault tolerance is conditional — not "any 2 drives"

- 80 Plus = efficiency rating, not a literal gold connector or extended warranty

- CPU gets power from EPS12V connector, separate from the main 24-pin