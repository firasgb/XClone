🐦 X Clone - Twitter/X Clone
A full-stack Twitter/X clone built with the MERN stack (MongoDB, Express, React, Node.js) featuring real-time social interactions, JWT authentication, and admin capabilities.

✨ Features

👤 User Features
✅ Secure Authentication – JWT-based login/signup with HTTP-only cookies
✅ Create Posts – Text, image, or both (Cloudinary integration)
✅ Like/Comment – Interact with posts in real-time
✅ Follow System – Follow/unfollow other users
✅ Real-time Notifications – Get notified for interactions
✅ Profile Management – Customizable profiles with verification badges
✅ Responsive Design – Mobile-friendly interface

⚙️ Admin Features
✅ User Management – View, update, and delete users
✅ Verification Management – Grant/revoke blue badges
✅ Statistics Dashboard – Platform insights and metrics

🛠️ Tech Stack

Frontend
React – UI library with Vite
Tailwind CSS – Utility-first CSS framework
DaisyUI – Component library
React Query – Data fetching & state management
React Icons – Icon library
React Hot Toast – Toast notifications

Backend
Node.js – Runtime environment
Express.js – Web framework
MongoDB – NoSQL database
Mongoose – ODM for MongoDB
JWT – Authentication
Bcryptjs – Password hashing
Cloudinary – Image hosting

🚀 Quick Start

Prerequisites
Node.js (v16+)
MongoDB (local or Atlas)
npm or yarn

Installation
Clone the repository
bash
git clone https://github.com/your-username/X_Clone.git
cd X_Clone

Setup environment variables
bash
# Copy environment example file
cp .env.example .env
Edit .env with your credentials:

MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
PORT=5000
CLIENT_URL=http://localhost:4000

Install dependencies
bash
# Backend dependencies
cd server
npm install

# Frontend dependencies
cd ../client
npm install
Run the application

bash
# From project root (recommended)
npm run dev

# Or run separately:
# Terminal 1 - Start backend
cd server
npm run dev
Backend API: ⚙️ http://localhost:5000/api

# Terminal 2 - Start frontend
cd client
npm run dev
Frontend: 🌐 http://localhost:4000

📁 Project Structure

X_Clone/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── pages/        # Page components (Home, Profile, etc.)
│   │   ├── hooks/        # Custom React hooks
│   │   ├── contexts/     # React contexts (Auth, Theme)
│   │   └── utils/        # Utility functions
│   ├── public/
│   └── vite.config.js    # Vite configuration
├── server/                 # Express backend
│   ├── controllers/       # Route controllers
│   ├── models/           # Mongoose models (User, Post, Notification)
│   ├── routes/           # API endpoints
│   ├── middleware/       # Authentication middleware
│   ├── security/         # JWT & cookie utilities
│   └── .env              # Environment variables
├── .env.example           # Environment template
└── README.md             # Project documentation

🐛 Common Issues & Troubleshooting

Issue	Solution
ECONNREFUSED from Vite proxy	Ensure backend is running on port 5000 and check client/vite.config.js
MongoDB connection error	Verify MONGODB_URI in .env and ensure MongoDB is running
JWT token not working	Check JWT_SECRET in environment variables
Cloudinary upload fails	Verify Cloudinary credentials in .env
CORS errors	Ensure CLIENT_URL is correctly set in backend CORS configuration
