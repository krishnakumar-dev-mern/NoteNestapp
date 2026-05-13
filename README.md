# 📝 NoteNest - Full Stack Notes Application

A modern, full-stack notes application built with React, Express.js, and MongoDB.

## ✨ Features

- ✅ User Authentication with JWT
- ✅ Email-based OTP Verification
- ✅ Create, Read, Update, Delete Notes
- ✅ Password Reset with OTP
- ✅ Responsive UI with Tailwind CSS
- ✅ Secure API with CORS

## 🏗️ Project Structure

```
NoteNest/
├── backend/                 # Node.js/Express API
│   ├── controllers/        # Route handlers
│   ├── models/             # MongoDB schemas
│   ├── routes/             # API endpoints
│   ├── middleware/         # Auth & validation
│   ├── utils/              # Email service
│   ├── server.js           # Express app
│   ├── package.json        # Dependencies
│   └── .env.example        # Env template
│
├── frontend/               # React/Vite app
│   ├── src/
│   │   ├── pages/         # Page components
│   │   ├── components/    # Reusable components
│   │   ├── lib/           # Axios config
│   │   ├── context/       # Auth context
│   │   └── App.jsx        # Main component
│   ├── public/            # Static assets
│   ├── package.json       # Dependencies
│   └── .env.example       # Env template
│
└── DEPLOYMENT_DOCS/        # Complete guides
    ├── 00_READ_ME_FIRST.txt
    ├── COMPLETE_DEPLOYMENT_GUIDE.md
    ├── RENDER_DEPLOYMENT_GUIDE.md
    ├── NETLIFY_DEPLOYMENT_GUIDE.md
    └── ... (more guides)
```

## 🚀 Quick Start (Local Development)

### Prerequisites
- Node.js >= 18.0.0
- MongoDB (local or MongoDB Atlas)
- npm or yarn

### Backend Setup

```bash
cd backend
cp .env.example .env
# Edit .env with your values
npm install
npm run dev
```

Backend runs on: `http://localhost:5000`

### Frontend Setup

```bash
cd frontend
cp .env.example .env
# Edit .env with backend URL
npm install
npm run dev
```

Frontend runs on: `http://localhost:5173`

## 📋 Environment Variables

### Backend (.env)
```
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USER=your_email@gmail.com
MAIL_PASS=your_app_password
MAIL_FROM=noreply@youremail.com
NODE_ENV=development
```

### Frontend (.env)
```
VITE_API_URL=http://localhost:5000/api
```

## 🌐 API Endpoints

### Auth
- `POST /api/auth/register` - Create account
- `POST /api/auth/verify-otp` - Verify email
- `POST /api/auth/resend-otp` - Resend OTP
- `POST /api/auth/login` - Login
- `POST /api/auth/forgot-password` - Reset password
- `POST /api/auth/verify-reset-otp` - Verify reset OTP
- `POST /api/auth/reset-password` - Set new password
- `GET /api/auth/me` - Get current user

### Notes
- `GET /api/items` - Get all notes
- `POST /api/items` - Create note
- `GET /api/items/:id` - Get note
- `PUT /api/items/:id` - Update note
- `DELETE /api/items/:id` - Delete note

### Health
- `GET /api/health` - Health check

## 📦 Production Deployment

### Using Render (Backend) + Netlify (Frontend)

1. **Read the guides:**
   - Open `DEPLOYMENT_DOCS/00_READ_ME_FIRST.txt`
   - Follow `DEPLOYMENT_DOCS/COMPLETE_DEPLOYMENT_GUIDE.md`

2. **Quick overview:**
   - Push code to GitHub
   - Deploy backend to Render
   - Deploy frontend to Netlify
   - Set environment variables on each platform

3. **Time required:** ~30-40 minutes

## 🔐 Security Features

- ✅ JWT Authentication
- ✅ CORS Protection
- ✅ Password Hashing (bcryptjs)
- ✅ OTP Email Verification
- ✅ Environment Variables for Secrets
- ✅ Input Validation

## 🛠️ Tech Stack

### Backend
- Express.js (Web framework)
- MongoDB (Database)
- Mongoose (ODM)
- JWT (Authentication)
- bcryptjs (Password hashing)
- Nodemailer (Email service)
- CORS (Cross-origin requests)

### Frontend
- React (UI framework)
- Vite (Build tool)
- Tailwind CSS (Styling)
- Axios (HTTP client)
- React Router (Navigation)
- React Hot Toast (Notifications)

## 📝 File Checklist Before Deployment

- [ ] `backend/server.js` - Fixed CORS configuration
- [ ] `backend/package.json` - All dependencies listed
- [ ] `backend/.env.example` - Template created
- [ ] `frontend/.env.example` - Template created
- [ ] `frontend/public/_redirects` - Netlify routing file
- [ ] `.gitignore` - Excludes sensitive files
- [ ] All code pushed to GitHub

## ✅ Testing Checklist

- [ ] Backend health check works
- [ ] Frontend loads without errors
- [ ] Can signup with email verification
- [ ] Can receive OTP emails
- [ ] Can login with credentials
- [ ] Can create notes
- [ ] Can edit notes
- [ ] Can delete notes
- [ ] Can logout

## 🆘 Troubleshooting

**CORS Error?**
- Check `CLIENT_URL` env var on Render backend
- Make sure it matches your frontend URL exactly
- Restart backend after changing env var

**OTP not received?**
- Verify Gmail app password (16 chars)
- Check 2FA is enabled on Gmail
- Check spam folder
- Check Render logs for errors

**Cannot connect to MongoDB?**
- Verify connection string in `MONGO_URI`
- Check MongoDB Atlas network access allows your IP
- Verify username and password

**See more troubleshooting:** `DEPLOYMENT_DOCS/COMPREHENSIVE_TROUBLESHOOTING.md`

## 📚 Documentation

All deployment guides are in `DEPLOYMENT_DOCS/`:

1. `00_READ_ME_FIRST.txt` - Start here
2. `COMPLETE_DEPLOYMENT_GUIDE.md` - Main deployment guide
3. `RENDER_DEPLOYMENT_GUIDE.md` - Backend deployment details
4. `NETLIFY_DEPLOYMENT_GUIDE.md` - Frontend deployment details
5. `QUICK_REFERENCE_CARD.md` - Quick lookup guide
6. `COMPREHENSIVE_TROUBLESHOOTING.md` - Solutions to 10+ issues

## 🚀 Next Steps

1. Read: `DEPLOYMENT_DOCS/00_READ_ME_FIRST.txt`
2. Follow: `DEPLOYMENT_DOCS/COMPLETE_DEPLOYMENT_GUIDE.md`
3. Deploy to production
4. Share your app with the world!

## 📄 License

MIT License - Feel free to use this project for learning and building.

## 👨‍💻 Author

Created as a full-stack learning project.

---

**Ready to deploy?** Open `DEPLOYMENT_DOCS/00_READ_ME_FIRST.txt` 🚀
