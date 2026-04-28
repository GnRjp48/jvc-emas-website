# JVC Emas Website - Quick Start Guide

## What You Have

A complete, professional business website with:
- ✅ Responsive design (works on mobile, tablet, desktop)
- ✅ Green/earth tone corporate theme
- ✅ All required sections (Hero, About, Services, Projects, Contact)
- ✅ WhatsApp integration
- ✅ Contact form
- ✅ Professional images
- ✅ Fast loading and SEO optimized

## File Overview

```
jvc-emas-website/
├── index.html              # Main website file (open this in browser)
├── style.css               # Website styling
├── script.js               # Website functionality
├── README.md               # Full documentation
├── DEPLOYMENT_GUIDE.md     # How to deploy on Netlify
├── QUICK_START.md          # This file
└── images/                 # Website images
    ├── quarry-operations.jpg
    ├── mining-site.jpg
    ├── heavy-equipment.jpg
    ├── equipment-operators.jpg
    └── sand-mining.jpg
```

## Test Locally (Before Deploying)

1. **Open in Browser**
   - Double-click `index.html`
   - Website opens in your default browser
   - Test all links and buttons

2. **Test on Mobile**
   - Open on smartphone/tablet
   - Check responsive design
   - Test contact form and WhatsApp button

3. **Check All Sections**
   - [ ] Navigation works
   - [ ] Hero section displays correctly
   - [ ] Images load properly
   - [ ] Contact form works
   - [ ] WhatsApp button works
   - [ ] Mobile menu works (hamburger)

## Customize Your Website

### 1. Update Contact Information

**In `index.html`, find and replace:**

```html
<!-- Phone -->
<a href="tel:+60123456789">+60 12 345 6789</a>

<!-- Email -->
<a href="mailto:info@jvcemas.com">info@jvcemas.com</a>

<!-- WhatsApp -->
<a href="https://wa.me/60123456789">WhatsApp Us</a>
```

**Replace with your actual:**
- Phone number
- Email address
- WhatsApp number (format: +60123456789)

### 2. Update Company Information

**Find these sections in `index.html`:**

```html
<!-- Hero Section -->
<h2 class="hero-title">Reliable Trading & Mining Solutions Partner</h2>
<p class="hero-subtitle">Your custom subtitle here</p>

<!-- About Section -->
<p>Your company description here...</p>

<!-- Services -->
<h3>Your Service Name</h3>
<p>Your service description...</p>
```

### 3. Replace Images

**Replace these files in the `images/` folder:**
- `quarry-operations.jpg` - Your quarry/mining photo
- `mining-site.jpg` - Your mining operation photo
- `heavy-equipment.jpg` - Your equipment/trading photo
- `equipment-operators.jpg` - Your team/staff photo
- `sand-mining.jpg` - Your sand supply photo

**Keep the same file names!**

### 4. Update Map Location

**Find this in `index.html`:**
```html
<iframe src="https://www.google.com/maps/embed?pb=..."></iframe>
```

**To update:**
1. Go to Google Maps
2. Search for your location
3. Click "Share" → "Embed a map"
4. Copy the new embed code
5. Replace the old one

### 5. Customize Colors (Optional)

**In `style.css`, find and modify:**
```css
:root {
    --primary-color: #2d5016;        /* Main green */
    --secondary-color: #4a7c2c;      /* Lighter green */
    --accent-color: #8b7355;         /* Earth/brown tone */
}
```

**Suggested colors:**
- Green theme (current): #2d5016, #4a7c2c
- Blue theme: #003366, #0066cc
- Orange theme: #cc6600, #ff9933

## Deploy to the Internet

### Option 1: Netlify (Recommended - 5 minutes)

1. **Create GitHub Account**
   - Go to https://github.com
   - Sign up (free)

2. **Upload Files to GitHub**
   - Create new repository: `jvc-emas-website`
   - Upload all files and folders

3. **Deploy on Netlify**
   - Go to https://www.netlify.com
   - Sign up with GitHub
   - Select your repository
   - Click "Deploy"
   - Done! Your website is live

4. **Get Custom Domain (Optional)**
   - Buy domain (GoDaddy, Namecheap, etc.)
   - Connect to Netlify
   - Your website has professional URL

**See DEPLOYMENT_GUIDE.md for detailed instructions**

### Option 2: Other Platforms

- **Vercel**: https://vercel.com (similar to Netlify)
- **GitHub Pages**: Free hosting on GitHub
- **Traditional Hosting**: Upload via FTP to your web host

## Important Customizations Checklist

- [ ] Update phone number
- [ ] Update email address
- [ ] Update WhatsApp number
- [ ] Update company description
- [ ] Update service descriptions
- [ ] Replace all 5 images
- [ ] Update map location
- [ ] Test website locally
- [ ] Deploy to Netlify
- [ ] Test live website
- [ ] Share with team

## Common Customizations

### Change Hero Headline
Find in `index.html`:
```html
<h2 class="hero-title fade-in">Reliable Trading & Mining Solutions Partner</h2>
```

### Add New Service
Copy this block and add to services section:
```html
<div class="service-card fade-in-up">
    <div class="service-image">
        <img src="images/your-image.jpg" alt="Service Name">
    </div>
    <div class="service-content">
        <h3>Your Service Name</h3>
        <p>Your service description...</p>
        <ul class="service-list">
            <li>✓ Feature 1</li>
            <li>✓ Feature 2</li>
        </ul>
    </div>
</div>
```

### Add New Project
Copy this block and add to projects section:
```html
<div class="project-card fade-in-up">
    <div class="project-image">
        <img src="images/your-image.jpg" alt="Project Name">
        <div class="project-overlay">
            <h4>Project Title</h4>
        </div>
    </div>
    <div class="project-info">
        <h4>Project Name</h4>
        <p class="project-category">Category</p>
        <p>Project description...</p>
    </div>
</div>
```

## Troubleshooting

### Images Not Showing
- Check image file names match exactly
- Ensure images are in `images/` folder
- Clear browser cache (Ctrl+Shift+Delete)

### Website Looks Broken
- Make sure all files are in same folder
- Check file names are correct
- Open in different browser
- Clear browser cache

### Contact Form Not Working
- Check WhatsApp number format: +60123456789
- Ensure JavaScript is enabled
- Test on different browser

### Website Not Loading
- Check internet connection
- Verify all files uploaded correctly
- Check Netlify deployment logs

## Need Help?

1. **Netlify Support**: https://www.netlify.com/support
2. **GitHub Help**: https://support.github.com
3. **Web Development**: https://developer.mozilla.org
4. **Contact a Developer**: Hire freelancer on Upwork or Fiverr

## Next Steps

1. ✅ Test website locally
2. ✅ Customize content and images
3. ✅ Deploy on Netlify
4. ✅ Set up custom domain
5. ✅ Share with team
6. ✅ Monitor performance
7. ✅ Update content regularly

---

**Your website is ready to go! Follow the steps above to customize and deploy.**

**Questions? See README.md or DEPLOYMENT_GUIDE.md for more details.**
