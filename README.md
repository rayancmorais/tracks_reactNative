# tracks_reactNative

An app that uses maps to track the user's location. This project is built with React Native and features secure user authentication with a Node.js backend.

---

### Features

* **Location Tracking:** Actively tracks and displays the user's current location on a map.
* **Secure User Authentication:** Implements a signup and signin flow with password hashing and salting for security.
* **Map View:** Provides a clear, interactive map interface powered by `react-native-maps`.
* **User Interface:** A simple and intuitive UI built with React Native components.

---

### Technologies Used

* **React Native:** The framework for building the mobile application.
* **React Navigation:** Handles navigation between different screens of the app.
* **React Native Maps:** A component library to integrate map views and markers.
* **MongoDB Atlas:** A cloud-based database for storing user information and tracks.
* **Node.js & Express:** Used to create the backend API for handling data and authentication.
* **Ngrok:** Exposes the local backend server to the internet for development and testing.
* **Password Hashing Library (e.g., bcrypt):** Used to securely hash and salt user passwords.
* **`@expo/vector-icons`:** Provides a set of vector icons for the UI.

---

### Getting Started

To get a copy of the project up and running on your local machine, follow these steps.

#### Prerequisites

* Node.js (LTS version recommended)
* npm or yarn
* A mobile device or an emulator with Android/iOS
* An Ngrok account and the Ngrok CLI installed

#### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/rayancmorais/tracks_reactNative.git](https://github.com/rayancmorais/tracks_reactNative.git)
    cd tracks_reactNative
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    ```
3.  **Set up the backend:**
    * Navigate to the `tracks-server` directory within this project.
    * Start the Node.js server.
    * In a separate terminal, use Ngrok to expose your local server to the public internet. This will generate a unique HTTPS forwarding URL.
    * Update the `API_URL` variable in the React Native project to this new Ngrok URL.

4.  **Run the app:**
    Start the development server.
    ```bash
    npm start
    # or
    yarn start
    ```
    * Scan the QR code displayed in the terminal with the Expo Go app on your phone.
    * Alternatively, press `a` for Android emulator or `i` for iOS simulator.
