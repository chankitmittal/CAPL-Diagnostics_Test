## Overview
This repository contains a comprehensive, reusable library of generic CAPL functions designed for Unified Diagnostic Services (UDS - ISO 14229) testing. 

These scripts are written to be easily integrated into Vector CANoe. By using these generic functions, you can quickly automate diagnostic testing, request standard UDS services, and handle sub-functions without writing raw byte arrays from scratch.

This is a working repository. In the future, more functions will be added to test NRCs, different scenarios to test robustness of diagnostic services.

## 🛠️ Supported UDS Services

This library currently supports the following UDS services and their associated sub-functions:

| SID | Service Name | Description |
| :--- | :--- | :--- |
| **`0x10`** | Diagnostic Session Control | Switch between default, programming, and extended diagnostic sessions. |
| **`0x11`** | ECU Reset | Perform hard, key-off, or soft resets. |
| **`0x14`** | Clear Diagnostic Information | Clear active or stored DTCs. |
| **`0x19`** | Read DTC Information | Read DTCs by status mask, snapshot data, or extended data records. |
| **`0x22`** | Read Data By Identifier | Read specific DID (Data Identifier) values. |
| **`0x23`** | Read Memory By Address | Read data directly from physical memory addresses. |
| **`0x27`** | Security Access | Request seed and send key for unlocking the ECU. |
| **`0x28`** | Communication Control | Enable/disable normal or network management communication. |
| **`0x2E`** | Write Data By Identifier | Write data payloads to specific DIDs. |
| **`0x31`** | Routine Control | Start, stop, or request routine results. |
| **`0x34`** | Request Download | Initiate a data transfer from the tester to the ECU. |
| **`0x36`** | Transfer Data | Transmit data blocks (flashing/reprogramming). |
| **`0x37`** | Request Transfer Exit | Terminate a data transfer. |
| **`0x3D`** | Write Data by address | Write data directly from physical memory addresses. |
| **`0x3E`** | Tester Present | Keep the current diagnostic session active. |
| **`0x85`** | Control DTC Setting | Turn DTC logging on or off. |

## 💻 Prerequisites
* **Environment:** Vector CANoe (version 11 above).
* **Network:** Standard CAN/CAN FD/ Flexray setup with a configured Diagnostics Console or CDD/PDX database attached to the node.

## 🚀 How to Use

1. **Clone the repository:**
2. Create new tests/ Update existing test cases available in Main.can file.
3. Add CAN file into Test Module inside Test Envrionment in CANOE.

You can check Diag_lib.cin file for generic functions.

## 📄 License
Distributed under the MIT License.
