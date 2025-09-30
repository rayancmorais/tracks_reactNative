# 📍 Tracks: Real-Time Location Tracking App

A full-stack, cross-platform mobile application for tracking and logging user movement, built with **React Native** and a secure **Node.js/MongoDB** backend.

---

## ✨ Features

| Icon | Feature | Description |
| :---: | :--- | :--- |
| 🗺️ | **Live Location Tracking** | Actively tracks and displays the user's current location on an interactive map in real-time. |
| 🔐 | **Secure User Authentication** | Full signup and signin flow featuring robust password hashing and salting (using `bcrypt`). |
| 💾 | **Track Persistence** | Allows users to save their recorded tracks and view them later. |
| 🧭 | **Intuitive Navigation** | Clean, user-friendly interface powered by **React Navigation**. |
| 📱 | **Cross-Platform** | Built with React Native for deployment on both iOS and Android devices via Expo. |

---

## 🚀 Technical Stack

This project is divided into two parts: the mobile client (in this repository) and a companion Node/Express backend.

### Client (Mobile App)

| Component | Technology | Role |
| :--- | :--- | :--- |
| **Framework** | **React Native** | Building cross-platform mobile UIs. |
| **Navigation** | **React Navigation** | Handling app routing and screen management. |
| **Mapping** | **`react-native-maps`** | Providing a clear, interactive map interface. |
| **Icons** | **`@expo/vector-icons`** | High-quality vector icons for the UI. |

### Server (API & Database)

| Component | Technology | Role |
| :--- | :--- | :--- |
| **Server** | **Node.js & Express** | The backend API for handling requests and authentication. |
| **Database** | **MongoDB Atlas** | Cloud-hosted NoSQL database for storing user accounts and track data. |
| **Security** | **Password Hashing Library (e.g., `bcrypt`)** | Securely hashing and salting user passwords. |

---

## ⚙️ Getting Started

Follow these steps to set up the project on your local machine for development and testing.

### Prerequisites

* **Node.js** (LTS version recommended)
* **npm** or **yarn**
* **Expo Go** app installed on your mobile device (or a working emulator/simulator)
* **Ngrok** CLI installed and an account for exposing your local backend server.

### 1. Clone the Repositories

This project requires both the client and its server. Assuming the server code is in a dedicated folder (e.g., `tracks-server`).

```bash
# Clone the client (this repository)
git clone [https://github.com/rayancmorais/tracks_reactNative.git](https://github.com/rayancmorais/tracks_reactNative.git)
cd tracks_reactNative

# Install client dependencies
npm install # or yarn install
