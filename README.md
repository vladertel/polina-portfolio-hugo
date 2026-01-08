# Polina Ertel - Digital Marketing Portfolio

A professional Hugo-powered portfolio website showcasing digital marketing case studies and expertise.

## 🎯 Features

- **7 Case Studies** - Comprehensive project showcases with results and metrics
- **Responsive Design** - Mobile-first, works perfectly on all devices
- **Teal Brand Colors** - Custom color scheme matching your brand
- **Fast & Secure** - Static site = lightning-fast loads and maximum security
- **SEO Optimized** - Built-in best practices for search engines
- **Easy to Update** - Simple markdown files for content
- **Filterable Projects** - Organize by industry, service, and category

## 📁 Project Structure

```
portfolio-hugo/
├── content/
│   └── projects/           # Case study markdown files
│       ├── artistro-usa/
│       ├── tremco-cpg-europe/
│       ├── mitsubishi-electric/
│       ├── artiteq/
│       ├── ormco-my-ideal-smile/
│       ├── valio/
│       └── zeelandia/
├── static/
│   └── images/             # Profile and static images
├── themes/
│   └── hugo-profile/       # Portfolio theme
├── public/                 # Generated site (deploy this!)
├── hugo.yaml               # Site configuration
├── DEPLOYMENT.md           # Detailed deployment guide
└── README.md               # This file
```

## 🚀 Quick Start

### Preview Locally

```bash
cd /Users/Vladislav.Ertel/portfolio/portfolio-hugo
hugo server -D
```

Open: http://localhost:1313/

### Build for Production

```bash
hugo --minify
```

This creates the `public/` folder ready for deployment.

## 📤 Deployment

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment instructions including:
- FTP/SFTP upload
- rsync deployment
- Automated GitHub Actions deployment

**Quick deploy**: Upload everything in the `public/` folder to your web hosting.

## ✏️ Updating Content

### Add a New Case Study

1. Create directory:
   ```bash
   mkdir -p content/projects/client-name/images
   ```

2. Create `index.md` with front matter:
   ```yaml
   ---
   title: "Client Name — Project Description"
   date: 2024-01-01
   industries: ["Industry 1", "Industry 2"]
   services: ["Service 1", "Service 2"]
   categories: ["Category"]
   tags: ["tag1", "tag2"]
   description: "Short description"
   image: images/cover.png
   ---
   ```

3. Add your content in markdown

4. Add images to `images/` folder

5. Rebuild: `hugo --minify`

### Update Existing Content

1. Edit the markdown file: `content/projects/[project-name]/index.md`
2. Rebuild: `hugo --minify`
3. Re-deploy the `public/` folder

### Change Site Settings

Edit `hugo.yaml` to modify:
- Site title and description
- Contact information
- Colors and branding
- Navigation menu
- Social links

## 🎨 Customization

### Colors

The site uses a teal color scheme. To change colors, edit `hugo.yaml`:

```yaml
params:
  color:
    primaryColor: "#509c6e"  # Teal
    secondaryBackgroundColor: "#e8f5f0"  # Light teal
```

### Profile Image

Replace: `static/images/profile.jpg`

### Adding More Sections

The theme supports:
- Projects/Case Studies (enabled)
- Blog posts (can be enabled)
- Experience timeline (can be enabled)
- Skills section (enabled)
- Achievements (enabled)

## 📊 Case Studies Included

1. **Artistro (USA)** - Social Growth & Conversion (+80K followers, +48% orders)
2. **Tremco CPG Europe** - HubSpot Email & CRM (+28% repeat sales)
3. **Mitsubishi Electric** - Digital + PR (+45% traffic, 30+ publications)
4. **Artiteq** - Showroom Launch (60+ new clients)
5. **Ormco / My Ideal Smile** - Social + Education (+4,000 followers)
6. **Valio** - Product Launch (Complete content package)
7. **Zeelandia** - Instagram Content System (+1,000 followers, +15% inquiries)

## 🛠️ Technology Stack

- **Hugo** v0.125.3 (Static Site Generator)
- **hugo-profile** theme (Free, open-source)
- **Bootstrap 5** (Responsive framework)
- **Font Awesome** (Icons)
- **Markdown** (Content format)

## ⚡ Performance

- **Build time**: ~186ms
- **210 pages** generated
- **Static HTML** - instant page loads
- **Minified assets** - optimized for speed
- **No database** - maximum security

## 🔧 Requirements

- Hugo v0.125.3+ (Extended version)
- Git (for version control)
- Web hosting with static file support

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🆘 Support

- **Hugo Docs**: https://gohugo.io/documentation/
- **Theme GitHub**: https://github.com/gurusabarish/hugo-profile
- **Hugo Forum**: https://discourse.gohugo.io/

## 📝 To-Do (Optional Enhancements)

- [ ] Add more case study images from Notion exports
- [ ] Create portfolio assets pages (Instagram layouts, Pinterest, etc.)
- [ ] Add blog section for marketing insights
- [ ] Implement contact form
- [ ] Add Google Analytics
- [ ] Set up automated GitHub Actions deployment

## 📄 License

This portfolio site is for Polina Ertel. The hugo-profile theme is MIT licensed.

---

**Built with Hugo** • **Designed for Performance** • **Ready to Deploy**

For deployment instructions, see [DEPLOYMENT.md](DEPLOYMENT.md)
