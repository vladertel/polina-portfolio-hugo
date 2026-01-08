# GitHub Pages Deployment Guide for polina.ertel.one

Your site is configured to deploy to **https://polina.ertel.one/** using GitHub Pages for free!

## 🚀 Setup Steps

### 1. Create GitHub Repository

```bash
# Option A: Create via GitHub CLI (if installed)
gh repo create portfolio-hugo --public --source=. --remote=origin

# Option B: Create via GitHub website
# Go to https://github.com/new
# Create a new public repository named "portfolio-hugo"
```

### 2. Push Your Code to GitHub

```bash
# Add GitHub remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/portfolio-hugo.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under "Build and deployment":
   - **Source:** Select "GitHub Actions"
4. The site will automatically build and deploy!

### 4. Configure DNS for ertel.one Domain

You need to add a CNAME record to point `polina.ertel.one` to GitHub Pages:

**DNS Settings at your domain registrar (where you manage ertel.one):**

| Type  | Name/Host | Value/Target              | TTL  |
|-------|-----------|---------------------------|------|
| CNAME | polina    | YOUR_USERNAME.github.io.  | 3600 |

**Replace `YOUR_USERNAME` with your actual GitHub username!**

Example:
- If your GitHub username is `polinaertel`
- CNAME record: `polina` → `polinaertel.github.io.`

### 5. Enable HTTPS (After DNS Propagates)

After DNS propagates (can take 24-48 hours):

1. Go to repository **Settings** → **Pages**
2. Under "Custom domain", you should see: `polina.ertel.one` ✓
3. Check **Enforce HTTPS**

## ✅ What Happens Next

1. **Push to GitHub** → GitHub Actions automatically builds your site
2. **DNS configured** → `polina.ertel.one` points to your GitHub Pages site
3. **Free HTTPS** → GitHub provides SSL certificate automatically
4. **Auto-deploy** → Every push to `main` branch updates your live site

## 🔄 How to Update Your Site

```bash
# 1. Make changes to your content
vim content/projects/some-project/index.md

# 2. Test locally
hugo server

# 3. Commit and push
git add .
git commit -m "Update project content"
git push

# 4. GitHub Actions automatically rebuilds and deploys!
# Check progress at: https://github.com/YOUR_USERNAME/portfolio-hugo/actions
```

## 📊 Deployment Status

Your site will be live at:
- **Primary URL:** https://polina.ertel.one/
- **GitHub Pages URL:** https://YOUR_USERNAME.github.io/portfolio-hugo/

## 🐛 Troubleshooting

### DNS not working?
- Wait 24-48 hours for DNS propagation
- Check DNS with: `dig polina.ertel.one`
- Verify CNAME points to `YOUR_USERNAME.github.io.`

### Build failing?
- Check GitHub Actions tab for errors
- Ensure `hugo.yaml` baseURL is correct: `https://polina.ertel.one/`

### HTTPS not available?
- DNS must propagate first
- GitHub needs to provision SSL certificate (automatic, takes ~1 hour)

## 💰 Cost

**Completely FREE!** GitHub Pages includes:
- ✓ Free hosting
- ✓ Free SSL certificate
- ✓ Free custom domain support
- ✓ Free automatic builds
- ✓ 1GB storage limit (your site is ~45MB, plenty of room)
- ✓ 100GB bandwidth/month (more than enough)

## 📝 Files Added

- `.github/workflows/deploy.yml` - GitHub Actions workflow for auto-deploy
- `static/CNAME` - Custom domain configuration
- `hugo.yaml` - Updated baseURL to `https://polina.ertel.one/`

## 🔐 Repository Visibility

Your repository should be **PUBLIC** for free GitHub Pages hosting. If you need a private repo, you'll need GitHub Pro ($4/month).

---

**Next Step:** Push to GitHub and configure DNS! 🚀
