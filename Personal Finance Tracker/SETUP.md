# 🚀 Spendly Setup Guide

This guide will help you set up the Spendly Personal Finance Tracker project on your local machine and deploy it to the GitHub repository.

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v16 or higher)
- [Git](https://git-scm.com/)
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- A code editor (VS Code recommended)

## 🔧 Step-by-Step Setup

### 1. Clone and Setup Repository

```bash
# Clone the repository
git clone https://github.com/Swapnaja7/Spendly.git
cd Spendly

# Initialize git (if not already done)
git init
git remote add origin https://github.com/Swapnaja7/Spendly.git
```

### 2. Backend Environment Setup

Create a `.env` file in the `backend/` directory:

```bash
cd backend
touch .env
```

Add the following content to `backend/.env`:

```env
# Database Configuration
MONGODB_URI=mongodb://localhost:27017/spendly

# JWT Configuration
JWT_SECRET=your_super_secret_jwt_key_here_make_it_long_and_random

# Google OAuth Configuration
GOOGLE_CLIENT_ID=your_google_client_id_here
GOOGLE_CLIENT_SECRET=your_google_client_secret_here
GOOGLE_CALLBACK_URL=http://localhost:5000/api-v1/auth/google/callback

# Server Configuration
PORT=5000
NODE_ENV=development

# Frontend URL (for CORS and redirects)
FRONTEND_URL=http://localhost:5173
```

### 3. Frontend Environment Setup

Create a `.env` file in the `frontend/` directory:

```bash
cd ../frontend
touch .env
```

Add the following content to `frontend/.env`:

```env
# Google OAuth Configuration
VITE_GOOGLE_CLIENT_ID=your_google_client_id_here

# API Configuration
VITE_API_URL=http://localhost:5000/api-v1

# Optional: Environment
VITE_NODE_ENV=development
```

### 4. Install Dependencies

```bash
# Install backend dependencies
cd ../backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 5. Google OAuth Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select an existing one
3. Enable the Google+ API
4. Go to "Credentials" → "Create Credentials" → "OAuth 2.0 Client IDs"
5. Set application type to "Web application"
6. Add authorized redirect URIs:
   - `http://localhost:5000/api-v1/auth/google/callback`
   - `http://localhost:5173`
7. Copy the Client ID and Client Secret
8. Update both `.env` files with these values

### 6. Database Setup

#### Option A: Local MongoDB
```bash
# Install MongoDB locally or use Docker
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

#### Option B: MongoDB Atlas
1. Go to [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create a free cluster
3. Get your connection string
4. Update `MONGODB_URI` in `backend/.env`

### 7. Start the Application

```bash
# Terminal 1: Start Backend
cd backend
npm start

# Terminal 2: Start Frontend
cd frontend
npm run dev
```

The application should now be running at:
- Frontend: http://localhost:5173
- Backend: http://localhost:5000

## 🚀 Deployment to GitHub

### 1. Initial Commit

```bash
# Add all files
git add .

# Initial commit
git commit -m "Initial commit: Add Spendly Personal Finance Tracker"

# Push to main branch
git push -u origin main
```

### 2. Verify on GitHub

Visit [https://github.com/Swapnaja7/Spendly](https://github.com/Swapnaja7/Spendly) to see your project.

## 🔍 Troubleshooting

### Common Issues

1. **Port already in use**
   ```bash
   # Kill process using port 5000
   lsof -ti:5000 | xargs kill -9
   ```

2. **MongoDB connection failed**
   - Check if MongoDB is running
   - Verify connection string in `.env`
   - Ensure network access (for Atlas)

3. **Google OAuth not working**
   - Verify Client ID and Secret in both `.env` files
   - Check redirect URIs in Google Cloud Console
   - Ensure API is enabled

4. **Frontend can't connect to backend**
   - Check if backend is running
   - Verify `VITE_API_URL` in frontend `.env`
   - Check CORS configuration in backend

### Environment Variables Checklist

- [ ] `JWT_SECRET` (backend)
- [ ] `GOOGLE_CLIENT_ID` (both)
- [ ] `GOOGLE_CLIENT_SECRET` (backend)
- [ ] `MONGODB_URI` (backend)
- [ ] `VITE_API_URL` (frontend)

## 📱 Testing the Application

1. **Sign Up**: Create a new account
2. **Login**: Test both email/password and Google OAuth
3. **Add Account**: Create a test bank account
4. **Add Transaction**: Log a test transaction
5. **Create Budget**: Set up a monthly budget
6. **View Analytics**: Check charts and reports

## 🌐 Production Deployment

### Backend (Render/Heroku)
1. Connect your GitHub repository
2. Set environment variables
3. Deploy automatically on push

### Frontend (Vercel/Netlify)
1. Connect your GitHub repository
2. Build command: `npm run build`
3. Output directory: `dist`
4. Deploy automatically on push

## 📚 Additional Resources

- [React Documentation](https://react.dev/)
- [Node.js Documentation](https://nodejs.org/docs/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [Google OAuth Documentation](https://developers.google.com/identity/protocols/oauth2)

## 🤝 Support

If you encounter any issues:
1. Check the troubleshooting section above
2. Review the console logs
3. Open an issue on GitHub
4. Check the README.md for additional information

---

**Happy coding! 🎉**
