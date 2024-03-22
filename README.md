# VMS_Merach_PM_chesticki

## Description:

This Arduino code is designed for an air quality monitoring system utilizing the S2 Mini sensor with the PMS5003 sensor module. It also includes functionalities for connecting to the internet via WiFi and uploading data to ThingSpeak for remote monitoring and analysis.

## Libraries Used:

LiquidCrystal_I2C: This library facilitates the interfacing of the liquid crystal display (LCD) via I2C communication. It's likely sourced from johnrickman's repository.
PMS: This library provides support for the PMS series of air quality sensors, specifically for particulate matter (PM) measurements.
WiFiManager: Enables easy setup and management of WiFi connections for IoT devices.
WiFi: Arduino library for connecting to WiFi networks.
ThingSpeak: Facilitates communication with the ThingSpeak IoT platform for data logging and visualization.
Adafruit_NeoPixel: Library for controlling NeoPixels (LEDs) for visual feedback.
Adafruit_NeoMatrix: Extends NeoPixel functionality to matrices for displaying text or patterns.
Pin Configuration:

The NeoMatrix is configured with PIN 5 for communication with the NeoPixel LED matrix.

## Variables:

x1: Stores the current position for text scrolling on the NeoMatrix.
pass: Used for cycling through colors on the NeoMatrix.
myChannelNumber and myWriteAPIKey: Credentials for ThingSpeak channel access.
Setup Function:

Initializes the NeoMatrix display, sets up WiFi connection using WiFiManager, initializes the ThingSpeak client, and initializes the PMS5003 sensor.
Loop Function:

Reads data from the PMS5003 sensor.
If sensor data is available, it prints air quality metrics and optionally temperature, humidity, and formaldehyde concentration to the serial monitor.
Updates ThingSpeak fields with sensor data.
Scrolls and displays air quality metrics on the NeoMatrix.
Uploads data to the ThingSpeak channel and prints success or failure messages to the serial monitor.
This code provides a comprehensive solution for real-time air quality monitoring and remote data logging, suitable for IoT projects and environmental monitoring applications.
