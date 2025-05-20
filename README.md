# Lab 4 - Gesture Recognition using MPU6050 and Edge Impulse

## Overview
This project is an implementation of gesture recognition using the MPU6050 accelerometer and Edge Impulse. The system captures accelerometer data when a button is pressed, performs inference using a pre-trained Edge Impulse model, and lights up an LED to indicate the recognized gesture. The recognized gesture is also printed to the serial monitor.

## Features
- **Gesture Recognition**: Recognizes predefined gestures (e.g., "O", "V", "Z") based on accelerometer data.
- **LED Feedback**: Visual feedback with RGB LEDs corresponding to each gesture.
- **Button Trigger**: Start capturing data by pressing a button.
- **Edge Impulse Integration**: Uses Edge Impulse for gesture recognition based on accelerometer data.

## Hardware Required
- **ESP32/Arduino Board**: Microcontroller to run the code.
- **MPU6050 Accelerometer**: Sensor for capturing motion data.
- **RGB LED**: Red, Green, and Blue LEDs for visual feedback.
- **Push Button**: Button to trigger the data collection process.
- **Battery**: Battery to power the system.
- **Enclosure**: An enclosure to hold the components safely (optional, based on the requirement).

## Circuit Diagram
- **Button Pin**: D3 (Input)
- **LED Pins**: D8 (Blue), D9 (Green), D10 (Red)
- **MPU6050 Pins**: I2C (SDA: GPIO21, SCL: GPIO22)

## Setup Instructions
1. **Hardware Setup**:
    - Connect the **MPU6050** to your ESP32/Arduino board using I2C (SDA to GPIO21, SCL to GPIO22).
    - Connect an **RGB LED** to pins D10, D9, and D8.
    - Connect a **button** to pin D3, with a pull-up resistor.

2. **Software Setup**:
    - Install the required libraries:
        - `Adafruit_MPU6050` for accelerometer functionality.
        - `Adafruit_Sensor` for sensor data.
        - `Edge Impulse` model header file (`VictoriaYang-LAB4_inferencing.h`).
    - Upload the provided code to the ESP32/Arduino.

3. **Edge Impulse Model**:
    - This code assumes you have trained a gesture recognition model on Edge Impulse and have downloaded the corresponding model files.
    - Ensure the model's inference header file (`VictoriaYang-LAB4_inferencing.h`) is included in the project.

## Running the Code
1. Press the button to start capturing data from the MPU6050.
2. The system will collect accelerometer data and send it to Edge Impulse for inference.
3. Based on the inference result, the corresponding LED color will light up and the gesture label will be displayed in the Serial Monitor.

## Deliverables
- **GitHub Repository** with all the code files.
- **Demo Video** showcasing the functionality of the system.
- **Report** detailing the process, challenges faced, and results.

## License
This project is licensed under the MIT License.
