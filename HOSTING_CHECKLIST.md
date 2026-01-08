# Hosting Deployment Checklist

## ✅ Site Ready for Deployment

Your Hugo portfolio site has been built and is ready to deploy!

### Production Build Complete
- **Location:** `/Users/Vladislav.Ertel/portfolio/portfolio-hugo/public/`
- **Build status:** Optimized with `hugo --minify`
- **Pages generated:** 282
- **All images:** Included and optimized

---

## 🚀 Deployment Steps

### Step 1: Update Domain (IMPORTANT!)

Before uploading, update the `baseURL` in `hugo.yaml`:

```bash
# Edit hugo.yaml line 1:
baseURL: "https://your-actual-domain.com/"

# Then rebuild:
hugo --minify
```

### Step 2: Upload to Your Hosting

**Option A: FTP/SFTP Upload**
1. Connect to your hosting via FTP client (FileZilla, Cyberduck, etc.)
2. Navigate to your web root directory (usually `public_html/` or `www/`)
3. Upload **everything inside** the `public/` folder:
   ```
   /Users/Vladislav.Ertel/portfolio/portfolio-hugo/public/*
   ```
4. Your site should be live at your domain!

**Option B: Command Line (if you have SSH access)**
```bash
# Replace with your actual hosting details
rsync -avz --delete public/ username@yourhost.com:/path/to/web/root/
```

**Option C: Modern Static Hosting**
- **Netlify:** Drag & drop the `public/` folder
- **Vercel:** Connect GitHub repo (you'll need to push first)
- **Cloudflare Pages:** Connect GitHub repo

---

## 📋 Pre-Launch Checklist

Before making your site live, verify:

- [ ] Updated `baseURL` in `hugo.yaml` to your actual domain
- [ ] Rebuilt site with `hugo --minify` after domain update
- [ ] Tested locally with `hugo server`
- [ ] All 7 case studies display correctly
- [ ] All gallery images load properly
- [ ] Contact email link works (paulina.d.ertel@gmail.com)
- [ ] LinkedIn link works
- [ ] Mobile responsiveness looks good
- [ ] SSL certificate is active on hosting (HTTPS)

---

## 📁 What Gets Uploaded

The `public/` folder contains:
- `index.html` - Your homepage
- `projects/` - All 7 case study pages with images
- `css/`, `js/`, `images/` - Optimized assets
- All necessary HTML, CSS, JS files

**Total size:** ~15-20 MB

---

## 🔄 Updating Your Site Later

When you want to update content:

1. Edit markdown files in `content/projects/`
2. Rebuild: `hugo --minify`
3. Re-upload the `public/` folder to your hosting

---

## ✅ Post-Launch Verification

After uploading, test:
- Visit `https://your-domain.com/`
- Click through all 7 case studies
- Verify all images load
- Test on mobile device
- Check contact links work

---

## 📊 Your Portfolio

**7 Case Studies with Galleries:**
1. Artistro (USA) - 8 images
2. Artiteq (RUS/NL) - 7 images
3. Mitsubishi Electric - 8 images
4. Ormco / My Ideal Smile - 8 images
5. Tremco CPG Europe - No gallery
6. Valio (RUS) - No gallery
7. Zeelandia (NL/RU) - No gallery

**Homepage Features:**
- Professional bio with profile photo
- Core strengths listed
- Selected results/metrics
- Education & certificates
- All case studies displayed as cards
- Contact section with email and LinkedIn

---

## 🆘 Need Help?

- **Hugo Documentation:** https://gohugo.io/documentation/
- **Theme Issues:** https://github.com/gurusabarish/hugo-profile
- **Rebuild Site:** `hugo --minify`
- **Test Locally:** `hugo server`

---

**Your site is production-ready in the `public/` folder!**

Just update the domain, rebuild, and upload. 🎉
