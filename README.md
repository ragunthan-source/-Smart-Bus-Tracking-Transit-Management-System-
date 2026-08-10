# 🚌 Smart Bus Tracking & Transit Management System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-green.svg)](https://nodejs.org/)
[![React Native](https://img.shields.io/badge/Frontend-React_Native-61DAFB.svg)](https://reactnative.dev/)
[![Flutter](https://img.shields.io/badge/Frontend-Flutter-02569B.svg)](https://flutter.dev/)
[![Socket.io](https://img.shields.io/badge/RealTime-Socket.io-black.svg)](https://socket.io/)

**Smart Bus Tracking & Transit Management System** is a full-stack public transportation & transit tracking platform engineered to provide real-time bus locations, digital QR ticketing, automated stop announcements, and route management for commuters and transit operators.

---

## ✨ Features

- 🛰️ **Real-Time GPS Tracking**: Stream live bus coordinates from driver devices to passengers with low latency using **WebSockets (Socket.io)**.
- 📱 **Dual-Role Mobile Dashboards**:
  - **Passengers**: Search bus routes, view live positions, check arrival ETAs, and receive voice announcements.
  - **Drivers / Transit Operators**: Broadcast live locations, manage active routes, and view schedules.
- 🎟️ **QR Code Ticketing & Verification**: Integrated camera scanning (`expo-camera` / Flutter QR) for instant ticket validation.
- 🗣️ **Automated Voice Announcements**: Text-to-Speech (TTS) integration announcing upcoming stops and route alerts for commuters.
- 🗄️ **Dual Database Architecture**: Relational data (buses, schedules, drivers) in **MySQL** combined with real-time location logs in **MongoDB**.

---

## 🏗️ Architecture & Technology Stack

| Layer | Technologies |
| :--- | :--- |
| **Backend API** | Node.js, Express.js, JWT Authentication |
| **Real-Time Communication** | Socket.io (WebSockets) |
| **Databases** | MySQL (`mysql2`), MongoDB (`mongoose`) |
| **Mobile App (React Native)** | Expo, React Navigation, Expo Location, Expo Speech, Socket.io-client |
| **Mobile App (Flutter)** | Dart, Flutter SDK, Provider, Mobile Scanner |

---

## 📁 Repository Structure

```text
.
├── backend/             # Node.js Express server + Socket.io + Database models
│   ├── models/          # MongoDB location telemetry schema
│   ├── sql/             # MySQL schema definitions
│   ├── server.js        # Core REST & WebSocket server
│   └── db.js            # Database connections
├── mobile-app/          # Expo / React Native Mobile Application
│   ├── src/
│   │   ├── screens/     # Driver, Passenger, QR Scanner screens
│   │   └── services/    # Socket & API client logic
└── sihproject/          # Flutter Cross-Platform App (Android, iOS, Web)
    └── lib/             # Flutter screens, widgets, and state management
```

---

## ⚡ Quick Start & Setup

### Prerequisites
- [Node.js](https://nodejs.org/) (v16+)
- [MySQL Server](https://www.mysql.com/) & [MongoDB](https://www.mongodb.com/)
- [Expo CLI](https://docs.expo.dev/) (for React Native) or [Flutter SDK](https://docs.flutter.dev/get-started/install)

---

### 1. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install

# Configure environment variables
# Create a .env file with your DB credentials & JWT secret
PORT=5000
JWT_SECRET=your_jwt_secret
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=your_password
MYSQL_DATABASE=smart_bus
MONGO_URI=mongodb://localhost:27017/smart_bus

# Start the server
npm run dev
```

---

### 2. React Native App Setup

```bash
# Navigate to mobile app directory
cd mobile-app

# Install dependencies
npm install

# Start the Expo development server
npx expo start
```

---

### 3. Flutter App Setup

```bash
# Navigate to Flutter project directory
cd sihproject

# Get dependencies
flutter pub get

# Run the app
flutter run
```

---

## 🛡️ License

Distributed under the MIT License. See `LICENSE` for details.
