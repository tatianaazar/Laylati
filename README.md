# Laylati Project

This repository contains both the backend (Node.js/Express/TypeScript) and frontend (React Native/Expo) for the Laylati app.

---

## Prerequisites

- [Node.js](https://nodejs.org/) (v18+ recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) account (or local MongoDB)
- [Expo CLI](https://docs.expo.dev/get-started/installation/) (`npm install -g expo-cli`)
- (Optional) [Git](https://git-scm.com/)

---

## 1. Clone the Repository

```sh
git clone https://github.com/tatianaazar/Laylati.git
cd laylati
```

---

## 2. Backend Setup

### A. Install Dependencies

```sh
cd laylati-backend/laylati-backend
npm install
```

### B. Configure Environment Variables

- In the `.env` file in the 'laylati-backend' folder, add the connection string URI for your created MongoDB cluster:

  ```
  MONGODB_URI=your_mongodb_connection_string

  ```
- Update the `MONGODB_URI` with your MongoDB Atlas connection string or local MongoDB connection details. This should be a cluster created in MongoDB Atlas or a local MongoDB instance. 

### C. Build and Start the Server

```sh
npm run build
npm start
```
- The backend should run on [http://localhost:5000](http://localhost:5000) by default.
- 'MongoDB Connected' will be displayed if the connection to the database is successful. 

---

## 3. Frontend Setup

### A. Install Dependencies

```sh
cd ../../laylati-frontend/laylati-frontend
npm install
```

### B. Configure API URLs

- Update API URLs in `constants/api.ts` or wherever your frontend fetches data, to point to your backend server (e.g., `http://localhost:5000` or your LAN IP if testing on a device).

### C. Start the Expo App

```sh
npm start
```
- Scan the QR code with [Expo Go](https://expo.dev/client) on your phone, or run on an emulator.

---

## 4. Notes

- Make sure your backend is running and accessible from your device (use LAN IP if testing on a real device).
- For Google Sheets integration, ensure your credentials and tokens are set up as described in the backend scripts.
- If you use environment variables in the frontend, consider using a library like `expo-constants` or `.env` files with [react-native-dotenv](https://github.com/goatandsheep/react-native-dotenv).

---

## 5. Troubleshooting

- If you get network errors on Expo Go, ensure your phone and computer are on the same network, or use Expo's Tunnel mode.
- If MongoDB connection fails, check your `.env` and MongoDB Atlas IP whitelist.

---

## 6. Scripts

- **Backend**
  - `npm run build` — Compile TypeScript
  - `npm start` — Start backend server

- **Frontend**
  - `npm start` — Start Expo development server

---

## License

MIT