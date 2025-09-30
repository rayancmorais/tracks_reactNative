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

```

## 2. Set Up the Backend

The mobile client needs a running, publicly accessible backend to connect to for authentication and data management.

1.  **Navigate to your server directory** (e.g., `tracks-server`).
2.  **Start the Node.js server:**
    ```bash
    npm start # or node index.js
    ```
3.  **Expose the server using Ngrok:** In a new terminal window, run Ngrok, specifying the port your Node.js server is running on (e.g., port 3000):
    ```bash
    ngrok http 3000
    ```
    This will generate a unique HTTPS forwarding URL (e.g., `https://abcdef12345.ngrok.io`). **This is your `API_URL`**.

## 3. Configure the Mobile Client

1.  In the client repository (`tracks_reactNative`), locate where the API URL is defined (e.g., in a file like `src/api/tracker.js`).
2.  **Update the `API_URL`** to the HTTPS URL provided by Ngrok.

    ```javascript
    // Example: src/api/tracker.js
    // Change this base URL every time you restart your Ngrok session!
    const instance = axios.create({
      baseURL: 'YOUR_NGROK_HTTPS_URL_HERE' 
    });
    ```

## 4. Run the Mobile App

Start the Expo development server:

```bash
npm start # or yarn start

1.  A **QR code** will appear in your terminal.
2.  Open the **Expo Go** app on your phone and scan the QR code to load the application.
3.  Alternatively, press `a` for Android emulator or `i` for iOS simulator.

