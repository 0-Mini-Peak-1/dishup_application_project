# DishUp Application

A mobile application development project for CSC452 Mobile Programming. 

DishUp allows you to manage and maintain your health simply by planning your meals with good nutrition. You can also track your daily routine, whether it's an exercise routine or your sleep hours. This app motivates you to become healthy in a long, sustainable path.

> **Note:** This repository contains both the **Frontend** (Flutter) and **Backend** (Node.js) for the application.

## Tech Stack
* **Frontend:** Flutter (Dart)
* **Backend:** Node.js, Express.js
* **Database:** MySQL / TiDB Cloud

## Getting Started

To run this project, you need to set up both the backend server and the mobile app.

### 1. Prerequisites
* [Flutter SDK](https://flutter.dev/docs/get-started/install) installed.
* [Node.js](https://nodejs.org/) installed.
* An Android Emulator or Physical Device.

### 2. Backend Setup
The backend must be running for the app to function.

1.  Navigate to the backend folder:
    ```bash
    cd dishup-backend
    ```
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  **Create a `.env` file** inside the `dishup-backend` folder with the following credentials:
    ```env
    DB_HOST=your_host_here
    DB_PORT=4000
    DB_USER=your_user
    DB_PASSWORD=your_password
    DB_NAME=dishup-project
    ```
4.  Start the server:
    ```bash
    npm run start
    # or
    node server.js
    ```
    *You should see: "Server running at http://localhost:3000"*

### 3. Frontend Setup
Open a new terminal window (do not close the backend terminal).

1.  Return to the root project folder:
    ```bash
    cd ..
    ```
2.  Install Flutter dependencies:
    ```bash
    flutter pub get
    ```
3.  **Create a `.env` file** in the root folder (if using flutter_dotenv) for your API URL:
    ```env
    # For Android Emulator, use 10.0.2.2 instead of localhost
    BASE_URL=[http://10.0.2.2:3000](http://10.0.2.2:3000)
    ```
4.  Run the application:
    ```bash
    flutter run
    ```

## Troubleshooting

**App won't login / Network Error?**
If you are testing on an **Android Emulator**, you cannot use `localhost` to connect to your computer. You must use the special Android alias IP:
* **Correct:** `http://10.0.2.2:3000`
* **Incorrect:** `http://localhost:3000`

Ensure your `android/app/src/main/AndroidManifest.xml` allows cleartext traffic:
```xml
<application android:usesCleartextTraffic="true" ... >
```

This is a final course project for **educational purposes** only.
