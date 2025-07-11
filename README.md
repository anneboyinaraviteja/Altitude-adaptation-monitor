# Altitude-adaptation-monitor

## Introduction
"High-Altitude Health Monitoring – Continuous real-time monitoring of vital signs (pulse, body temperature) and environmental parameters (altitude, atmospheric pressure, humidity, and ambient temperature) to identify early signs of altitude sickness, hypoxia, and fatigue during ascent."

 ## List of Sensors used
- **ESP32**              : Main controller with Bluetooth + Wi-Fi
- **MAX30102**            : Measures blood oxygen saturation and pulse rate
- **MLX90614(IR)**        : Non-contact body temperature measurement
- **BME280**              : Measures altitude and atmospheric pressure
- **0.96" OLED Display**  : Shows real-time vitals on-device
- **5V Piezo Buzzer**     : Audio alert for critical conditions
- **3.7V Li-Po + TP4056** :  Power supply with rechargeable module

## TRL-8 goals
1. To validate the accuracy and stability of HR and IR values from the MAX30102 and temperature readings from the MLX90614, by comparing them with clinical-grade devices under both resting and active human physiological conditions.

2. Drift Assessment: Monitor each sensor’s output for 24 hours to assess long-term stability and thermal drift, especially during ambient temperature changes but due to lack of stable environment we have taken the log report in unstable conditions only.

3. Altitude Simulation Tests: Use controlled elevation environments (staircases and stable altitude place) to simulate altitude changes and observe variations vitals.

4. Threshold Alert Testing: Simulated abnormal vitals (finger off sensor) to verify alert triggering for high and low HR, or abnormal temperature.

5.WiFi & App Reliability: Test wireless transmission latency, data loss, and real-time display across varying distances and interference conditions using the web server.

## Setup Steps
**1. Assemble Hardware:** Connect all sensors (SpO₂, temperature, pressure) and modules (OLED, buzzer, GSM/Bluetooth) to the microcontroller as per the schematic.

**2. Flash Firmware:** Upload the modular ESP32 code using the Arduino IDE.

**3. Start Web Dashboard**: Connect the device to Wi-Fi and access a built-in web server via browser to monitor live vitals and download data logs.

**4. Calibrate Sensors:** Use known reference values to fine-tune sensor readings for accuracy.

**5. Power the System:** Use a Li-ion battery with TP4056 charging module or USB power.

**6. Test Outputs:** Verify vitals on the OLED and app, and test alert triggers for abnormal conditions.
