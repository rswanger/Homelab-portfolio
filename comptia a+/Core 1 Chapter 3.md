---

tags: [comptia-aplus, core1, chapter3, hardware]

exam: 220-1201

status: reviewed

---

  

# Chapter 3 — Peripherals, Cables & Connectors

  

## USB Standards & Speeds

  

| Standard | Speed | Notes |

|---|---|---|

| USB 1.1 | 12 Mbps | Legacy |

| USB 2.0 (Hi-Speed) | 480 Mbps | Backward compatible — USB 3.0 device in 2.0 port works, just at this speed |

| USB 3.0 / 3.1 Gen1 (SuperSpeed) | 5 Gbps | Blue port |

| USB 3.1 Gen2 (SuperSpeed+) | 10 Gbps | Teal port |

| USB 3.2 Gen2x2 | 20 Gbps | |

| USB4 | 40 Gbps | |

  

- Backward compatibility is electrical AND physical — older port pins are a subset of newer ones

- No voltage mismatch issues mixing USB 2.0/3.0 devices and ports

  

## USB Connector Shapes

  

| Connector | Description / Common Use |

|---|---|

| Standard-A | Flat rectangular — host/computer end |

| **Standard-B** | Square w/ beveled top corners — **printers, scanners** |

| Mini-B | Small trapezoidal — older cameras, MP3 players |

| Micro-B | Thin, small — older Android phones |

| USB-C | Oval, reversible — modern devices |

  

⚠️ Don't confuse Standard-B (printer connector) with Mini-B (small trapezoidal, older portable devices)

  

## Video Connectors

  

- **DVI** (DVI-D, DVI-A, DVI-I) — **video only, no audio** — common trap on exam

- **HDMI** — digital video + audio, single cable

- **DisplayPort / Mini DisplayPort** — digital video + audio

- **VGA** — analog, legacy

- **Thunderbolt 3/4** — uses **USB-C connector shape**; can carry DisplayPort signal (DP Alt Mode) for driving external displays

  - Thunderbolt 1/2 used Mini DisplayPort shape, NOT USB-C

  

### Adapter Rules

- **Passive adapters** only work between same signal type (e.g., DisplayPort↔HDMI, both digital)

- **Active adapters** (contain a chip) required to convert between analog ↔ digital (e.g., HDMI→VGA)

  - A "simple cable" cannot do digital-to-analog conversion — needs active circuitry

  

## Audio (3.5mm Jacks)

  

| Color | Function |

|---|---|

| **Green** | Line-out / front speakers (main output) |

| **Pink** | Microphone input |

| **Blue** | Line-in (auxiliary input) |

| Orange | Subwoofer/center (surround) |

| Black | Rear surround speakers |

| Gray | Side surround speakers |

  

⚠️ Green = output, Blue = input — easy to mix up

  

## Storage Cables & Connectors

  

- **SATA data connector** — flat, L-shaped 7-pin, keyed so it can't be inserted wrong

- **SATA power connector** — wider, flat 15-pin (different from data connector)

- **PATA/IDE ribbon cable** — wide flat ribbon, 40-pin connector, 40 or 80 conductor wires (80-wire = extra grounds for higher speed modes)

  

## Wireless Peripherals

  

- 2.4GHz band shared by Bluetooth, many wireless dongles, AND Wi-Fi

  - Crowded spectrum near other 2.4GHz devices → interference → input lag/dropped keystrokes on wireless keyboards/mice

  - Some premium peripherals use 5GHz or dedicated RF to avoid this

  

## Laser Printer Process (order matters!)

  

1. **Processing** — image rasterized into printer memory

2. **Charging** — drum charged (~ -600V)

3. **Exposing** — laser writes image, discharges exposed areas

4. **Developing** — toner sticks to discharged areas

5. **Transferring** — toner moves to paper (paper given opposite charge)

6. **Fusing** — heat + pressure bonds toner to paper

7. **Cleaning** — excess toner removed from drum

  

Mnemonic: **P**our **C**heap **E**lection **D**onuts **T**o **F**lorida **C**ounties

  

---

  

## 🎯 Exam Traps / Easy to Miss

- DVI carries NO audio (regardless of variant) — classic "no sound over video cable" answer

- Green = audio OUT, Blue = audio IN (opposite of what many assume)

- Standard-B = printer connector; Mini-B = old portable device connector (don't swap these)

- Active vs passive adapters — analog↔digital conversion ALWAYS needs active (powered) hardware

- Thunderbolt version matters for connector shape (3/4 = USB-C, 1/2 = Mini DisplayPort)

- SATA has TWO different connectors — 7-pin data (L-shaped) vs 15-pin power (flat, wider)