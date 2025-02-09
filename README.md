# Autonomous Agricultural Navigation System

## Project Overview
The **Autonomous Agricultural Navigation System** is designed to optimize precision farming by enabling self-driving agricultural vehicles. The system integrates advanced navigation, sensor fusion, and real-time data processing to enhance operational efficiency, reduce labor costs, and improve crop management.<br><br>

## How?
### MPU6050 IMU
Measures acceleration and rotation to determine movement changes. It is crucial for tracking motion dynamics in real-time.<br><br>

### Accelerometer & Gyroscope Measurement
The IMU captures acceleration values via the accelerometer and rotational speed via the gyroscope. These values help understand the vehicle’s movement.<br><br>

### I2C Communication
The MPU6050 transmits collected data to the STM32 via I2C protocol. This ensures efficient data transfer between components.<br><br>

### STM32 Processing
The microcontroller receives sensor data and processes it for navigation. It plays a key role in fusing multiple sensor inputs.<br><br>

### Receiving Sensor Samples via I2C
The STM32 continuously receives acceleration and gyroscope readings. These samples are used to update the vehicle’s movement.<br><br>

### Accelerometer & Gyroscope Calibration
The system applies calibration algorithms to correct errors in sensor readings. This improves the accuracy of the navigation system.<br><br>

### Raw Data Collection
The system initially stores unprocessed sensor data. This raw data is later refined to remove noise and errors.<br><br>

### Processed Sensor Data
The refined data is filtered and optimized for precise calculations. This ensures better decision-making for autonomous movement.<br><br>

### Position Estimation
The system estimates its position based on accelerometer and gyroscope readings. These readings help track real-time displacement and rotation.<br><br>

### Complementary Filter Application
A complementary filter combines accelerometer and gyroscope data. This improves position accuracy by balancing short-term and long-term sensor errors.<br><br>

## CAN Activities
- **Node 1**: Collects data from sensors like IMU and encoders.<br>
- **Message Preparation**: Data is packaged into a CAN message.<br>
- **Message Transmission**: Node 1 sends the message through the CAN bus.<br>
- **CAN Bus**: Acts as the communication network between all nodes.<br>
- **Node 2**: Receives messages from Node 1.<br>
- **Message Unpacking**: Extracts sensor data from CAN messages.<br>
- **Data Processing**: Filters, calibrates, and stores sensor information.<br>
- **Sensor Calibration**: Ensures accuracy and corrects potential errors.<br>
- **Raw vs. Processed Data**: Ensures only validated data is used for system functions.<br><br>

## Key Components
- **MPU9250**: Provides orientation and acceleration data.<br>
- **CAN Transceiver TJA1051**: Enables CAN bus communication.<br>
- **CAN Shield**: Interfaces microcontroller with the CAN network.<br>
- **Arduino Uno**: Manages sensors and actuators.<br>
- **NRF24**: Enables wireless communication.<br>
- **Encoder**: Measures wheel position and speed.<br>
- **Servo Motor**: Controls steering.<br>
- **ESC (Electronic Speed Controller)**: Regulates motor speed.<br><br>

## Results & Benefits
- **Accurate Navigation**: Improved waypoint tracking with minimal drift.<br>
- **Automation**: Reduced manual intervention and operator fatigue.<br>
- **Efficiency**: Optimized movement, reduced fuel consumption, and improved execution speed.<br>
- **Reliable Communication**: Stable data exchange via CAN Shield and Arduino Uno, ensuring smooth system operation.<br><br>

This system represents a significant step toward modernizing agriculture, offering farmers an intelligent solution for autonomous field operations.

