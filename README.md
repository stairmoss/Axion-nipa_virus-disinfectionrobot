Autonomous Air Sanitization Machine – Project Abstract

Location: Kerala
Alias: Nipa Virus

The Autonomous Air Sanitization Machine is an AI-driven, autonomous system designed to filter and disinfect air, targeting germs, viruses, and COVID-19 particles. It is primarily intended for hospital environments where air contamination poses serious health risks. The machine maps the area, navigates autonomously, detects obstacles using ultrasonic sensors, and alerts humans with a buzzer if they are in the path.

Key Features:

Eliminates 90% of dust, smoke, viruses, germs, and COVID particles as small as 0.1 microns.

Disinfects a 600 sq. ft. area in ~8.5 minutes.

Autonomous navigation with stored area maps for repeated operation.

Filtration & UV disinfection for safe and effective air cleaning.

Lightweight (~9 kg), compact dimensions, smooth rubber wheels, low noise, and cost-effective.

Technologies Used:

Python & Arduino for control and automation

Sensors: Ultrasonic for obstacle detection

Embedded systems for motor and UV control

Impact:
Provides a safer environment in hospitals and indoor spaces, reduces the spread of COVID-19 and other airborne diseases, and improves overall air quality.



Things used in this project:  How to Build the Autonomous Air Sanitization Machine

The Autonomous Air Sanitization Machine is a robotics project designed to filter, disinfect, and monitor indoor air, primarily targeting viruses, germs, and COVID-19 particles. This guide details the hardware, sensors, electronics, and software setup, and explains how all components work together to create a fully autonomous system.  
   | Component                                                      | Quantity | Purpose                                                                                         |
| -------------------------------------------------------------- | -------- | ----------------------------------------------------------------------------------------------- |
| **ULPA Filter**                                                | 1        | High-efficiency filter to capture particles as small as 0.1 microns including viruses and dust. |
| **UV Light 254nm**                                             | 1        | Disinfects trapped germs in the filter without exposing humans to harmful rays.                 |
| **Alphanumeric LED Display (Red)**                             | 1        | Displays air quality, battery status, and distance covered.                                     |
| **Arduino Mega 2560**                                          | 1        | Main microcontroller to control motors, sensors, and UV system.                                 |
| **Ultrasonic Sensor HC-SR04**                                  | 3        | Detect obstacles on the left, right, and front sides of the machine for autonomous navigation.  |
| **Grove Air Quality Sensor v1.3**                              | 1        | Detects air pollution levels (smoke, dust, VOCs) in real-time.                                  |
| **Air Quality Monitor (PM2.5, Formaldehyde, Temp & Humidity)** | 1        | Provides precise environmental readings for monitoring indoor air quality.                      |
| **Fermion SGP40 Air Quality Sensor (Breakout)**                | 1        | Detects volatile organic compounds (VOCs) for improved accuracy.                                |
| **Rechargeable Battery 12V**                                   | 1        | Powers the entire system including motors, sensors, and UV light.                               |
| **Geared DC Motors 12V**                                       | 4        | Drives wheels for smooth autonomous movement.                                                   |
| **Wheels**                                                     | 4        | Ensures stable movement on indoor surfaces.                                                     |
| **Dual H-Bridge Motor Driver L298**                            | 1        | Controls motor speed and direction using Arduino commands.                                      |
| **Big Red Dome Button**                                        | 1        | Emergency stop button for safety.                                                               |
| **General Purpose NPN Transistor**                             | 1        | Switches high-current loads like UV light or motors safely.                                     |
| **Charging Circuit**                                           | 1        | Allows battery recharging and prevents overcharging.                                            |






  2️⃣ Software & Development Tools  
| Tool                             | Purpose                                                                                  |
| -------------------------------- | ---------------------------------------------------------------------------------------- |
| **Arduino IDE**                  | Write and upload firmware to the Arduino Mega controlling motors, sensors, and UV light. |
| **Microsoft Visual Studio 2015** | Optional for advanced simulations, integrating display visuals, and monitoring logs.     |




3️⃣ Assembly & Integration 

Step 1: Base Structure & Mobility

Attach 4 wheels to the geared DC motors.

Mount the motors on the chassis with proper alignment to ensure stability.

Connect the motors to the L298 dual H-bridge motor driver.

Wire the motor driver to Arduino Mega 2560 using PWM pins for speed and direction control.

Step 2: Filtration & Disinfection

Mount the ULPA filter securely on top of the chassis.

Position the UV light (254nm) inside the filter enclosure to disinfect trapped particles.

Use the NPN transistor to safely switch the UV light on/off via Arduino.

Step 3: Sensor Installation

Place HC-SR04 ultrasonic sensors at the front, left, and right for obstacle detection.

Install air quality sensors (Grove v1.3, PM2.5 monitor, Fermion SGP40) in the airflow path after the filter to monitor air quality post-filtration.

Connect sensors to Arduino analog/digital pins as per datasheets.

Step 4: Display & Controls

Mount the alphanumeric LED display on the front of the machine.

Connect the Big Red Dome Button to Arduino’s digital input for emergency stop.

Program the display to show real-time air quality, battery percentage, and distance traveled.

Step 5: Power & Battery

Connect the 12V rechargeable battery to power motors and sensors.

Ensure the charging circuit is properly integrated to allow safe battery recharging.

Use voltage regulators if necessary for stable power supply to Arduino and sensors.

4️⃣ Software Programming
Arduino Firmware

Initialize all sensors, motors, UV light, and display in the setup() function.

Write functions for:

Obstacle detection → stop or turn if ultrasonic sensor detects an object.

Autonomous navigation → follow a pre-mapped route using stored coordinates.

Air monitoring → read data from air quality sensors continuously.

UV control → activate UV light only when machine is running.

Program LCD updates for air quality, distance traveled, and battery.

Implement emergency stop logic linked to the red dome button.

Optional Visual Monitoring (Visual Studio)

Visualize real-time sensor readings and machine position.

Log air quality and coverage data for analysis.

5️⃣ Operation Instructions

Place the machine at the starting point (preferably near charging station).

Press the REPEAT button to start autonomous navigation.

Machine moves along pre-stored map, avoiding obstacles using ultrasonic sensors.

UV light disinfects air in the filter continuously.

Upon completing a round, machine returns to the charging point if battery is low.

6️⃣ Safety Considerations

Ensure UV light exposure is confined to the filter to prevent harm.

Do not operate the machine near flammable gases.

Regularly check and replace the ULPA filter every 5–7 months.

Keep emergency stop button accessible at all times.

7️⃣ Expected Performance

Disinfects 600 sq. ft. area in ~8–9 minutes.

Eliminates 90% of dust, smoke, germs, and viruses.

Lightweight and low-noise operation for indoor use.
  

Conclusion:
The system demonstrates an innovative, autonomous approach to air sanitization. With proper implementation, it can significantly reduce infection risks and serve as a reliable daily air-cleaning solution for healthcare facilities and large buildings.
