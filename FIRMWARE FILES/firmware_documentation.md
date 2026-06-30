# Macropad Firmware Documentation

## Overview

This firmware runs my 9-key macropad using a Seeed Studio XIAO RP2040 and KMK firmware.

It handles:

- 9 macro keys
- SSD1306 128×32 OLED display
- 9 daisy-chained NeoPixel RGB LEDs
- Rotary encoder for volume control

Everything works together to handle input, visual feedback, and media controls.

---

## Hardware

### Microcontroller

- Seeed Studio XIAO RP2040

### Display

- SSD1306 OLED (128×32, I2C)
- Address: `0x3C`
- Custom framebuffer-based driver

### Input

- 3×3 key matrix (9 keys)
- Rotary encoder

### Output

- 9 NeoPixel RGB LEDs connected in a single chain

---

## Pin Mapping

### Key Matrix

- Columns: GP26, GP27, GP28
- Rows: GP4, GP2, GP1
- Diode orientation: `COL2ROW`

### OLED (I2C)

- SDA: GP6
- SCL: GP7
- I2C Speed: 400 kHz

### Encoder

- A: GP29
- B: GP0

### NeoPixel

- Data: GP3
- 9 LEDs

---

## Key System

Each key has:

- A label
- A macro or keyboard shortcut
- A color
- A bitmap for the OLED
- An LED index

### Current key actions

- Screenshot tools
- Open Chrome
- Reopen closed tab
- Force Quit
- Lock screen
- Full screenshot
- Open Spotify
- Play/Pause
- Spotlight Search

---

## Key Press Behavior

When a key is pressed:

1. The OLED animation starts.
2. The LED animation begins.
3. The macro or shortcut runs.
4. The matching bitmap is shown on the OLED.

When the key is released:

- The LEDs clear with the reverse animation.

---

## OLED System

The OLED uses a custom framebuffer-based driver.

### Features

- Text rendering
- 128×32 bitmap rendering
- Direct I2C updates

---

## OLED Animation States

### Idle

- Shows the current time in `HH:MM`
- Shows the date below the time
- Slightly moves the text to keep the screen from looking static

### Slide In

- The bitmap slides in from the right.

### Hold

- The bitmap stays on screen for about 10 seconds.

### Fade Out

- The bitmap clears with a pixel wipe animation.
- The display returns to the clock.

---

## LED System

The LED system controls all 9 NeoPixels.

### Behavior

- All LEDs stay off while idle.
- Pressing a key starts an animation.
- Every key has its own RGB color.

### On Key Press

- LEDs light up one at a time from LED 0 to the selected key.

### On Key Release

- LEDs turn off one at a time back to LED 0.

### How it Works

- The animation runs inside the main keyboard scan loop.
- It doesn't block key presses while it's running.

---

## LED Animation Engine

The LEDs use a simple time-based animation.

### Fill Animation

- LEDs turn on from left to right.
- Each LED uses that key's assigned color.

### Clear Animation

- LEDs turn off from right to left.

### Timing

- The animation updates using timed intervals.
- No blocking delays are used.

---

## Rotary Encoder

The rotary encoder controls system volume.

- Rotate left → Volume Down
- Rotate right → Volume Up
- Press (if enabled) → Mute

---

## Macros

Some keys run multiple actions instead of a single shortcut.

### Spotify

- Opens Spotlight
- Types `spotify`
- Opens Spotify

### Chrome

- Opens Spotlight
- Opens Chrome
- Selects the correct profile

---

## Performance

### OLED

- The display only updates when it needs to.
- Animations control when each frame is drawn.

### LEDs

- LED animations run inside the keyboard scan loop.
- They don't block the rest of the firmware.

---

## System Flow

1. A key is pressed.
2. The macro or shortcut runs.
3. The OLED animation starts.
4. The LED animation starts.
5. The encoder continues handling volume independently.

---

## Summary

This firmware brings everything together into one system.

It includes:

- 9 programmable macro keys
- OLED animations
- RGB LED feedback
- Rotary encoder volume control

Everything runs together so the macros, display, LEDs, and encoder all stay in sync.
