# 🚀 SETUP GUIDE - Get Started in 5 Minutes

## Step 1: Install Dependencies

### Backend
```bash
cd backend
npm install
```

### Frontend
```bash
cd frontend
npm install
```

## Step 2: Create Environment Files

### Backend
```bash
cd backend
cp .env.example .env
```

Edit `backend/.env` and add:
- Your MongoDB Atlas connection string (MONGO_URI)
- Gmail credentials (MAIL_USER, MAIL_PASS)
- JWT secret

### Frontend
```bash
cd frontend
cp .env.example .env
```

Edit `frontend/.env`:
```
VITE_API_URL=http://localhost:5000/api
```

## Step 3: Start Development Servers

### Terminal 1 - Backend
```bash
cd backend
npm run dev
```

Should show:
```
✅ MongoDB connected
🚀 Server running on port 5000
```

### Terminal 2 - Frontend
```bash
cd frontend
npm run dev
```

Should show:
```
VITE v5.0.0  ready in xxx ms
➜  Local:   http://localhost:5173/
```

## Step 4: Test the Application

1. Open: `http://localhost:5173`
2. Click **Sign Up**
3. Enter: Name, Email, Password
4. Click **Send Verification OTP**
5. Check your email for OTP
6. Enter OTP and verify
7. Login with your credentials
8. Create a test note
9. Done! ✅

## Getting MongoDB Connection String

1. Go to [mongodb.com](https://mongodb.com)
2. Create free account
3. Create database (M0 tier - free)
4. Click **Connect**
5. Select **Drivers**
6. Copy connection string
7. Replace `<password>` with your actual password

## Getting Gmail App Password

1. Go to [myaccount.google.com](https://myaccount.google.com)
2. Enable **2-Step Verification** (if not enabled)
3. Go to **App Passwords**
4. Select **Mail** and **Windows/Linux/Mac**
5. Click **Generate**
6. Copy the 16-character password

## Common Issues

### Port Already in Use
```bash
# Kill process on port 5000
lsof -ti:5000 | xargs kill -9
```

### MongoDB Connection Error
- Verify connection string format
- Check MongoDB Atlas network access
- Verify username/password

### CORS Error
- Make sure backend is running
- Check frontend API URL in .env
- Restart both servers

## Next: Deployment

Once everything works locally, deploy to production:
- Read: `DEPLOYMENT_DOCS/COMPLETE_DEPLOYMENT_GUIDE.md`
- Takes about 30 minutes
- Your app will be live!

---

**Having issues?** Check `DEPLOYMENT_DOCS/COMPREHENSIVE_TROUBLESHOOTING.md`
