# ALPHA OneROM CN2 Adapter

## Overview

The **ALPHA OneROM CN2 Adapter** is designed for use with **Piers OneROM Fire 28** when running **ALPHA Emu firmware**.

This adapter allows datalogging from the Honda OBD1 ECU **CN2 pin header** through the OneROM using the **SEL pins**.

The Piers OneROM has **non-5V-tolerant pins** at the SEL pin header. Since the Honda ECU CN2 TX signal can be 5V logic, this adapter level shifts the ECU CN2 TX line from **5V to 3.3V** so it can safely interface with the OneROM.

## Purpose

The purpose of this adapter is to provide a safe and clean way to connect the Honda OBD1 ECU CN2 datalogging header to the OneROM SEL pins while running ALPHA Emu firmware.

Instead of connecting the ECU CN2 TX line directly to the OneROM, this adapter protects the OneROM by reducing the signal voltage from 5V to 3.3V.

## Compatibility

This adapter is intended for:

- Piers OneROM Fire 28
- ALPHA Emu firmware
- Honda OBD1 ECUs with a CN2 datalogging pin header
- USDM Honda OBD1 ECUs
- JDM Honda OBD1 ECUs

The PCB is designed to fit both **JDM** and **USDM** ECUs.

Each input header is labeled for the ECU style it is intended to be used with.

## Important Voltage Warning

The OneROM SEL pins are **not 5V tolerant**.

Do **not** connect the ECU CN2 TX line directly to the OneROM SEL header.

Doing so may damage the OneROM hardware.

This adapter level shifts the ECU CN2 TX signal from **5V to 3.3V** before it reaches the OneROM SEL pins.

## Connections

The adapter connects to the Honda OBD1 ECU CN2 pin header and routes the datalogging signal to the OneROM SEL pins.

The CN2 adapter connects to the OneROM using standard breadboard / Arduino-style jumper wires.

Use the input header labeled for your ECU style:

```text
USDM
JDM
```

Make sure the adapter is installed in the correct orientation for your ECU.

## Bill of Materials

| Quantity | Part | Notes |
|---:|---|---|
| 3 | 10K resistor, 0402 | 1/16W is fine |
| 1 | 2-pin header | 90-degree preferred |
| 1 | 5-pin female pin header | Used for ECU CN2 connection |
| 1 | 4-pin female pin header | Used for ECU CN2 connection |

## Assembly Notes

One of the pin headers will need to be trimmed down to fit at the 90-degree junction.

Take care when soldering the 0402 resistors. Inspect the board for solder bridges before connecting it to the ECU or OneROM.

Before powering anything on, verify continuity and confirm that the ECU CN2 TX signal is being level shifted to 3.3V.

## Usage

Install the adapter onto the ECU CN2 header using the input header labeled for your ECU style.

Connect the adapter to the OneROM SEL pins using breadboard / Arduino-style jumper wires.

Run the ALPHA Emu firmware on the OneROM.

Use the supported ALPHA Emu datalogging features to communicate with the ECU CN2 datalog port through the OneROM.

## Notes

This adapter is not a standalone datalogging device.

It is an interface adapter that allows the Honda OBD1 ECU CN2 datalog signal to be safely connected to the OneROM SEL pins.

The adapter does not modify the ECU.

The adapter is designed specifically around using the OneROM SEL pins with ALPHA Emu firmware.

## Disclaimer

Use this adapter at your own risk.

Always verify wiring, orientation, signal direction, and voltage levels before connecting to your ECU or OneROM.

Incorrect wiring may damage the OneROM, ECU, or connected hardware.
