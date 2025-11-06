# 🛰️ Instrument Simulator for REAL CubeSat (Flatsat)

> Teensy 4.1–based simulator for the **REAL CubeSat instrument**, enabling robust spacecraft integration testing without needing physical flight hardware.  

## 🎯 Project Purpose

This project implements an **instrument simulator** that emulates the behavior and data flow of the **REAL CubeSat** instrument.  
Running on a **Teensy 4.1 microcontroller**, it supports full packet-level communication with the satellite’s **On-Board Computer (OBC)** over UART, following CCSDS telemetry standards.

The simulator:
- Receives command frames from the OBC  
- Validates integrity with a **CRC-CCITT16** checksum  
- Responds with CCSDS-compliant telemetry frames  
- Emits periodic “1 PPS” status updates  
- Allows system debugging and validation *without needing the flight instrument hardware*

## 🧠 System Overview

- **Platform:** Teensy 4.1 (C++ / Arduino Core)
- **Communication:** UART (Serial2)
- **Protocol:** CCSDS Packet Standard  
- **Error Checking:** CRC-CCITT16  
- **Design Goal:** Mirror instrument state logic and communication timing of the actual payload

## ⚙️ Core Features

| Feature | Description |
|----------|-------------|
| **Command Interface** | Parses and executes CCSDS command packets from the OBC |
| **Telemetry Simulation** | Generates housekeeping & science packets |
| **CRC Validation** | Implements 16-bit CCITT CRC with lookup optimization |
| **Heartbeat System** | Periodic “1 PPS” telemetry update and internal timekeeping |
| **State Machine Architecture** | FSM-based packet reception and handling (`getData()` loop) |


## ✨ Acknowledgements

- Developed at the **Space Science Engineering Lab** at Montana State University.

- **Authors:**  
  Tyler Holliday, Connor Parrott, Andrew Johnson, Emma Stensland, Nevin Leh
