# SPECTRE Firmware

SPECTRE is a firmware project for ESP32 that is made for learning and testing embedded systems and wireless communication. This project uses a TFT display with a simple pink and dark interface. It is made for educational purposes only and should only be used on devices you own or have permission to use.

---

## Purpose

This project is made to learn how embedded systems work, how microcontrollers interact with hardware, and how wireless communication works using modules like CC1101 and NRF24L01+. It also helps to learn how to build menus and user interfaces on small displays.

---

## Features

- Simple menu system  
- Pink and dark UI design  
- Scrollable navigation  
- Status bar display  
- Support for CC1101 module  
- Support for NRF24L01+ module  
- Button navigation  
- Organized code structure  

---

## Hardware

- ESP32  
- TFT display (ILI9341 or similar, 240x320)  
- Push buttons  
- Optional RF modules:
  - CC1101  
  - NRF24L01+  

---

## Wiring

### TFT Display

MOSI -> GPIO 23
MISO -> GPIO 19
SCK  -> GPIO 18
CS   -> GPIO 15
DC   -> GPIO 2
RST  -> GPIO 4

---

### Buttons

SELECT -> GPIO 25
UP     -> GPIO 26
DOWN   -> GPIO 27
BACK   -> GPIO 33

---

### CC1101

MOSI -> GPIO 23
MISO -> GPIO 19
SCK  -> GPIO 18
CSN  -> GPIO 5
GDO0 -> GPIO 21

---

### NRF24L01+

MOSI -> GPIO 23
MISO -> GPIO 19
SCK  -> GPIO 18
CE   -> GPIO 22
CSN  -> GPIO 5

---

## Setup

1. Install Arduino IDE or PlatformIO  
2. Install ESP32 board support  
3. Install TFT_eSPI library  
4. Set up display in `User_Setup.h`  
5. Configure pins in `config.h`  
6. Upload code to ESP32  

---

## Project Structure

/src main.cpp menu.cpp menu.h input.cpp input.h ui.cpp ui.h config.h

/assets icons.h

---

## UI

The UI uses a dark background with pink highlight color. The interface is simple and easy to read. It has a top bar for system status and a menu that can be scrolled using buttons.

---

## How It Works

The system starts and loads the UI. The menu is shown on the screen. The user moves through the menu using buttons. Each menu item can open a function or a submenu. The display updates when needed to keep performance smooth.

---

## Wireless Modules

### CC1101

This module is used for learning sub-GHz communication. It helps understand how signals are sent and received.

---

### NRF24L01+

This module is used for learning short range wireless communication. It helps understand how devices send data to each other.

---

## Notes

This project is for educational use only. Do not use it for illegal or harmful activities. Follow local laws when working with wireless devices.

---





---

## Future

- Add more tools  
- Improve UI  
- Add settings menu  
- Improve performance  

---

## Credits

- TFT_eSPI library  
- Arduino core for ESP32  
- SPI library  
- RF modules: CC1101, NRF24L01+  

Thanks to all tools and libraries used in this project.

---

## License

MIT License
