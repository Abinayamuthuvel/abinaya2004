# Interactive Python Code Generator for Arduino Control

## Project Overview
This project demonstrates the integration of SvelteKit, Blockly, and pyFirmata to create an interactive web-based application for generating Python code to control an Arduino. Users can visually program Arduino functionality using Blockly blocks, generate Python code, and execute it to control hardware components like LEDs and buttons.

---

## Features
- **Visual Programming Interface**: Drag-and-drop blocks using Blockly to create Arduino control programs.
- **Python Code Generation**: Automatically generate Python code based on block arrangements.
- **Custom Blocks**:
  - LED Control Block: Turns an LED on or off.
  - Delay Block: Pauses execution for a specified duration.
  - Button Control Block: Reads button input to control the LED.
- **Code Export**: Download the generated Python code as a `.py` file.
- **Arduino Control**: Execute Python scripts with pyFirmata to control Arduino hardware.

---

## Block Diagram
```plaintext
[User Interface (SvelteKit)]
          |
          v
[Blockly Workspace (Visual Programming)]
          |
          v
[Python Code Generator (Blockly)]
          |
          v
[Python Execution Environment (pyFirmata)]
          |
          v
[Arduino Hardware (LED, Button, etc.)]
```

---

## Requirements
### Software:
- [Node.js](https://nodejs.org/)
- [SvelteKit](https://kit.svelte.dev/)
- [Blockly](https://developers.google.com/blockly)
- [Python](https://www.python.org/)
- [pyFirmata](https://pypi.org/project/pyFirmata/)
- Arduino IDE (to upload the Firmata firmware)

### Hardware:
- Arduino board (e.g., Arduino Uno)
- LED
- Resistor (220Ω)
- Push button
- Breadboard and jumper wires

---

## Installation and Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Start the Development Server
```bash
npm run dev
```

### 4. Upload Firmata Firmware to Arduino
1. Open Arduino IDE.
2. Go to **File > Examples > Firmata > StandardFirmata**.
3. Select the correct port and board from **Tools > Port** and **Tools > Board**.
4. Upload the firmware to the Arduino.

---

## Usage

### 1. Launch the Application
Access the application in your browser at `http://localhost:5173/`.

### 2. Design Your Program
- Drag and drop blocks in the Blockly workspace.
- Customize block inputs (e.g., pin numbers, delay durations).

### 3. Generate Python Code
- View the Python code generated from your block arrangement.
- Click **Download Code** to save the script as a `.py` file.

### 4. Run the Python Script
- Ensure the Arduino is connected to your computer.
- Run the downloaded Python script using:
  ```bash
  python arduino_control.py
  ```
---


