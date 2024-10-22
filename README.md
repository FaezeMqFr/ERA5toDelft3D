# ERA5toDelft3D: Wind, Pressure, and Rainfall Data Conversion for Delft3D

Welcome to the **ERA5toDelft3D** repository! This repository contains scripts to convert ERA5 reanalysis data, specifically wind, pressure, and precipitation, into a format compatible with Delft3D hydrodynamic models. The data is extracted from NetCDF files and processed to meet the requirements of the Delft3D-FM suite.

## Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [References](#references)
- [Author](#author)

## Introduction

The **ERA5toDelft3D** repository includes scripts to:
- Convert wind (U10 and V10 components), pressure (mean sea level pressure), and precipitation data from ERA5 reanalysis datasets to NetCDF format required by Delft3D.
- Handle time, longitude, latitude, and variable flipping required for integration into Delft3D models.

These scripts are ideal for researchers and engineers working on coastal or riverine hydrodynamic modeling, integrating ERA5 data into Delft3D-FM simulations.

## Prerequisites

Before running the scripts, ensure you have the following:
- Python 3.9 or later
- Required Python libraries:
  - `netCDF4`
  - `numpy`
  - `datetime`

To install the required libraries, run:
```bash
pip install -r requirements.txt
```

## Project Structure

- `wind_pressure_conversion.py`: Script for converting wind (U10, V10) and pressure (mean sea level) data from ERA5 to Delft3D-compatible NetCDF format.
- `rainfall_conversion.py`: Script for converting total precipitation (rainfall) data from ERA5 to Delft3D-compatible NetCDF format.
- `input/`: Directory for input ERA5 NetCDF files.
- `output/`: Directory for the generated output NetCDF files.

## Usage

### 1. Wind and Pressure Data Conversion
The script `wind_pressure_conversion.py` extracts and processes wind (U10, V10) and pressure (mean sea level) data from an ERA5 NetCDF file, then writes the data into a new NetCDF file compatible with Delft3D.

**Example usage:**
python wind_pressure_conversion.py

### 2. Rainfall Data Conversion
The script `rainfall_conversion.py` extracts total precipitation data (rainfall) from an ERA5 NetCDF file and converts it into a Delft3D-compatible format.

**Example usage:**
python rainfall_conversion.py

## References
- [ERA5 Dataset Documentation](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5)
- [Delft3D Documentation](https://www.deltares.nl/en/software/delft3d-4-suite/)
- [ECMWF Python Tools](https://confluence.ecmwf.int/display/CKB/How+to+download+ERA5)

## Author
This project is implemented by **Faezah Maghsoodifar**. For more information and updates, visit [Curious Seekers Hub](https://faezehmfr.wixsite.com/curiousseekers).
