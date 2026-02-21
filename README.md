# connectIN

A LinkedIn-style alumni networking app with authentication, profiles, posts (images/GIFs/videos), real-time chat/notifications, mentorship matching, and basic analytics.

## Tech Stack
- **Client:** React + Vite + Tailwind
- **Server:** Node.js + Express + MongoDB (Mongoose)
- **Realtime:** Socket.IO
- **Media storage:** Cloudinary

## Monorepo Structure
- `client/` – React frontend
- `server/` – Express API + Socket.IO + MongoDB models

## Prerequisites
- Node.js 18+ (recommended)
- MongoDB connection string (local or Atlas)
- Cloudinary account (for uploads)

## Environment Variables

Create `server/.env`:

```env
PORT=5000
MONGO_URI=mongodb+srv://...
JWT_SECRET=your_long_random_secret

# Google OAuth (Sign-in)
GOOGLE_CLIENT_ID=130574480266-4qeuib68n1ok96g822u5q8dkotuah1jf.apps.googleusercontent.com

# Cloudinary
CLOUDINARY_CLOUD_NAME=...
CLOUDINARY_API_KEY=...
CLOUDINARY_API_SECRET=...

Notes:

JWT_SECRET must match what the client uses via the API token flow.
Cloudinary is required for avatar/cover and post media uploads.
Create client env files (Vite):

client/.env.local (local dev):

VITE_API_BASE_URL=http://localhost:5000/api
VITE_SOCKET_URL=http://localhost:5000
VITE_GOOGLE_CLIENT_ID=130574480266-4qeuib68n1ok96g822u5q8dkotuah1jf.apps.googleusercontent.com

Production (set in hosting provider or client/.env.production)

VITE_API_BASE_URL=https://YOUR-RENDER-BACKEND.onrender.com/api
VITE_SOCKET_URL=https://YOUR-RENDER-BACKEND.onrender.com

## Install

From the repo report:

cd server
npm install

cd ../client
npm install

## Run (Development)

Start the API server:

cd server
npm run dev
# or: npm start

Start the client:

cd client
npm run dev

Default URLs:

Client: http://localhost:5173
Server: http://localhost:5000