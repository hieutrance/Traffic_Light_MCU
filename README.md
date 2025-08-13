# 🚦 Traffic Light System for 4-Way Intersection using STM32F103RB

## 📌 Overview
This project implements a **traffic light control system** for a **4-way intersection** using the STM32F103RB microcontroller.  
The system uses:
- **Finite State Machine (FSM)** for mode control (automatic & manual modes)
- **Timer interrupts** for precise timing
- **7-segment display** for countdown timers
- **Button inputs** for mode switching and configuration

The project is developed using **STM32CubeIDE** and simulated in **Proteus**.

---

## 🎯 Features
- **Automatic Mode**:
  - Controls Red, Yellow, and Green lights for 4 directions.
  - Countdown display for each light.
- **Manual Mode**:
  - Allows manual control of traffic lights using push buttons.
- **Configurable Timers**:
  - Adjust Red, Yellow, Green durations.
- **Debounced Button Input** using software.
- **7-Segment LED Display** for real-time countdown.
- **Timer Interrupts** to handle periodic events without blocking code.

---

## 🛠 Hardware & Tools
### Hardware
- STM32F103RB (ARM Cortex-M3)
- LEDs (Red, Yellow, Green for each lane)
- 4 x 7-Segment Displays
- Push Buttons
- Resistors
- Breadboard / PCB

### Software & Tools
- STM32CubeIDE
- STM32CubeMX
- Proteus 8 Professional (for simulation)
- Git (for version control)

---

## 📂 Project Structure
Src/
│ LAB3_Proteus_Simulation.pdsprj # Proteus simulation file
│ button.c # Button handling & debounce
│ display7SegLed.c # 7-segment display control
│ fsm_automatic.c # Automatic mode FSM logic
│ fsm_manual.c # Manual mode FSM logic
│ global.c # Global variables & constants
│ main.c # Main program entry
│ software_timer.c # Software timer management
│ stm32f1xx_hal_msp.c # HAL MSP initialization
│ stm32f1xx_it.c # Interrupt handlers
│ syscalls.c # System call stubs
│ sysmem.c # Memory management stubs
│ system_stm32f1xx.c # System clock configuration
Inc/
(Header files for above modules)
Startup/
startup_stm32f103xb.s # Startup assembly code
Debug/
(Build output)

---

## ⚙️ How It Works
1. **Initialization**:
   - Configure GPIO for LEDs, buttons, and 7-segment display.
   - Set up hardware timers and interrupts.
2. **FSM Control**:
   - Automatic mode cycles through traffic light phases with predefined durations.
   - Manual mode allows user intervention via buttons.
3. **Timer Interrupts**:
   - Timer triggers every 10ms for precise countdown updates.
4. **7-Segment Display**:
   - Multiplexing used to display countdown values for each lane.

---

## 🚀 Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/hieutrance/Traffic_Light_MCU.git
