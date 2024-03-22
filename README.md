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

## WiFi Manager

The WiFiManager library for Arduino serves as a convenient tool for managing WiFi connections on IoT devices without the need for hardcoding network credentials into the sketch. It simplifies the process of connecting Arduino-based projects to WiFi networks, especially in scenarios where the network environment may change frequently or where manual configuration via code is impractical.

Key features of the WiFiManager library include:

Dynamic Configuration: WiFiManager allows users to configure network settings dynamically at runtime, eliminating the need to modify and re-upload the sketch whenever network credentials change.

Access Point Mode: When the device fails to connect to a known WiFi network, WiFiManager switches to Access Point (AP) mode. In AP mode, the device acts as a temporary WiFi hotspot, enabling users to connect to it via a web browser and input new network credentials.

Web-Based Configuration Portal: WiFiManager hosts a web server on the device in AP mode, presenting users with a user-friendly configuration portal accessible through a standard web browser. This portal provides an intuitive interface for entering WiFi credentials and other configuration parameters.

Integration with Existing Sketches: WiFiManager can be easily integrated into existing Arduino sketches with minimal code modifications. It provides simple API functions for initializing and managing WiFi connections within the sketch.

Overall, WiFiManager simplifies the process of configuring and managing WiFi connections on Arduino-based projects, enhancing their flexibility, usability, and resilience in dynamic network environments. It is particularly valuable for IoT applications where seamless connectivity and remote management are essential requirements.
