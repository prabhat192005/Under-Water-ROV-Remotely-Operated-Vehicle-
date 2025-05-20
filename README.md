## Underwater ROV Project ( Under Development Stage of Autonomous Underwater Vehicle (AUV) )

### Project Overview

The Underwater ROV (Remotely Operated Vehicle) is a low-cost, DIY underwater exploration robot designed for real-time remote operation. The system uses Arduino Nano as the transmitter (surface controller) and Arduino Uno as the receiver (onboard controller) to send and receive commands through a wired tether.

This ROV is capable of navigating underwater environments using multiple thrusters and can stream live video using a camera module mounted on the vehicle. It also supports integration with various sensors to monitor underwater conditions like depth, temperature, and pressure.

Communication between the surface station and the ROV is achieved via serial communication over the tether cable, ensuring reliable control and feedback. The vehicle is powered by a rechargeable battery and can be controlled via a joystick or a PC interface.

This project is aimed at students, hobbyists, and researchers who are exploring underwater robotics and want a modular, affordable platform for learning and experimentation.

### Circuit Components:

* **Arduino Uno (Receiver):** Receives control signals from the transmitter and controls the motors and ESCs accordingly.
* **Arduino Nano (Transmitter):** Sends control commands through serial communication to the receiver.
* **L298N Motor Driver Module:** Controls the three DC motors for propulsion and direction control.
* **ESC (Electronic Speed Controller) x 2:** Controls the two brushless motors for vertical and horizontal thrust.
* **AA Battery Pack:** Power source for the joystick module.
* **Joystick Module x 2:** Used to control motor speed and direction (one for propulsion, one for thrust).

### Features:

* Movement Control – Multi-directional movement using thrusters (forward, backward, ascend, descend, rotate).

* Live Video Streaming – Real-time underwater video using a USB or Raspberry Pi camera module.

* Tethered Communication – Stable and responsive command/data communication between the ROV and surface controller.

* Sensor Integration – Optional modules for depth, temperature, and pressure sensing.

* Modular Design – Easily upgradeable frame and electronics.

* ESP32/Raspberry Pi Integration – Control logic and video streaming using ESP32 (for controls) and Raspberry Pi (for camera + network).


### Circuit Connections:


![Circuit Diagram](https://github.com/user-attachments/assets/a8e7d133-3548-4d9e-86ee-911e87a30e27)



* **Motor Connections:**

  * The L298N motor driver is connected to three DC motors responsible for propulsion and maneuvering.
  * The power connections from the battery pack are routed through the L298N motor driver to provide power to the motors.

* **ESC Connections:**

  * Two ESCs are connected to the brushless motors. Each ESC receives PWM signals from the Arduino Uno to control motor speed and direction.

* **Transmitter (Arduino Nano) Connections:**

  * The joystick modules are connected to the analog pins of the Nano to read control inputs.
  * The Nano sends serial data to the Uno through a wired connection.

* **Receiver (Arduino Uno) Connections:**

  * The Arduino Uno receives serial data from the Nano and processes it to control the L298N motor driver and ESCs.

### Serial Communication:

* The Arduino Nano acts as the transmitter, reading joystick inputs and sending control commands as serial data to the Arduino Uno.
* The Arduino Uno interprets the commands and adjusts motor speed and direction accordingly.

### Results: 

![IMG-20241217-WA0022](https://github.com/user-attachments/assets/872e9704-af12-4676-b457-cbd0bd58283e)

![IMG-20241217-WA0019](https://github.com/user-attachments/assets/b807adbd-f0a9-46aa-9fe6-577281245039)

![IMG-20241217-WA0023](https://github.com/user-attachments/assets/43039118-1e6b-4d16-95b7-95cb025611f5)

![Remote](https://github.com/user-attachments/assets/d9ac87d5-aa34-462a-82e2-f8d6d9bc1cc0)

### Applications

* Underwater Inspection

* Marine Research and Exploration

* Search & Rescue Missions

* Educational and Academic Projects



### Development Stage and Future Plans:

* The current ROV setup serves as a foundational stage in developing a fully autonomous underwater vehicle (AUV).
* Further development will include implementing autonomous navigation, sensor integration, and control algorithms to transition from remote control to autonomous operation.
