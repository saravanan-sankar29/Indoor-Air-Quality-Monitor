# IoT Indoor Air Quality Monitor for Hospital Environments

A reliable, real-time indoor air quality (IAQ) monitoring system designed specifically for hospital wards and healthcare facilities to ensure patient safety, maintain sterile environmental baselines, and track atmospheric vitals.

##  Project Overview
Maintaining optimal air quality, temperature, and humidity is critical in healthcare settings to prevent the airborne transmission of pathogens and ensure patient comfort. This project introduces an ESP32-based embedded monitor that continuously samples environmental data, detects harmful gas thresholds, and provides immediate visual telemetry.

---

##  Key Features & Modules
* **Automated Gas & Pollutant Detection (MQ135):** Monitors ambient air quality by detecting harmful gases, smoke, ammonia, and alcohol ppm levels common in clinical environments.
* **Climate Telemetry (DHT11):** Continuously tracks temperature and relative humidity percentages to ensure sensitive medical zones stay within regulatory safety thresholds.
* **Real-Time Visual Interface (16x2 LCD Display):** Provides on-site healthcare staff with an instantaneous, easy-to-read dashboard showing gas concentrations, temperature, and humidity.
* **Central Processing & Edge Logic (ESP32):** Serves as the high-speed processing core, managing sensor calibration, data parsing, and threshold logic.

---

## Hardware Architecture & Specifications

### Component Technical Breakdown
| Component | Function / Role | Interface Used | Operating Voltage |
| :--- | :--- | :--- | :--- |
| **ESP32** | Central microcontroller & processing unit | GPIO, I²C / Parallel | 3.3V |
| **MQ135 Sensor** | Hazardous gas and air pollution monitoring | Analog Input | 5V |
| **DHT11 Sensor** | Ambient temperature & humidity tracking | Digital (Single-Wire) | 3.3V–5V |
| **16x2 LCD Display** | Real-time local data visualization | I²C (via backpack) or Parallel | 5V |

---

## Firmware & Standards Compliance
* **Language & Environment:** C / C++ utilizing the Arduino IDE framework.
* **Libraries Used:** `DHT.h` for climate data parsing, and `LiquidCrystal_I2C.h` (or standard `LiquidCrystal.h`) for display drivers.
* **Data Processing:** Features baseline sensor calibration algorithms to filter noise and map raw analog sensor voltage directly to air pollution indexing profiles.

---

##  Healthcare Application
* **Patient Wards:** Safeguards respiratory patients by tracking sudden humidity drops or pollutant spikes.
* **Intensive Care Units (ICUs):** Ensures a highly controlled ambient climate to assist recovery and mitigate bacterial survival rates.
* **Sterile Storage:** Monitors storage environments for temperature-sensitive medical supplies and surgical equipment.

---

## Future Enhancements
* **IoT Cloud Telemetry:** Integrating AWS IoT Core or Blynk to log historical data and send instant push notifications to hospital administration dashboards.
* **Intelligent HVAC Integration:** Modulating ventilation fans or air purifiers automatically when gas thresholds are breached.
* **Aerosol Particle Counting:** Upgrading the hardware stack to include particulate matter sensors (PM2.5 / PM10) for comprehensive sterile room certification.

---

##  Author
* **Saravanan S** ([Email](mailto:saravanansankar2917@gmail.com)) — B.Tech Electrical and Electronics Engineering
