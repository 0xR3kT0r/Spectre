# SPECTRE Firmware

Spectre is a portable firmware toolkit designed for educational and research purposes in wireless communication and embedded systems. It runs on microcontroller-based hardware with a TFT display and optional radio modules for experimenting with wireless signals, protocols, and device interaction in a controlled and legal environment.

---

## Overview

Spectre provides a structured interface for exploring wireless concepts, device interaction, and system monitoring using a clean, responsive UI. It is intended strictly for learning, testing, and development purposes on your own hardware.

---

## Purpose

This firmware is built for:

- Learning how wireless communication works
- Experimenting with embedded systems
- Testing RF modules in controlled environments
- Understanding device interfaces and protocols
- Building and extending custom tools for education

---

## Supported Hardware

### Microcontroller
- ESP32 (recommended)

### Display
- TFT Display (ILI9341 or compatible)
- Resolution: 240x320 (portrait mode recommended)

### RF Modules (Optional)
- CC1101 sub-GHz transceiver module
- NRF24L01+ 2.4GHz transceiver module

These modules are used for educational experimentation with wireless communication concepts.

---

## Pin Configuration

### TFT Display (TFT_eSPI)

Configured via `User_Setup.h`:

TFT_MOSI  -> GPIO 23 TFT_MISO  -> GPIO 19 TFT_SCLK  -> GPIO 18 TFT_CS    -> GPIO 15 TFT_DC    -> GPIO 2 TFT_RST   -> GPIO 4

---

### Buttons

SELECT   -> GPIO 25 UP       -> GPIO 26 DOWN     -> GPIO 27 BACK     -> GPIO 33

---

### CC1101 Module

MOSI -> GPIO 23 MISO -> GPIO 19 SCK  -> GPIO 18 CSN  -> GPIO 5 GDO0 -> GPIO 21

---

### NRF24L01+ Module

MOSI -> GPIO 23 MISO -> GPIO 19 SCK  -> GPIO 18 CE   -> GPIO 22 CSN  -> GPIO 5

---

## Features

- Modular menu-based interface
- Clean pink-themed UI
- Status bar with system indicators
- Scrollable navigation system
- Support for RF modules (NRF24 / CC1101)
- Smooth rendering optimized for TFT displays
- Organized input handling system
- Expandable feature structure

---

## UI Design

Spectre uses a minimal, modern interface:

- Dark background with pink accents
- Top status bar showing system state
- Scrollable menu with icons
- Simple navigation with buttons
- Clean layout optimized for small screens

---

## Project Structure

/src main.cpp menu.cpp menu.h input.cpp input.h ui.cpp ui.h config.h

/assets icons.h

---

## How It Works

- The menu system is built using structured arrays and function mappings
- Each menu item can:
  - Open a submenu
  - Call a function
  - Trigger a tool or module
- Input is processed separately for clean and responsive control
- The UI is rendered with minimal redraws to reduce flickering
- RF modules can be initialized and controlled through dedicated functions

---

## Wireless Modules (Educational Use)

### CC1101

The CC1101 is a sub-GHz transceiver used for experimenting with low-frequency wireless communication. It allows learning about:

- Frequency modulation
- Packet transmission
- Signal reception
- RF protocol behavior

---

### NRF24L01+

The NRF24L01+ is a 2.4GHz transceiver used for short-range wireless communication experiments:

- Peer-to-peer communication
- Packet-based data transfer
- Low-power wireless systems
- Network behavior simulation

---

## Usage Notes

- This firmware is intended for **educational and personal testing only**
- Always follow local laws and regulations regarding radio frequency usage
- Only use on hardware you own or have permission to test
- Do not interfere with external or public wireless systems

---

## Installation

1. Clone the repository:

git clone https://github.com/yourusername/spectre-firmware.git

2. Open in Arduino IDE or PlatformIO

3. Install required libraries:
- TFT_eSPI
- SPI
- Radio libraries (for CC1101 / NRF24 if used)

4. Configure:
- `User_Setup.h` for TFT display
- Pin definitions in `config.h`

5. Upload to ESP32

---

## Configuration

All main settings are found in:

- `config.h`  
- `menu.cpp`  
- `input.cpp`  

You can modify:

- Colors (pink theme variables)
- Menu structure
- Button mappings
- Module initialization

---

## Planned Features

- Advanced RF utilities (analysis tools)
- Improved UI animations
- Expanded settings menu
- Custom themes
- Logging and diagnostics tools
- Signal visualization

---

## Known Issues

- Some displays may experience minor flickering depending on refresh timing
- RF module performance depends on wiring quality and power stability
- Scroll behavior may require tuning for specific hardware

---

## Image Requirement

To properly present this project on GitHub, include:

### Required Images

1. Main menu screenshot (showing pink UI)
2. Submenu or tool screen (demonstrating navigation)
3. Status bar view (showing WiFi / battery indicators if used)
4. Hardware setup photo (ESP32 + TFT + RF module)

### Suggested File Paths

/assets/main_menu.png /assets/submenu.png /assets/status_bar.png /assets/hardware_setup.png

---

### Example Usage in README

```markdown
![Main Menu](assets/main_menu.png)
![Hardware Setup](assets/hardware_setup.png)


---

Safety & Legal Notice

This firmware is strictly for:

Education

Development

Personal experimentation


Do not use this firmware for any unauthorized or harmful activity. Always comply with local laws and regulations regarding wireless communication.


---

License

MIT License


---

Credits

Built for embedded system learning and experimentation with a focus on clean UI design and modular architecture.
