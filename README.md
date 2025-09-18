# Custom 5V Power Supply Circuit

A professionally designed **5V buck converter power supply** built around the [Texas Instruments TPS5430](https://www.ti.com/product/TPS5430).  
This circuit ensures a **stable and efficient 5V output** under varying load conditions, making it ideal for embedded systems, IoT projects, and other electronics requiring reliable regulation.

---

## 📖 Overview
This project provides a custom-designed **5V DC power supply module** implemented in Kicad **[Pictures ](https://github.com/AMAR124595/Buck-converter-5.v/tree/master/Image)**.  
It is optimized to deliver **up to 3A continuous output current** from a lithium battery pack (2S2P, 7.4V nominal) or other DC sources within the supported input range.

---

## ✨ Features
- ✅ Input voltage range: **6V – 36V** (tested with 2S Li-ion pack, 7.4V nominal, 8.4V max)  
- ✅ Regulated **5V output**, capable of delivering up to **3A**  
- ✅ Based on **TI TPS5430 step-down (buck) converter**  
- ✅ Incorporates **low-ESR polymer capacitor** for stable ripple performance  
- ✅ Compact SMD layout with optimized PCB grounding for thermal and electrical efficiency  
- ✅ Ideal for powering **ESP32, microcontrollers, sensors, and small audio circuits**

---

## ⚙️ How It Works
1. **Input Power**  
   - The circuit accepts power from a **2S Li-ion pack** (7.4V nominal, 8.4V fully charged) or other DC supplies up to 35V.  

2. **Buck Conversion (TPS5430)**  
   - The TPS5430 regulator steps down the input voltage to a stable 5V output.  
   - Switching frequency and inductor values are chosen for efficiency and low ripple.  

3. **Output Filtering**  
   - A combination of **ceramic capacitors** (high-frequency filtering) and a **bulk polymer capacitor (220µF, low ESR)** ensures clean output with minimal voltage ripple.  

4. **Enable Pin (EN)**  
   - Left floating by default → device enabled automatically.  
   - Can be tied to logic-level signals for power sequencing if required.  

---

## 🛠️ Tools Used
- **Schematic & PCB Design:** [The entire design and simulation process was completed using KiCad](https://github.com/AMAR124595/Buck-converter-5.v/tree/master) 
- **Datasheet Reference:** [Texas Instruments TPS5430 Datasheet](https://www.ti.com/lit/ds/symlink/tps5430.pdf)  
- **Simulation & Validation:** TI Webench, vendor application notes  
- **BOM Management:** Digi-Key / Mouser / Robu.in  

---

## 🧾 Component List (BOM)

Below is the list of major components used in this custom 5V power supply design:

| Component | Value / Spec | Package | Link |
|-----------|--------------|---------|------|
| C1        | 10 µF, 50V, X7R MLCC | 1210 | [Samsung CL32B106KBJNNWE](https://robu.in/product/cl32b106kbjnnwe-samsang-50v-10uf-x7r-%C2%B110-1210-multilayer-ceramic-capacitors-mlcc-smd-smt-rohs/?) |
| L1        | 15 µH, 3A (4A peak), Shielded Inductor | SRP7028CC | [Bourns SRP7028CC-150M](https://robu.in/product/srp7028cc-150m-bourns-srp7028cc-150m-power-inductor-smd-15-%C2%B5h-3-a-shielded-4-a-srp7028cc-series/?) |
| D1        | Schottky Diode, 40V, 3A | DO-214AC (SMA) | [Vishay B340A-E3/5AT](https://robu.in/product/b340a-e3-5at-vishay-intertech-40v-3a-550mv3a-do-214acsma-schottky-diodes-rohs/?) |
| C2        | 0.01 µF, 50V, C0G | 0805 | [Samsung CL21C103JBFNNNE](https://robu.in/product/cl21c103jbfnnne-samsung-cap-ceramic-0-01uf-50v-c0g-5-pad-smd-0805-125c-t-r/?) |
| U1        | DC-DC Buck Converter IC | SO PowerPAD-8 | [TI TPS5430DDAR](https://robu.in/product/tps5430ddar-so-powerpad-8-dc-dc-buck-step-down-switching-voltage-regulators/) |
| R1        | 3.24 kΩ, 1%, 0603 | 0603 | [Uniohm 0603WAF3241T5E](https://robu.in/product/0603waf3241t5e-uniohm-royal-ohm-100mw-thick-film-resistors-75v-%C2%B1100ppm-%E2%84%83%C2%B11-3-24k%CF%89-0603-chip-resistor-surface-mount-rohs/) |
| R2        | 10 kΩ, 1%, 0603 | 0603 | [0603 SMD Resistor Pack](https://robu.in/product/10k-ohm-1-4w-0603-surface-mount-chip-resistor-pack-of-100/?) |
| C3        | 220 µF, 10V, Low-ESR Polymer Capacitor | 2917 (7343) | [Panasonic 10TPB220M](https://www.digikey.com/en/products/detail/panasonic-electronic-components/10TPB220M/4204779) |

---

## 👤 Author
**Amar Gangadhar A (SenseAbility innovations pvt.ltd)**  
Electronics Engineer | Embedded Systems Designer |   Embedded Firmware Developer

---
