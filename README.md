# Recoil Control Utility [my recoil tool.txt]

## Tutorial

Watch calibration and advanced configuration tutorials on YouTube:
https://www.youtube.com/@kydn-iu5kd

## Overview

A configurable recoil control utility designed for tactical shooter games. The utility compensates for weapon recoil patterns by adjusting aim based on configurable vertical and horizontal values.

**Note:** Despite the `.txt` extension, this is a Lua utility.

## Requirements

- Lua 5.1+ compatible runtime environment
- A game with weapon recoil mechanics (e.g., Rainbow Six Siege, FPS games with predictable recoil)
- Knowledge of the specific weapon's recoil pattern for initial calibration

## Setup

1. Load the utility into Logitech G HUB.
2. Configure the settings in the utility header (see below).
3. Save and run.

## Configuration

### Basic Settings (top of utility)

```lua
ENABLE_RAMPING = false          -- Enable bullet ramping for first-shot kick
RAMP_DELAY_MS = 250             -- Milliseconds of heavy initial kick
FIRST_SHOT_RAMP = 0             -- Adjust if shots fly UP (increase) or DOWN (decrease)
```

### Weapon-Specific Calibration

Different weapons have different recoil patterns. Calibrate by:

1. Take the weapon into a Custom Match or Shooting Range.
2. Shoot a full magazine at a wall **without moving your mouse**.
3. Observe the crosshair drift:
   - **Drifts too high** → increase the `vert` value slightly
   - **Pulls too low** → decrease the `vert` value
   - **Drifts left** → decrease the `horizontal` value
   - **Drifts right** → increase the `horizontal` value (positive = pull right, negative = pull left)

### Default Optimization

The utility is optimized for:
- Sensitivity: 5-5
- Advanced settings: default
- Field of View (FOV): 84

## Usage

- The utility runs automatically when loaded.
- Toggle with the configured hotkey (check utility for `TOGGLE_KEY`).
- Adjust values in real-time during testing — changes apply immediately.

## Disclaimer

For educational purposes only. Use in private/custom games where permitted by the game's terms of service.
