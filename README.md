# 🚍 PassEase – Smart Bus Pass Management System

**PassEase** is a digital platform that automates the traditional bus pass generation system, especially aimed at student commuters and public transport users. It eliminates the need for offline processes and integrates secure online registration, document upload, admin verification, QR code validation, and payment through Razorpay – all inside a mobile-first user experience.

---

## 📌 Project Highlights

- 📱 Mobile-first app built using **React Native + Expo**
- 📁 Upload PDF and profile picture to **Cloudinary**
- 🔐 Secure **Login & Registration** with role-based access
- 🛂 **Admin Dashboard** to approve/reject applications
- 📤 QR code generation for **pass verification**
- 💳 Payment processing with **Razorpay**
- 🧾 MongoDB database integration
- 📊 Real-time application status tracking

---

## 🧰 Tech Stack

| Layer     | Technologies Used        |
|-----------|--------------------------|
| Frontend  | React Native (Expo)      |
| Backend   | Node.js, Express.js      |
| Database  | MongoDB (Mongoose)       |
| Storage   | Cloudinary               |
| Payment   | Razorpay API             |
| Others    | QR Code, JWT, Axios, Multer |

---

## 🛠️ Installation & Setup Guide

### 1. 🔁 Clone the Repository

git clone https://github.com/LeORM96/PassEase.git
cd PassEase

2. ⚙️ Backend Setup

cd backend
npm install

Create .env file inside backend/:

PORT=5000
MONGO_URI=your_mongo_db_connection_string
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
JWT_SECRET=your_jwt_secret

Start the backend server:
npm run dev

3. 📱 Frontend Setup (React Native + Expo)
cd ../frontend
npm install

Start the frontend Expo server:
expo start
You can scan the QR code with Expo Go on your mobile device to open the app.

✅ Features Breakdown

Feature	                    Description
📝 Registration	            Users register and upload documents
🔑 Authentication	        JWT-based login and protected routes
📂 File Upload	            Uploads documents & images to Cloudinary
🎛️ Admin Panel	            View, verify, and reject user applications
📦 QR Code	                Generated post-verification; used for validation
💵 Razorpay	                Online payment for pass processing
🧾 Status Tracker	        Users can monitor current application/payment status


📬 API Endpoints Overview

🔐 Auth
POST /api/register – Register a new user
POST /api/login – Login and receive token

📄 File & Profile Upload
POST /api/upload – Upload profile picture and documents

🧾 Application Status
GET /api/status/:userId – Get status of application

🧑‍💼 Admin
GET /api/admin/users – List all pending applications
POST /api/admin/verify/:id – Approve a user
POST /api/admin/reject/:id – Reject a user

💳 Payment
POST /api/payment/create – Initiate Razorpay order
POST /api/payment/verify – Confirm payment success

🔮 Upcoming Enhancements

OTP Verification during registration
Email/SMS alerts on application updates
Pass history download (PDF export)
Rich admin analytics panel


