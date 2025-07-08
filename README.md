# Scrap Pickup Platform

A React Native-based platform for scheduling and managing scrap pickups, consisting of two apps: **Customer App** and **Partner App**, powered by a shared `json-server` mock API. The Customer App allows users to schedule scrap pickups, while the Partner App enables partners to accept, process, and submit items for approval. The project uses TypeScript, `react-native-paper` for UI, and `@notifee/react-native` for notifications.

## Features
- **Customer App**: Phone/OTP login, schedule pickups, view order history, logout, and receive login notifications.
- **Partner App**: Phone/OTP login, accept/process pickups, submit items for approval, and receive login notifications.
- **Mock API**: `json-server` with `db.json` for users and pickups, served at `http://localhost(yourip address):3000/users`.

## Project Structure scrap-pickup-platform/
├── mock-api/
│   ├── db.json
│   ├── package.json
│   └── package-lock.json
├── customer-app/
│   ├── src/
│   │   ├── api/
│   │   │   └── api.ts
│   │   ├── components/
│   │   │   ├── Button.tsx
│   │   │   ├── InputField.tsx
│   │   │   └── PickupCard.tsx
│   │   ├── context/
│   │   │   └── AppContext.tsx
│   │   ├── navigation/
│   │   │   └── AppNavigator.tsx
│   │   ├── screens/
│   │   │   ├── DashboardScreen.tsx
│   │   │   ├── LoginScreen.tsx
│   │   │   ├── OrderHistoryScreen.tsx
│   │   │   └── SchedulePickupScreen.tsx
│   │   ├── types/
│   │   │   └── index.ts
│   │   ├── utils/
│   │   │   └── constants.ts
│   │   └── assets/
│   ├── App.tsx
│   ├── package.json
│   ├── tsconfig.json
│   ├── android/
│   ├── ios/
│   └── README.md
├── partner-app/
│   ├── src/
│   │   ├── api/
│   │   │   └── api.ts
│   │   ├── components/
│   │   │   ├── Button.tsx
│   │   │   ├── InputField.tsx
│   │   │   ├── PickupCard.tsx
│   │   │   └── ItemInputForm.tsx
│   │   ├── context/
│   │   │   └── AppContext.tsx
│   │   ├── navigation/
│   │   │   └── AppNavigator.tsx
│   │   ├── screens/
│   │   │   ├── AvailablePickupsScreen.tsx
│   │   │   ├── DashboardScreen.tsx
│   │   │   ├── InProcessPickupsScreen.tsx
│   │   │   └── LoginScreen.tsx
│   │   ├── types/
│   │   │   └── index.ts
│   │   ├── utils/
│   │   │   └── constants.ts
│   │   └── assets/
│   ├── App.tsx
│   ├── package.json
│   ├── tsconfig.json
│   ├── android/
│   ├── ios/
│   └── README.md
├── .gitignore
└── README.md



## Prerequisites
- **Node.js**: v18 or higher
- **React Native CLI**: `npm install -g react-native-cli`
- **json-server**: `npm install -g json-server`
- **Android SDK** (for Android) or **Xcode** (for iOS)
- **Physical device/emulator** on the same network as the API server
- **ADB** (for USB debugging, optional)

## Quick Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/scrap-pickup-platform.git
   cd scrap-pickup-platform

Mock API:Navigate to mock-api:bash

cd mock-api
npm install
json-server --watch db.json --port 3000

Update customer-app/src/utils/constants.ts and partner-app/src/utils/constants.ts with your local IP (e.g., http://localhost(yourip address):3000/users.).
Test: curl http://localhost(yourip address):3000/users.


