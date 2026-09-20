> 🚧 **Project Status: In Active Development** 
> The hardware prototype and Python dashboard are currently being finalized. 

# SENTINEL: Multi-Sensor Spatial Sensing & Navigation System

**Team Members:** Tannishtha Gupta & Dhvan Shah

## Overview
This project is a low-cost, modular multi-sensor spatial sensing and navigation prototype[cite: 9]. It serves as a passive, standalone RF and thermal anomaly-bearing demonstrator[cite: 10]. The system applies a weighted sensor-fusion algorithm to hardware measurements to output a fused compass bearing, estimated angular uncertainty, and data-quality indicators without relying on active ranging[cite: 9, 10]. 

## Hardware Architecture
* **Microcontroller:** ESP32-S3[cite: 10]
* **Orientation & Positioning:** GNSS module and 9-axis IMU (calibrated, tilt-compensated AHRS)[cite: 10]
* **Sensors:** Passive directional 433/915 MHz RF front end and MLX90640 thermal camera (55°x35° FOV)[cite: 10]
* **Mechanical:** Pan/tilt mechanism for angular sweep[cite: 10]

## Software Interface
The dashboard is built with Python, Dash, and Plotly, running locally to ingest JSON telemetry via Serial, HTTP, or WebSocket[cite: 10]. 

**To run the dashboard locally:**
1. Navigate to the dashboard directory: `cd dashboard`
2. Install dependencies: `pip install -r requirements.txt`
3. Execute the interface: `python dashboard.py`

## Applications
The system supports applications in autonomous robotics, search-and-rescue, disaster response, environmental monitoring, industrial inspection, infrastructure monitoring, and remote-area sensing[cite: 9]. 

> **System Boundary Note:** This system is for telemetry-visualization and sensor-fusion research[cite: 10]. It contains no targeting, guidance, jamming, or firing control logic[cite: 10].
