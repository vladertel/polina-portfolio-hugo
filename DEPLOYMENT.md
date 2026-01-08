# Hugo Portfolio Deployment Guide

## Site Overview

Your Hugo portfolio site has been successfully built and is ready for deployment.

### Content Summary
- **7 Main Case Studies** (displayed on homepage):
  - Artistro (USA) — Social Growth & Conversion
  - Tremco CPG Europe — HubSpot Email & CRM
  - Mitsubishi Electric — Website Growth + Instagram + PR
  - Artiteq (RUS/NL) — Showroom Launch
  - Ormco / My Ideal Smile — Social + Education Product
  - Valio (RUS) — Product Launch
  - Zeelandia (NL/RU) — Instagram Content System

- **9 Portfolio Assets** (accessible via direct links, not shown on homepage):
  - Instagram Layouts & Posts Design
  - Pinterest Presence
  - Social Media Assets
  - Press-release & Event Support
  - Instagram Launch & Post Examples
  - Showroom Opening
  - Instagram Example Layouts & Reels
  - Banners for Shopify
  - Learning Process Assets

### Site Features
- Responsive design for mobile, tablet, desktop
- Teal color scheme matching brand (#509c6e)
- Search functionality
- Filterable projects by industry, service, category, tags
- Dark/light mode toggle
- Optimized image processing (quality: 85, Lanczos resampling)
- 282 total pages generated

## Building the Site

### Development Build
```bash
cd /Users/Vladislav.Ertel/portfolio/portfolio-hugo
hugo server
```
Site will be available at http://localhost:1313

### Production Build
```bash
cd /Users/Vladislav.Ertel/portfolio/portfolio-hugo
hugo --minify
```
This creates optimized production files in the `public/` folder.

## Deployment Options

### Option 1: Manual Upload (FTP/SFTP)
1. Build the production site: `hugo --minify`
2. Upload the entire `public/` folder contents to your web hosting
3. Point your domain to the hosting directory
4. Ensure SSL certificate is configured

### Option 2: GitHub + Automated Deployment
1. Create a GitHub repository for your portfolio
2. Push your Hugo site to GitHub (excluding `public/` folder)
3. Set up GitHub Actions for automatic builds:
   - On push to main branch, GitHub Actions runs `hugo --minify`
   - Automatically deploys to your hosting via FTP/SFTP
4. Store FTP credentials as GitHub Secrets

### Option 3: Modern Static Hosting
Deploy to platforms that support Hugo:
- **Netlify**: Connect GitHub repo, auto-builds on push
- **Vercel**: Similar to Netlify, one-click deploy
- **Cloudflare Pages**: Fast CDN, automatic HTTPS
- **GitHub Pages**: Free hosting for public repos

## Configuration Before Deployment

### Update Base URL
Edit `hugo.yaml` and change:
```yaml
baseURL: "https://example.org/"  # Replace with your actual domain
```
to:
```yaml
baseURL: "https://yourdomain.com/"  # Your actual domain
```

### Copyright Year
Update footer copyright in `hugo.yaml` if needed.

## File Structure
```
portfolio-hugo/
├── hugo.yaml           # Site configuration
├── content/
│   └── projects/       # 16 projects (7 case studies + 9 assets)
├── static/
│   └── images/         # Profile and cover images
├── themes/
│   └── hugo-profile/   # Theme files
└── public/             # Generated site (upload this folder)
```

## Post-Deployment Checklist
- [ ] Update baseURL in hugo.yaml to actual domain
- [ ] Rebuild site with `hugo --minify`
- [ ] Upload public/ folder to hosting
- [ ] Verify domain DNS settings
- [ ] Test all 7 case study pages load correctly
- [ ] Test mobile responsiveness
- [ ] Verify SSL certificate is active
- [ ] Test search functionality
- [ ] Test contact email link
- [ ] Check LinkedIn profile link works

## Maintenance

### Adding New Case Studies
1. Create new directory: `content/projects/project-name/`
2. Add `index.md` with front matter (use existing case studies as template)
3. Add project images to `content/projects/project-name/images/`
4. Rebuild: `hugo --minify`
5. Deploy updated `public/` folder

### Updating Existing Content
1. Edit the relevant `index.md` file in `content/projects/`
2. Rebuild: `hugo --minify`
3. Deploy updated `public/` folder

### Theme Updates
To update the hugo-profile theme:
```bash
cd themes/hugo-profile
git pull origin master
cd ../..
hugo --minify
```

## Support
- Hugo Documentation: https://gohugo.io/documentation/
- Theme Documentation: https://github.com/gurusabarish/hugo-profile
- Issue Reporting: https://github.com/gurusabarish/hugo-profile/issues

## Build Performance
- Build time: ~150ms
- Pages generated: 282
- Static files: 2051
- Processed images: Optimized with Lanczos resampling at 85% quality
