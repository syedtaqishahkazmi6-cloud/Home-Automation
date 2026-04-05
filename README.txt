ESP32 8-Channel Smart Relay Controller (Blynk IoT)

This project uses an ESP32 to control an 8-Channel Relay Module via the Blynk IoT Cloud. It allows for remote toggling of appliances through a web dashboard or a mobile app, bypassing the need for local port forwarding or complex network configurations.

Features
Remote Access: Control relays from anywhere in the world via Blynk Cloud.

8-Channel Control: Individual toggles for 8 different electrical loads.

Live Status: Real-time feedback on the connection status and relay states.

Simulation-Ready: Fully compatible with Wokwi for testing without hardware.

Hardware / Simulation Components

MCU: ESP32 (DevKit V1)

Output: 8-Channel Relay Module (Connected to Pins: 4, 5, 6, 7, 15, 16, 17, 18)

Connectivity: WiFi (Wokwi-GUEST for simulation)

Setup Instructions
1. Blynk Cloud Configuration
Create a free account at Blynk.cloud.

Create a New Template named "Smart Relay Controller" for ESP32 using WiFi.

Add 8 Datastreams (V1 through V8) as Integers (Min: 0, Max: 1).

Build a Web Dashboard with 8 Switch widgets assigned to those Virtual Pins.

Go to Search -> New Device -> From Template to generate your unique Auth Token.

2. Wokwi Simulation Setup
Copy the project code into the sketch.ino file.

Library Manager: Add the Blynk library (by Volodymyr Shymanskyy).

Firmware Config: Replace the placeholders at the top of the code with your specific BLYNK_TEMPLATE_ID, BLYNK_TEMPLATE_NAME, and BLYNK_AUTH_TOKEN.

Press Play.

3. Usage
Once the Serial Monitor displays Ready (ping: XXms), your device is online.

Open your Blynk Web Dashboard to toggle the relays.

Observe the relay modules in Wokwi changing state (and LEDs turning on/off) in real-time.

📂 Project Structure
sketch.ino: The C++ source code for the ESP32.

diagram.json: The wiring layout for the Wokwi simulator.

README.md: This documentation file.

⚠️ Important Notes
Active LOW vs HIGH: This code is configured for Active LOW relays (common in most modules). If your relays act backwards, swap the HIGH and LOW logic in the BLYNK_WRITE functions.

Network: No local gateway software (like wokwi-gateway.exe) is required for this Blynk version of the project.

How to use this text:
Create a new file in your project folder (or a new tab in Wokwi if supported) named README.md.

Paste the text above into it.

Save it. Now you have a complete record of your hard work!