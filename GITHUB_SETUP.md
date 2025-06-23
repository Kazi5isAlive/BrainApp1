# GitHub Setup and Hosting Guide

## Setting Up on GitHub

### 1. Create GitHub Repository
1. Go to [GitHub.com](https://github.com) and create a new repository
2. Name it `audio-frequency-tuner` (or your preferred name)
3. Set it to **Public** for free hosting options
4. Don't initialize with README (we have our own)

### 2. Upload Your Code
**Option A: GitHub Web Interface**
1. Download the project files from Replit
2. Drag and drop all files to the new GitHub repository
3. Commit with message: "Initial commit - Audio Frequency Tuner"

**Option B: Git Commands (if you have Git installed)**
```bash
git init
git add .
git commit -m "Initial commit - Audio Frequency Tuner"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/audio-frequency-tuner.git
git push -u origin main
```

## Hosting Options

### Option 1: Vercel (Recommended - Free)
1. Go to [vercel.com](https://vercel.com)
2. Sign up with your GitHub account
3. Click "New Project" and select your repository
4. Vercel will auto-detect the settings
5. Deploy automatically on every GitHub push

**Configuration for Vercel:**
- Build Command: `npm run build`
- Output Directory: `dist/public`
- Install Command: `npm install`

### Option 2: Netlify (Free)
1. Go to [netlify.com](https://netlify.com)
2. Connect your GitHub account
3. Select your repository
4. Build settings:
   - Build command: `npm run build`
   - Publish directory: `dist/public`

### Option 3: GitHub Pages (Free - Static only)
**Note:** GitHub Pages only hosts static sites, so the backend won't work. You'd need to modify the app for frontend-only use.

1. Go to repository Settings > Pages
2. Choose "GitHub Actions" as source
3. Create workflow file (see below)

### Option 4: Railway/Render (Free tier available)
Both support full-stack applications with backend servers.

## Environment Variables for Production

For any hosting platform, you'll need to set:
- `NODE_ENV=production`
- `SESSION_SECRET=your-secure-random-string`

Generate a secure session secret:
```bash
node -e "console.log(require('crypto').randomBytes(32).toString('base64'))"
```

## GitHub Actions Workflow (Optional)

Create `.github/workflows/deploy.yml` for automated deployment:
```yaml
name: Deploy
on:
  push:
    branches: [ main ]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - uses: actions/setup-node@v3
      with:
        node-version: '18'
    - run: npm install
    - run: npm run build
    - name: Deploy to hosting
      # Add your hosting provider's deployment action here
```

## Benefits of GitHub + Hosting

✓ **Free hosting** for personal projects
✓ **Automatic deployments** on code changes
✓ **Custom domain** support (most platforms)
✓ **SSL certificates** included
✓ **Version control** and collaboration
✓ **Issue tracking** and project management

## Repository Structure
Your GitHub repo will contain:
- All source code
- README.md with setup instructions
- Package.json with dependencies
- Build configuration files
- This setup guide