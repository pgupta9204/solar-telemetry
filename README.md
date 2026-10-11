# Solar Telemetry (Sub-8g Wildlife Telemetry Node)

An ultra-lightweight ($<8.0\text{g}$) energy-autonomous telemetry beacon designed for wildlife tracking and environmental monitoring. Colloquially conceived as a "Solar AirTag", the system is engineered from the ground up for perpetual outdoor operation using solar harvesting rather than short-range BLE or disposable coin cells.

---

## Hardware Overview

The hardware design is located in [`solar-airtag-kicad/`](./solar-airtag-kicad):

* **Energy Harvesting PMIC:** e-peas AEM10941 (QFN-28) with flexible solar input and rechargeable buffer management.
* **Microcontroller & Radio:** STMicroelectronics STM32WL55 (UFQFPN-48) with integrated Sub-GHz radio transceiver (868 / 915 MHz).
* **Motion / Wake-up Sensor:** STMicroelectronics LIS2DW12 ultra-low-power 3-axis accelerometer for motion-triggered telemetry bursts.
* **Antenna Network:** $50\Omega$ tuned $\Pi$-matching network to an $8.2\text{cm}$ wire monopole.
* **Board Form Factor:** $20\text{mm} \times 25\text{mm}$, 4-layer FR4 stackup ($0.8\text{mm}$ thickness).

---

## Repository Structure

```
├── solar-airtag-kicad/      # KiCad 8+ schematic, PCB layout, and custom component libraries
│   ├── libraries/           # Footprints, symbols, and 3D step models (AEM10941, LIS2DW12TR)
│   ├── solar-airtag-kicad.kicad_sch  # Main system schematic
│   └── solar-airtag-kicad.kicad_pcb  # 4-layer PCB layout
├── .gitignore
└── README.md
```
