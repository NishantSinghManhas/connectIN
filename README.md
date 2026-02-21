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