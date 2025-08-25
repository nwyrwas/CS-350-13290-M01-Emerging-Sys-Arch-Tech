# CS-350-13290-M01-Emerging-Sys-Arch-Tech

# 🌡️ Thermostat Control System  

## 📌 Project Overview  
This project demonstrates a thermostat prototype designed for the **Raspberry Pi** platform. It integrates **LEDs**, **buttons**, and state management to simulate the behavior of a real-world heating and cooling system. The thermostat cycles through three distinct states:  

- **Off** – all LEDs remain off  
- **Heat** – represented by a red LED (solid when temperature is at or above setpoint, fading when below setpoint)  
- **Cool** – represented by a blue LED (solid when temperature is at or below setpoint, fading when above setpoint)  

Buttons allow the user to:  
- Cycle between states (Off → Heat → Cool)  
- Increase the target setpoint temperature  
- Decrease the target setpoint temperature  

This project was designed to explore how embedded systems integrate hardware and software while solving the problem of **state management and user interaction**. It provides a simplified but effective model of how thermostats regulate environments, offering practical insight into how **hardware-software integration** and **state machines** can be applied to real-world systems.  

---

## 🎥 Demo Video  

[![Watch the Thermostat Demo](https://img.youtube.com/vi/nlIeEz6BLFo/0.jpg)](https://www.youtube.com/watch?v=nlIeEz6BLFo)  


---

## 📝 Reflection  

### Summarize the project and what problem it was solving  
The thermostat project aimed to simulate the functionality of a household thermostat using simple electronic components on a Raspberry Pi. By designing a system that could switch between heating, cooling, and off states while adjusting the setpoint temperature, I solved the problem of **how to model and manage system states effectively in embedded systems**. The project demonstrated how a physical device can reflect changes in system logic through LEDs and user input, addressing the challenge of connecting **low-level hardware control with high-level logic design**.  

---

### What did you do particularly well?  
I did particularly well in implementing the **state machine design pattern** to govern the thermostat’s behavior. This ensured that the system was modular, organized, and easy to understand. Instead of relying on complex conditional statements, the state machine allowed me to clearly define transitions and behaviors for each state, which made debugging and testing much more efficient.  

Another area I excelled in was **creating a user-friendly interaction model**. By mapping the thermostat controls to simple buttons, I was able to simulate real-world usability, giving the project a practical feel. Additionally, I added **fading LED effects**, which provided more realistic visual feedback for heating and cooling states. This not only made the project functional but also enhanced its presentation value.  

---

### Where could you improve?  
One area for improvement is integrating a **real temperature sensor** (such as the AHTx0) to replace simulated temperature values. While the current project successfully demonstrates logic and interaction, adding live environmental data would make it far more realistic and useful.  

I could also improve error handling by adding safeguards against unexpected hardware behavior, such as button bounce or disconnections. Another improvement would be expanding the system with an **LCD display** to show the current temperature, setpoint, and system state. Finally, I could enhance scalability by designing the system to support more advanced communication, such as a mobile app or web interface to remotely control and monitor the thermostat.  

---

### What tools and/or resources are you adding to your support network?  
To complete this project, I expanded my support network of tools and resources significantly:  
- **Python 3**: Chosen for its readability and extensive support for Raspberry Pi.  
- **gpiozero library**: Simplified GPIO pin interactions, making hardware integration straightforward.  
- **statemachine library**: Provided a clean framework for managing states and transitions.  
- **Raspberry Pi 4 hardware**: The primary platform for running and testing the system.  
- **Online documentation and forums**: Raspberry Pi and Python communities were invaluable for troubleshooting hardware/software issues.  
- **YouTube tutorials and technical blogs**: Helped me visualize wiring setups and refine LED/button interactions.  

These tools and resources have become part of my permanent development toolkit for future embedded systems and IoT projects.  

---

### What skills from this project will be particularly transferable to other projects and/or course work?  
Several skills from this project are highly transferable:  

- **State Machine Design**: The ability to model systems with clearly defined states and transitions is useful not only for embedded systems but also for robotics, automation, and game development.  
- **Hardware-Software Integration**: Understanding how code interacts with physical components is a critical skill for IoT, sensor networks, and real-time systems.  
- **Modular Programming Practices**: By structuring my code into functions and modules, I strengthened my ability to write maintainable software that can be scaled to larger projects.  
- **Debugging in Real-Time Environments**: Learning to debug both hardware wiring and software logic simultaneously will benefit future coursework and professional projects.  
- **Documentation and Reflection**: Writing detailed reflections like this README reinforces the importance of communication, which is an essential professional skill.  

---

### How did you make this project maintainable, readable, and adaptable?  
To make the project **maintainable**, I followed consistent coding standards, breaking down logic into smaller, reusable functions rather than embedding everything into a single loop. This makes the code easier to extend or update in the future.  

For **readability**, I used descriptive variable names, inline comments, and section headers throughout the code. This ensures that other developers (or even myself in the future) can quickly understand the logic without needing to re-learn the project from scratch.  

The project was designed to be **adaptable** by using modular design principles. For example, the thermostat logic can easily be extended to work with additional hardware like temperature sensors, LCD displays, or WiFi modules. The state machine pattern also makes it simple to add new states or behaviors without rewriting the entire program. Together, these practices ensure the system is flexible and ready for future improvements.  

---

## 📂 Milestone Work  

### 🔸 Milestone One: Pulse Width Modulation (PWM) Lab  
- Implemented **PWM control** to fade an LED in and out:contentReference[oaicite:6]{index=6}:contentReference[oaicite:7]{index=7}  
- Observed LED brightness changes based on duty cycle (10–20 Hz visible blinking, >60 Hz appears solid).  
- Demonstrated **how PWM can control brightness without voltage changes**.  
- **Skills gained:** PWM design, LED fading control, GPIO programming.  

---

### 🔸 Milestone Two: GPIO UART Lab  
- Expanded functionality to include **serial communication**:contentReference[oaicite:8]{index=8}:contentReference[oaicite:9]{index=9}:contentReference[oaicite:10]{index=10}.  
- Created `SerialTest-Write.py` and `SerialTest-Read.py` for UART testing:contentReference[oaicite:11]{index=11}:contentReference[oaicite:12]{index=12}.  
- Built a **client-server system** (`SerialLightControl-Client.py` / `SerialLightControl-Server.py`) for remote LED control.  
- Implemented **encode/decode conversions** for serial byte streams.  
- Added **exception handling and cleanup** to ensure system stability.  
- **Skills gained:** UART comms, serial debugging, client-server logic, safe GPIO handling.  

---

## 📂 Repository Contents  

### Core Project Files  
- `Thermostat.py` → Final thermostat implementation:contentReference[oaicite:13]{index=13}  
- `MultiButtonTest.py` → Demonstrates multiple button input with PWM LEDs:contentReference[oaicite:14]{index=14}  
- `ThermostatServer-Simulator.py` → Simulates receiving thermostat data via UART:contentReference[oaicite:15]{index=15}  

### Milestone One (PWM)  
- `Milestone1.py` → PWM LED fading demo:contentReference[oaicite:16]{index=16}  
- `2-4 Milestone One.docx` → Written milestone reflection:contentReference[oaicite:17]{index=17}  

### Milestone Two (UART)  
- `SerialTest-Read.py` → UART serial input demo:contentReference[oaicite:18]{index=18}  
- `SerialTest-Write.py` → UART serial output demo:contentReference[oaicite:19]{index=19}  
- `SerialLightControl-Client.py` → Client to send LED control commands:contentReference[oaicite:20]{index=20}  
- `SerialLightControl-Server.py` → Server to interpret commands and control LED:contentReference[oaicite:21]{index=21}  
- `3-3 Milestone Two.docx` → Written milestone reflection:contentReference[oaicite:22]{index=22}  

### Final Project Documentation  
- `7-1 Final Project Report.docx` → Full project report:contentReference[oaicite:23]{index=23}  
- `README.md` → Project overview and reflection  

---

## ▶️ How to Run  
1. Clone this repository to your Raspberry Pi.  
2. Install dependencies:  
   ```bash
   pip3 install gpiozero statemachine pyserial adafruit-circuitpython-ahtx0 adafruit-circuitpython-charlcd

---

## ▶️ How to Run  

- **Milestone One**: Wire an LED to GPIO 18 and run `Milestone1.py`.  
- **Milestone Two**: Connect a USB → TTL cable. Run `SerialLightControl-Server.py` on the Pi and `SerialLightControl-Client.py` for input.  
- **Thermostat Project**: Wire LEDs, buttons, LCD, and temperature sensor as described in code comments. Run `Thermostat.py`.  
- **Server Simulation**: Run `ThermostatServer-Simulator.py` to receive UART messages from the thermostat.  

---

## 🌟 Portfolio Reflection  

This project highlights my ability to:  
- Build **embedded system applications** with Raspberry Pi  
- Use **state machines** for clean, organized control logic  
- Apply **hardware/software integration** principles  
- Write **adaptable, maintainable, and readable code**  

It demonstrates not only technical skills but also:  
- Critical thinking  
- Problem-solving  
- Professional documentation  

For these reasons, it serves as a strong portfolio artifact and a meaningful reflection of my learning in **emerging systems architecture and technologies**.  


For these reasons, it serves as a strong portfolio artifact and a meaningful reflection of my learning in **emerging systems architecture and technologies**.  
