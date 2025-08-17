# 💰 Spendly - Personal Finance Tracker

A comprehensive personal finance management application that helps you track transactions, manage budgets, monitor accounts, and gain insights into your spending habits.

## ✨ Features

- **🔐 Secure Authentication**
  - Traditional email/password login
  - Google OAuth integration
  - JWT-based session management

- **💳 Account Management**
  - Multiple account types (Savings, Checking, Credit Cards)
  - Account balance tracking
  - Transfer between accounts

- **📊 Transaction Tracking**
  - Add, edit, and categorize transactions
  - Date-based filtering and search
  - Transaction history and analytics

- **🎯 Budget Management**
  - Set monthly budgets by category
  - Track spending against budgets
  - Visual progress indicators

- **📈 Analytics & Insights**
  - Spending trends and patterns
  - Category-wise expense breakdown
  - Interactive charts and graphs

- **⚙️ User Settings**
  - Profile management
  - Password changes
  - Dark/Light theme support

## 🚀 Tech Stack

### Frontend
- **React 18** with Vite
- **Tailwind CSS** for styling
- **Zustand** for state management
- **React Router** for navigation
- **React Hook Form** with Zod validation
- **Google OAuth** integration

### Backend
- **Node.js** with Express
- **MongoDB** with Mongoose
- **JWT** for authentication
- **Passport.js** for OAuth strategies
- **bcrypt** for password hashing

## 📋 Prerequisites

- Node.js (v16 or higher)
- MongoDB database
- Google OAuth credentials
- Git

## 🛠️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/Swapnaja7/Spendly.git
cd Spendly
```

### 2. Backend Setup
```bash
cd backend
npm install

# Create .env file
cp .env.example .env
# Edit .env with your configuration

npm start
```

### 3. Frontend Setup
```bash
cd frontend
npm install

# Create .env file
cp .env.example .env
# Edit .env with your configuration

npm run dev
```

## ⚙️ Environment Variables

### Backend (.env)
```env
JWT_SECRET=your_super_secret_jwt_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:5000/api-v1/auth/google/callback
MONGODB_URI=your_mongodb_connection_string
NODE_ENV=development
FRONTEND_URL=http://localhost:5173
```

### Frontend (.env)
```env
VITE_GOOGLE_CLIENT_ID=your_google_client_id
VITE_API_URL=http://localhost:5000/api-v1
```

## 🗄️ Database Setup

The application uses MongoDB. You can either:
- Use MongoDB Atlas (cloud)
- Set up local MongoDB instance
- Use Docker: `docker run -d -p 27017:27017 --name mongodb mongo:latest`

## 🔐 Google OAuth Setup

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select existing one
3. Enable Google+ API
4. Create OAuth 2.0 credentials
5. Add authorized redirect URIs
6. Copy Client ID and Client Secret to your .env files

## 📱 Usage

1. **Sign Up/Login**: Create an account or use Google OAuth
2. **Add Accounts**: Set up your bank accounts, credit cards, etc.
3. **Create Budgets**: Set monthly spending limits by category
4. **Track Transactions**: Log your income and expenses
5. **Monitor Progress**: View spending patterns and budget status
6. **Analyze Data**: Use charts and reports to understand your finances

## 🏗️ Project Structure

```
Spendly/
├── backend/                 # Backend API server
│   ├── controllers/        # Route controllers
│   ├── database/           # Database schemas
│   ├── middleware/         # Authentication middleware
│   ├── routes/             # API routes
│   └── libs/               # Utility libraries
├── frontend/               # React frontend application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Application pages
│   │   ├── store/          # State management
│   │   └── libs/           # API and utility functions
│   └── public/             # Static assets
└── README.md               # This file
```

## 🧪 Testing

```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
```

## 🚀 Deployment

### Backend (Render/Heroku)
```bash
# Set environment variables in your hosting platform
# Deploy using git push or platform-specific commands
```

### Frontend (Vercel/Netlify)
```bash
# Build the project
npm run build

# Deploy the dist folder
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- React team for the amazing framework
- Tailwind CSS for the utility-first CSS framework
- MongoDB for the flexible database solution
- Google for OAuth authentication

## 📞 Support

If you have any questions or need help:
- Open an issue on GitHub
- Contact: [Your Email]
- Project Link: [https://github.com/Swapnaja7/Spendly](https://github.com/Swapnaja7/Spendly)

---

**Made with ❤️ by Swapnaja**
