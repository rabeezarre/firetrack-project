# FireTrack - Wildfire Management System

## Table of Contents
- [About](#about)
    - [Features](#features)
    - [Sub-Systems](#sub-systems)
- [Project Status](#project-status)
- [Deployment](#deployment)
- [Technology Stack](#technology-stack)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
    - [Important Links](#important-links)
- [Contributing](#contributing)
- [License](#license)
- [Authors and Acknowledgment](#authors-and-acknowledgment)
- [Testing the Website](#testing-the-website)

## About
FireTrack is an integrated wildfire management system developed by rabeezarre, designed for monitoring, early detection, and efficient response to wildfires. It includes frontend, backend, mobile, and embedded components.

### Features
- Real-time monitoring of forest conditions.
- Tracking point inspections using mobile devices.
- Timely alerts for wildfire incidents.

### Sub-Systems
- **Web**: Interactive map with tracking point information.
- **Mobile**: Real-time tracking service for inspections.
- **Backend**: Centralized database using Spring Boot, Java 17, and Gradle.
- **Embedded Programming**: Utilizes LoRaWAN for data sharing.

## Project Status
In Progress

## Deployment
Deployed on CleverCloud: [firetrack.cleverapps.io](https://firetrack.cleverapps.io/)

## Technology Stack
- Backend: Java 17, Spring Boot, Gradle
- Frontend: Vue.js, SCSS, Bootstrap
- Database: H2 Database
- API Documentation: Swagger

## Installation and Setup
### Backend
1. Clone `git clone https://github.com/rabeezarre/firetrack-backend.git`
2. Navigate `cd firetrack-backend`
3. Build with Gradle `./gradlew build`
4. Add frontend build files to `src/main/resources/static`

### Frontend
1. Clone `git clone https://github.com/rabeezarre/firetrack-frontend.git`
2. Navigate `cd firetrack-frontend`
3. Install dependencies `npm install`
4. Compile for development `npm run serve`
5. Compile for production `npm run build`
6. Lint `npm run lint`
7. Copy build files to backend's static directory.

### Mobile
1. Prerequisites: Android Studio, Kotlin, Gradle.
2. Clone `git clone https://github.com/rabeezarre/firetrack-mobile.git`
3. Open and build in Android Studio.
4. Run on emulator or device.

### Embedded Programming
Clone `git clone https://github.com/rabeezarre/firetrack-embed.git`

#### `client_lora`
1. Assemble hardware with Adafruit Feather Bluefruit Sense and RFM95W LoRa Radio.
2. Install Visual Studio and CircuitPython plugin.
3. Clone, load CircuitPython code.

#### `server_wifi`
1. Assemble hardware with Adafruit HUZZAH32 and RFM95W LoRa Radio.
2. Install Arduino IDE and ESP32 package.
3. Clone, upload Arduino sketch.

## Usage
FireTrack provides various RESTful API endpoints:

### User Controller
- **GET** `/api/users/{userId}`: Retrieve user details by user ID.
- **PUT** `/api/users/{userId}`: Update user details.
- **DELETE** `/api/users/{userId}`: Delete a user.
- **POST** `/api/users/register`: Register a new user.
- **POST** `/api/users/login`: User login.

### Tracking Point Controller
- **GET** `/api/trackingPoints/{pointId}`: Get details of a specific tracking point.
- **PUT** `/api/trackingPoints/{pointId}`: Update a tracking point.
- **DELETE** `/api/trackingPoints/{pointId}`: Delete a tracking point.
- **GET** `/api/trackingPoints`: Retrieve all tracking points.
- **POST** `/api/trackingPoints`: Create a new tracking point.

### Alert Controller
- **PUT** `/api/alerts/{alertId}`: Update an alert.
- **GET** `/api/alerts`: Get all alerts.
- **POST** `/api/alerts`: Create a new alert.
- **GET** `/api/alerts/trackingPoint/{pointId}`: Get alerts for a specific tracking point.
- **GET** `/api/alerts/active`: Retrieve active alerts.

### Sensor Data Controller
- **POST** `/api/sensorData`: Submit new sensor data.
- **GET** `/api/sensorData/{pointId}`: Retrieve sensor data for a specific point.

### Scanning History Controller
- **GET** `/api/scanningHistory`: Get all scanning history records.
- **POST** `/api/scanningHistory`: Create a new scanning history record.
- **GET** `/api/scanningHistory/user/{userId}`: Get scanning history by user.
- **GET** `/api/scanningHistory/point/{pointId}`: Get scanning history for a specific point.

### Important Links
- Swagger UI: `/swagger-ui/index.html#/`
- H2 Database Console: `/h2-console/`

## Authors and Acknowledgment
Author: rabeezarre [GitHub](https://github.com/rabeezarre)

## Testing the Website
Access [firetrack.cleverapps.io](https://firetrack.cleverapps.io/) with email: worker@example.com and password: worker

For more details, please refer to the respective repositories on GitHub:
- [Backend Repository](https://github.com/rabeezarre/firetrack-backend)
- [Frontend Repository](https://github.com/rabeezarre/firetrack-frontend)
- [Mobile Repository](https://github.com/rabeezarre/firetrack-mobile)
- [Embedded Programming Repository](https://github.com/rabeezarre/firetrack-embed)
