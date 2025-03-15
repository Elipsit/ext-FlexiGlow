# ext-FlexiGlow LED Guide
 FlexiGlow Wearable Hexagon Neopixels

# FlexiGlow LED Guide

![FlexiGlow Logo](https://github.com/Elipsit/ext-FlexiGlow/blob/main/pics/10-IMG_2035%20Copy.JPG)

## 📌 Overview
FlexiGlow is a flexible PCB LED module designed for costumes and sci-fi-themed projects. This guide covers the design, assembly, and usage of the FlexiGlow LEDs, including schematics, PCB files, and build instructions.

## 📜 Features
- 🌟 Flexible PCB with addressable LEDs
- 🔧 Compact design with daisy-chain support
- ⚡ Powered via 5V supply
- 📷 Customizable lighting effects via WLED

## 📷 Project Gallery
Here are some images showcasing the design and final assembly of the FlexiGlow LED module.

### Schematics:
![Schematic](docs/images/schematic.png)

### PCB Layout:
![PCB Layout](docs/images/pcb_layout.png)

### Assembled Module:
![Assembled](docs/images/assembled_module.png)

## 🛠️ Bill of Materials (BOM)
| Part | Quantity | Description |
|------|----------|-------------|
| WS2812B LED | 25 | Addressable LEDs |
| Capacitor 100µF | 1 | Power stabilization |
| Resistor 330Ω | 1 | Data line protection |
| Flexible PCB | 1 | Custom design |

## 📥 Download Files
The PCB design and schematics are available in the `hardware/` folder.

- **[Schematic PDF](hardware/schematic.pdf)**
- **[PCB Gerber Files](hardware/gerbers.zip)**
- **[BOM File](hardware/bom.csv)**

## 🔨 Assembly Instructions
1. **Solder the LEDs** – Align and solder the WS2812B LEDs onto the flexible PCB.
2. **Attach Capacitor & Resistor** – Place the capacitor near the power input and the resistor on the data line.
3. **Test the Circuit** – Connect to a microcontroller and verify LED functionality.
4. **Encapsulation (Optional)** – Use a silicone conformal coating for protection.

## 📥 Installation & Code
```sh
# Clone the repository
git clone https://github.com/your-username/FlexiGlow.git
cd FlexiGlow

# Install dependencies
pip install adafruit-circuitpython-neopixel
```

### Example Code
```python
import board
import neopixel

pixels = neopixel.NeoPixel(board.D6, 25, brightness=0.5, auto_write=True)

pixels.fill((255, 0, 0))  # Set all LEDs to red
```

## 🤝 Contributing
Contributions are welcome! If you have improvements or want to add features, fork the repo and submit a PR.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

📌 **Tip:** Store your images in `docs/images/` for easy reference and organization.
