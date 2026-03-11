# AQI Model-Based Reflex Agent 🍃

This repository contains a simple, dependency-free **Model-Based Reflex Agent** written in Python. It is designed to "perceive" raw PM2.5 particulate matter data from a CSV file and "act" by calculating and outputting the standardized Air Quality Index (AQI) based on official concentration breakpoints.

## Features
* **Zero External Dependencies:** Built entirely with standard Python libraries (`csv`).
* **AI Architecture:** Implements a classic Model-Based Reflex Agent paradigm (Perceive $\rightarrow$ Act).
* **Accurate Calculations:** Uses standard piecewise linear interpolation and official breakpoints (30, 60, 90, 120, 250) to accurately map raw PM2.5 concentrations to the AQI scale.
* **Error Handling:** Gracefully handles missing sensor data files.

## How it Works
1. **Perceive:** The agent reads `sensor_data.csv`, extracting raw PM2.5 readings.
2. **Act:** It runs each reading through a rule set of `if-elif` breakpoints, calculating the final AQI score.

## Quick Start

1. Create a `sensor_data.csv` file in the root directory with a `pm25` column:
   ```csv
   pm25
   45.2
   15.0
   85.5
