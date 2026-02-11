# OLED I2C Demo (`README.md`)

Project that demonstrates using an SSD1306 I2C OLED with an Arduino board. Source is in `src/main.cpp`.

## CLion
- IDE: `CLion`
- Tested version: `CLion 2025.3.2`
- Recommended workflow: open the project directory in CLion, configure an Arduino toolchain or PlatformIO integration, then build/upload using the configured run target.

## Code overview (`src/main.cpp`)
- Initializes I2C OLED display (128x64) using Adafruit libraries.
- On `setup()` it initializes the display, clears it, sets text size/color, prints a few lines and calls `display.display()`.
- `loop()` is currently empty (place repeating logic there).

## Libraries
- `Arduino.h`
- `Wire` (I2C)
- `Adafruit_GFX`
- `Adafruit_SSD1306`

Install these via Arduino Library Manager or your chosen build system.

## Dependencies
- Arduino core for your board (install via Arduino CLI / Board Manager).
- Adafruit SSD1306 library (compatible version for the Adafruit GFX library).
- Adafruit GFX library.
- I2C support (Wire library included in Arduino core).

## Components / Wiring for OLED (SSD1306 128x64 I2C)
- OLED module (SSD1306, 128x64)
- Connections:
  - `VCC` -> `3.3V` or `5V` (check your module voltage requirements)
  - `GND` -> `GND`
  - `SDA` -> board SDA pin (e.g., A4 on many UNO boards)
  - `SCL` -> board SCL pin (e.g., A5 on many UNO boards)
- Default I2C address used in code: `0x3C`
- Optional: pull-up resistors on SDA/SCL if module/board doesn't provide them.

## Software requirements
- `CLion 2025.3.2` (or newer)
- Arduino CLI or PlatformIO (to build and upload)
- Arduino board package for your target (UNO R4 or other)
- Installed libraries: Adafruit_SSD1306, Adafruit_GFX

## Hardware requirements
- Arduino board (example: `Arduino UNO R4`)
- SSD1306 I2C OLED 128x64
- USB cable for programming
- Jumper wires / breadboard as needed

## Build & Upload (brief)
1. Ensure Arduino CLI or PlatformIO is installed and configured in CLion.
2. Select the correct board (Arduino UNO R4) and serial port.
3. Build the project.
4. Upload to the board.

## Author
- `Oshiva09`
