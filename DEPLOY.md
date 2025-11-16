# Vercel Deployment Guide

## Deploy to Vercel (No Installation Required)

### Method 1: Deploy from GitHub (Easiest)

1. **Push your code to GitHub:**
   ```powershell
   git add .
   git commit -m "Prepare for Vercel deployment"
   git push
   ```

2. **Go to Vercel:**
   - Visit https://vercel.com
   - Click "Sign Up" and choose "Continue with GitHub"
   - Authorize Vercel to access your repositories

3. **Import your repository:**
   - Click "New Project"
   - Select your `junction_app` repository
   - Click "Import"
   - Vercel will auto-detect settings
   - Click "Deploy"

4. **Your app will be live at:**
   - `https://junction-app-[random].vercel.app`

### Method 2: Install Vercel CLI (If you install Node.js later)

1. **Install Node.js from:** https://nodejs.org
2. **Then run:**
   ```powershell
   npm install -g vercel
   vercel login
   vercel
   ```

### Files Ready for Deployment:
- ✅ `vercel.json` - Vercel configuration
- ✅ `requirements.txt` - Python dependencies
- ✅ `app.py` - Updated with Vercel export
- ✅ `Procfile` - Process file (backup)

### After Deployment:
Your Flask app will be available at a public URL like:
`https://junction-app.vercel.app`

### Troubleshooting:
- If build fails, check the build logs in Vercel dashboard
- Ensure all dependencies are in `requirements.txt`
- Static files go in `public/` or `static/`
