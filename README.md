# 🛰️ Instrument Simulator for REAL CubeSat (Flatsat)

> Teensy 4.1–based simulator of the **REAL CubeSat instrument**, enabling testing without needing physical flight hardware.  

## Project Purpose

This project implements an **instrument simulator** that emulates the behavior and data flow of the **REAL CubeSat** instrument. Uses the **Teensy 4.1 microcontroller**, to fake packet-based communication with the **On-Board Computer (OBC)** over serial, following CCSDS telemetry standards.

## Core Features

| Feature | Description |
|----------|-------------|
| **Command Interface** | Parses and CCSDS command packets from the OBC |
| **CRC Validation** | Implements 16-bit CCITT CRC with lookup optimization |
| **Heartbeat System** | Periodic “1 PPS” telemetry update and internal timekeeping |
| **State Machine Architecture** | FSM-based packet reception and handling |

## Acknowledgements

- Developed at the **Space Science Engineering Lab** at Montana State University.

- **Authors:**  
  Tyler Holliday, Connor Parrott, Andrew Johnson, Emma Stensland, Nevin Leh
