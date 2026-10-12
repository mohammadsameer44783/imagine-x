# 🌌 Imaginex

**Imaginex** is a modern AI-powered social media platform where creativity meets artificial intelligence. Users can generate AI art, share posts, follow creators, and engage with a community built entirely around machine-generated visuals.

---

## 🚀 Overview

Imaginex combines the power of AI image generation with a full-featured social networking experience. The platform allows users to transform ideas into visuals using prompts, publish their creations, and interact with other creators through likes, follows, and feeds.

It is built using the **MERN stack** and integrates an **AI image generation API** to deliver real-time creative results.

---

## ✨ Features

- 🔐 Authentication & Authorization (JWT based)
- 👤 User Profiles
- 🎨 AI Image Generation from prompts
- 📰 Feed system (latest + following)
- ❤️ Like / Unlike posts
- ➕ Follow / Unfollow users
- 🖼 Post sharing system
- 🔎 Explore page
- 📱 Responsive UI
- ⚡ Real-time experience

---

## 🛠 Tech Stack

**Frontend**

- React.js
- Axios
- Tailwind / CSS
- Redux / Context API

**Backend**

- Node.js
- Express.js

**Database**

- MongoDB
- Mongoose ODM

**AI Integration**

- Image Generation API (Prompt → Image)

---

## ⚙️ Environment Variables

Create a `.env` file in the project root directory (or copy `.env.example`):

```bash
cp .env.example .env
```

| Variable | Description | Default / Example |
| :--- | :--- | :--- |
| `PORT` | Backend server port (must match Vite proxy: 8080) | `8080` |
| `NODE_ENV` | Application environment (`development` or `production`) | `development` |
| `MONGO_URI` | MongoDB connection string (Local or MongoDB Atlas) | `mongodb://localhost:27017/imaginex` |
| `JWT_SECRET` | Secret key used to sign and verify JSON Web Tokens | `your_jwt_secret_key_here` |
| `GEMINI_API_KEY` | Google Gemini API Key for AI Image Generation | `your_gemini_api_key_here` |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary Cloud Name for storing generated images | `dqdejbfnx` |
| `CLOUDINARY_API_KEY` | Cloudinary API Key | `your_cloudinary_api_key_here` |
| `CLOUDINARY_API_SECRET` | Cloudinary API Secret | `your_cloudinary_api_secret_here` |

---

## 🏃 Getting Started

### 1. Install Dependencies
```bash
# Install root/server dependencies and client dependencies
npm run build
```

### 2. Configure Environment
Set up your `.env` file with your MongoDB URI, Gemini API Key, and Cloudinary keys.

### 3. Run Development Servers
```bash
npm run dev
```
- Frontend: `http://localhost:5173`
- Backend API: `http://localhost:8080`

---

## 🚀 Deploying to Render

This project is configured to deploy as a unified **Render Web Service** (serving the API + built React frontend from a single service).

### Deployment Settings on Render:
- **Environment**: `Node`
- **Build Command**: `npm run build`
- **Start Command**: `npm start`

### Required Environment Variables on Render:
| Variable | Value / Description |
| :--- | :--- |
| `NODE_ENV` | `production` *(tells Express to serve the built frontend)* |
| `MONGO_URI` | Cloud MongoDB URI (e.g. from MongoDB Atlas) |
| `JWT_SECRET` | Strong secret string |
| `GEMINI_API_KEY` | Your Google Gemini API Key |
| `CLOUDINARY_CLOUD_NAME` | `dqdejbfnx` or your Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Your Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Your Cloudinary API secret |

*(Note: Render automatically sets `PORT`, which the server binds to automatically).*
