# C3-Macropad
A ESP32-C3 based macropad which has 4 mechanical keys and a 128x64 oled

Features:
- 4 programmable Cherry MX mechanical switches
- 0.91" OLED display (SSD1306, I2C)
- USB serial communication (bidirectional)
- ESP32-C3 Super Mini (WiFi/BLE capable)
- Custom PCB design (KiCad)

Hardware required:
- ESP32-C3 Super Mini
- 0.91" OLED display (SSD1306, I2C)
- 4x Cherry MX mechanical switches (any color)
- 4x Keycaps
- Custom PCB (design in progress)

  ## 🛠️ Software Setup

### Arduino IDE
1. Add ESP32 board URL: `https://espressif.github.io/arduino-esp32/package_esp32_index.json`
2. Install `esp32` platform via Boards Manager
3. Select board: `Nologo ESP32 C3 Super Mini`
4. Set `USB CDC On Boot` to **Enabled**

### PlatformIO
Add these build flags to `platformio.ini`:
```ini
[env:esp32c3_supermini]
platform = espressif32
board = esp32-c3-devkitm-1
build_flags =
  -D ARDUINO_USB_MODE=1
  -D ARDUINO_USB_CDC_ON_BOOT=1

