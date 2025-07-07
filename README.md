# 🩺 Doctor Appointment App (Role-Based Access)

A powerful, cross-platform mobile app built for doctors and patients. Users can sign up as **Doctor** or **Patient** and experience a fully role-based system for healthcare management, appointment booking, prescriptions, and consultations — all in one app.

## 🚀 Features Overview

### 🔐 Role-Based Access
- One unified app
- Users select a role on login: **Doctor** or **Patient**
- Different dashboards, permissions & UI per role

## 👨‍⚕️ Doctor Features

| Feature                   | Description                                           |
|---------------------------|-------------------------------------------------------|
| 🗓️ View Appointments       | View upcoming, pending, and completed appointments     |
| 📅 Set Availability        | Define working hours and time slots                   |
| 👤 Patient Records         | View medical history and visit details                 |
| 💊 Upload Prescriptions    | Digitally send prescriptions to patients              |
| ✏️ Edit Profile            | Update bio, fees, image, and specialization           |
| ✅ Accept/Reject Bookings  | Approve or reject appointment requests                |
| ⭐ View Ratings & Reviews  | See patient feedback after consultations              |

## 👤 Patient Features

| Feature                   | Description                                           |
|---------------------------|-------------------------------------------------------|
| 🔍 Search Doctors          | Filter by name, specialty, or rating                  |
| 📅 Book Appointments       | Select doctor, choose time, and book                 |
| 🧾 View Prescriptions      | View/download prescription given by doctor           |
| 🕒 Appointment History     | See past and upcoming appointments                   |
| ⭐ Leave Reviews           | Give feedback & rate the doctor                      |
| ✏️ Edit Profile            | Manage personal info and update profile              |
| 💳 Payment (future)        | Online fee payment option *(optional)*               |

## 🛠️ Tech Stack

| Layer         | Technology                         |
|---------------|-------------------------------------|
| Frontend      | React Native CLI                    |
| Auth          | Firebase Authentication             |
| Backend       | Firebase Firestore (NoSQL DB)       |
| Media Upload  | Firebase Storage                    |
| Video Call    | WebRTC + Socket.IO                  |
| Notifications | Firebase Cloud Messaging (FCM)      |
| Admin Panel   | React JS + Tailwind CSS *(optional)*|

## 📬 Push Notifications

Push notifications are implemented using **Firebase Cloud Messaging (FCM)** to ensure real-time communication between the app and users.

### 🔔 Key Highlights:
- Firebase Cloud Messaging (FCM) integrated
- Role-based notification logic (Doctor vs Patient)
- Triggered automatically via Firestore triggers or manually via admin

### 🔔 Notifications Sent For:
- ✅ **Booking Confirmation** – when a user books an appointment
- ⏰ **Upcoming Appointment Reminder** – alert before appointment
- 🌟 **New Review Received** – doctor notified after feedback
- 💊 **New Prescription Uploaded** – patient notified instantly

## 🎥 Real-Time Video & Audio Calls

Real-time consultation is powered by **WebRTC** and **Socket.IO**, allowing live audio/video communication between doctors and patients.

### 🎯 Core Functionality:
- 1-on-1 live video consultation
- Seamless real-time communication
- Socket.IO used for signaling and connection setup

### 🛠️ Future Capabilities:
- 🧑‍🤝‍🧑 **Group Video Calls**
- 📤 **Screen Sharing**
- 📲 **Consultation Recording (Premium Version)**

## 🔒 Authentication & Security

Authentication and role management are securely handled using **Firebase Authentication** and **Firestore Security Rules**.

### 🔐 Auth Flow:
- Firebase Email/Password based login/signup
- Role (`doctor` or `patient`) is saved in Firestore upon registration
- Role-based navigation and access controlled from app side

### 🔐 Firestore Rules:
- Read/write access strictly filtered by user `uid` and `role`
- Example: Patient can't read other patients' prescriptions

### 🔐 Device Permissions:
- **Camera/Mic Access** – Required only during video calls
- **Secure Prompting** – OS-native permission request handled safely

## 📌 Future Enhancements

| Feature                        | Description                                      |
|-------------------------------|--------------------------------------------------|
| 💬 In-App Chat                 | Real-time messaging between doctor & patient     |
| 🎥 Video Consultation Module   | 1:1 high-quality video call system               |
| 📊 Admin Analytics Dashboard   | Graphs, reports, and user statistics             |
| 📧 Email or OTP Login          | Secure alternatives to password login            |
| ✅ Doctor Approval Flow        | Admin must approve before doctor goes live       |
| 💳 Payment Integration         | Online consultation fee via Stripe/Razorpay      |
| 🌐 Multi-language Support      | Support for EN, URDU, and more                   |

## 🗂️ Project Structure

mydoctor-app/
├── assets/ # Static assets (images, icons)
├── components/ # Reusable UI components
│ ├── common/ # Generic components
│ ├── doctor/ # Doctor-specific components
│ └── patient/ # Patient-specific components
├── config/ # App configuration
├── context/ # React context providers
├── navigation/ # App navigation
│ ├── DoctorStack.js # Doctor navigation
│ └── PatientStack.js # Patient navigation
├── screens/ # App screens
│ ├── auth/ # Authentication screens
│ ├── doctor/ # Doctor screens
│ └── patient/ # Patient screens
├── services/ # Business logic
│ ├── auth.js # Auth services
│ ├── firestore.js # Database operations
│ └── notification.js # Push notifications
├── styles/ # Global styles
└── utils/ # Helper functions



## 📥 Installation Guide

### Prerequisites
- Node.js (v14+)
- npm/yarn
- Expo CLI (if using Expo)
- Firebase account

### Setup Instructions
1. Clone the repository:
```bash
git clone https://github.com/danishshabbir-dev/Doctor-Appointment-App.git
cd Doctor-Appointment-App

npm install
# or
yarn install

npm run android

🤝 Contributing
Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE for more information.

✉️ Contact
Danish Shabbir - danishshabbir.dev@gmail.com
Project Link: https://github.com/danishshabbir-dev/Doctor-Appointment-App


This comprehensive README includes:
1. All features organized by role
2. Complete tech stack details
3. Project structure visualization
4. Detailed installation instructions
5. Contribution guidelines
6. License and contact information

The document is well-formatted for GitHub Markdown and provides everything a developer or user would need to understand and work with this project.
