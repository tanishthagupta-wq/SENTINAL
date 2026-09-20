> 🚧 **Project Status: In Active Development**
> The hardware prototype and Python dashboard are currently being finalized.

# SENTINEL: Microcontroller-Based Multi-Sensor Spatial Sensing and Intelligent Navigation System

**Team Members:** Tannishtha Gupta & Dhvan Shah

## Overview

This project explores precision-guidance concepts through a low-cost, modular multi-sensor spatial sensing and navigation prototype. The system automatically determines its geographical position via GPS, while allowing manual reference waypoint entry through a computer-based dashboard. Within a configurable search radius, RF and infrared/thermal sensors perform angular and spatial scanning to collect signal-strength and thermal-intensity measurements. An ESP32 microcontroller filters this data, identifies strong response regions, and applies a weighted sensor-fusion algorithm to compute a resultant vector and navigation heading. A fallback mode utilizes local sensor information and the last known position if GPS becomes unavailable.

## Repository Structure

```text
SENTINEL/
├── dashboard/
│   ├── dashboard.py          # Python-based dashboard interface
│   └── requirements.txt      # Dashboard dependencies
├── docs/
│   └── abstract.pdf         # Project documentation, schematics, and reports
├── firmware/
│   └── .keep                 # Placeholder for embedded C/C++ firmware
├── .gitignore                # Ignored system and cache files
├── LICENSE                   # Open-source license
└── README.md                 # Project front page
```

## Hardware Components

* **ESP32 Microcontroller:** Handles data filtering, vector conversion, and sensor-fusion algorithms.
* **GPS Module:** Automatically determines the current geographical position.
* **RF Sensing Module:** Performs angular and spatial scanning to collect signal-strength measurements.
* **Infrared/Thermal Sensor:** Collects thermal-intensity measurements within the configured search radius.

## Software & Expected Outputs

The software stack utilizes embedded C/C++ firmware alongside a Python-based dashboard, built to be adaptable for future hardware upgrades.

**Expected System Outputs:**

* Live GPS coordinates and waypoint information
* Sensor intensities and spatial heat maps
* Individual and fused vectors
* Estimated source location, confidence level, and navigation heading

## Applications

The system is designed to support applications in autonomous robotics, search-and-rescue, disaster response, environmental monitoring, industrial inspection, infrastructure monitoring, and remote-area sensing.
