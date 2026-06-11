# ALPHA OneROM CN2 Adapter

## Overview

The **ALPHA OneROM CN2 Adapter** is designed for use with **Piers OneROM Fire 28** when running **ALPHA Emu firmware**.

This adapter allows datalogging from the Honda OBD1 ECU **CN2 pin header** through the OneROM using the **SEL pins**.

The OneROM SEL pin header is **not 5V tolerant**. Since the ECU CN2 TX signal can be 5V logic, this adapter level shifts the ECU CN2 TX line down to **3.3V** so it can safely interface with the OneROM.

## Purpose

The purpose of this adapter is to provide a safe and clean way to connect the Honda OBD1 ECU CN2 datalogging header to the OneROM SEL pins while running ALPHA Emu firmware.

Instead of connecting the ECU CN2 TX line directly to the OneROM, this adapter protects the OneROM by reducing the signal voltage from 5V to 3.3V.

## Compatibility

This adapter is intended for:

- Piers OneROM Fire 28
- ALPHA Emu firmware
- Honda OBD1 ECUs with a CN2 datalogging header
- USDM Honda OBD1 ECUs
- JDM Honda OBD1 ECUs

The PCB is designed to fit both **JDM** and **USDM** ECU layouts. Each input header is labeled for the ECU style it is intended to be used with.

## Important Warning

The OneROM SEL pins are **not 5V tolerant**.

Do **not** connect the ECU CN2 TX line directly to the OneROM SEL header.

Doing so may damage the OneROM hardware.

This adapter level shifts the ECU CN2 TX signal from 5V to 3.3V before it reaches the OneROM SEL pins.

## Connections

The adapter connects to the Honda ECU CN2 header and routes the datalogging signal to the OneROM SEL pins.

The adapter connects to the OneROM using standard breadboard / Arduino-style jumper wires.

Use the header labeled for your ECU style:

```text
USDM
JDM
