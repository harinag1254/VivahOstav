# VivahOstav Deployment Guide

## Option 1: Deploy to Vercel (Recommended)

### Quick Deploy (One-Click)
Click the button below to deploy VivahOstav to Vercel with a single click:

```
[Deploy to Vercel]
https://vercel.com/new/clone?repository-url=https://github.com/yourusername/vivahostav
```

### Manual Vercel Deploy

1. **Install Vercel CLI:**
   ```bash
   npm install -g vercel
   ```

2. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/vivahostav.git
   cd vivahostav
   ```

3. **Deploy:**
   ```bash
   vercel
   ```

4. **Follow the prompts:**
   - Select your team (or create a new one)
   - Link to your GitHub account (optional but recommended)
   - Confirm project settings
   - Your live URL will appear: `https://vivahostav.vercel.app`

---

## Option 2: Create GitHub Repository & Deploy

### Step 1: Create Repository on GitHub

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `vivahostav`
3. Description: `VivahOstav — Wedding Operating System`
4. Set to **Public** (so others can see & fork your work)
5. Click **Create repository**

### Step 2: Initialize Local Git Repository

```bash
# Navigate to your project
cd /path/to/vivahostav

# Initialize git
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: VivahOstav v1.0 — wedding planning OS"

# Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/vivahostav.git

# Set branch to main
git branch -M main

# Push to GitHub
git push -u origin main
```

### Step 3: Deploy from GitHub to Vercel

1. Go to [vercel.com/new](https://vercel.com/new)
2. Click **Import Git Repository**
3. Paste your GitHub repo URL: `https://github.com/YOUR_USERNAME/vivahostav.git`
4. Click **Continue**
5. Vercel will auto-detect settings (static site)
6. Click **Deploy**
7. Wait for the deployment to complete (~30 seconds)
8. You'll get a live URL: `https://vivahostav.vercel.app`

### Step 4: Enable Auto-Deployments (Optional)

Once linked to GitHub, every push to `main` will auto-deploy:

```bash
# Make changes locally
nano vivahostav.html  # or use your editor

# Commit and push
git add .
git commit -m "Update: improved layout"
git push

# Vercel automatically deploys! ✨
```

---

## Option 3: Deploy to GitHub Pages

### Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/vivahostav.git
git branch -M main
git push -u origin main
```

### Enable GitHub Pages

1. Go to your GitHub repo → **Settings** → **Pages**
2. Under "Source," select **main** branch
3. Click **Save**
4. Your site will be live at: `https://YOUR_USERNAME.github.io/vivahostav`

---

## Option 4: Deploy to Netlify

1. Go to [netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop `vivahostav.html`
3. Wait for deployment (~10 seconds)
4. Get a shareable live URL instantly

---

## Verification Checklist

After deployment, verify:

- ✅ The app loads without errors
- ✅ Click through onboarding flow
- ✅ Add a guest, vendor, task
- ✅ Create an invitation
- ✅ Test RSVP and tracking
- ✅ Open on mobile (should be responsive)
- ✅ Hard refresh (Ctrl+Shift+R / Cmd+Shift+R) to test data persistence

---

## Continuous Updates

### After Deployment
To make updates and re-deploy:

```bash
# Make changes
# ... edit vivahostav.html, README, etc.

# Commit changes
git add .
git commit -m "Feature: added [feature]"

# Push to GitHub
git push origin main

# Vercel auto-deploys! (if linked)
# Or manually deploy: vercel --prod
```

---

## Troubleshooting

### "Failed to deploy to Vercel"
- Make sure you have a Vercel account
- Check that the file paths are correct
- Try: `vercel --prod` for a production deployment

### "GitHub Pages isn't working"
- Verify **Settings → Pages** shows "Published at: https://..."
- Wait 1-2 minutes for GitHub to process
- Check that `main` branch is selected

### "App loads but data doesn't persist"
- Open DevTools (F12) → Console
- Check for localStorage errors
- Try refreshing (Ctrl+R)
- Clear browser cache and try again

### "AI features not working"
- Verify you have an Anthropic API key (if self-hosting)
- Check browser console for CORS errors
- AI features require the Vercel proxy to work correctly

---

## Hosting Platform Comparison

| Platform | Setup | Cost | Auto-Deploy | Custom Domain | Best For |
|----------|-------|------|-------------|---------------|----------|
| Vercel | 2 min | Free tier | ✅ | ✅ | Production, SPA |
| GitHub Pages | 3 min | Free | ✅ | ✅ | Portfolio, static |
| Netlify | 1 min | Free tier | ✅ | ✅ | Quick launch |
| AWS S3 | 10 min | Pay-per-use | ❌ | ✅ | Enterprise |

**Recommendation:** Start with Vercel (fastest, best DX, free tier). GitHub Pages if you prefer GitHub-only workflow.

---

## Next Steps

1. Choose your platform (Vercel recommended)
2. Deploy using instructions above
3. Share the live link with friends & family
4. Gather feedback and iterate

**Need help?**
- Vercel docs: https://vercel.com/docs
- GitHub Pages: https://pages.github.com
- Report issues: Open a GitHub issue

---

**Happy planning! 🎉**
