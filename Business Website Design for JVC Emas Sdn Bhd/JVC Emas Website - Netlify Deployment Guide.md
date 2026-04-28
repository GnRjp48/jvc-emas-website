# JVC Emas Website - Netlify Deployment Guide

## Quick Start (5 Minutes)

### Prerequisites
- GitHub account (free at https://github.com)
- Netlify account (free at https://www.netlify.com)
- Your website files

---

## Step-by-Step Deployment

### Step 1: Create a GitHub Repository

1. **Go to GitHub**
   - Visit https://github.com and sign in
   - Click the "+" icon in the top right
   - Select "New repository"

2. **Create Repository**
   - Repository name: `jvc-emas-website`
   - Description: "Professional business website for JVC Emas Sdn. Bhd."
   - Choose "Public" (for easier deployment)
   - Click "Create repository"

3. **Upload Files**
   - Click "uploading an existing file"
   - Drag and drop all website files:
     - `index.html`
     - `style.css`
     - `script.js`
     - `README.md`
     - `DEPLOYMENT_GUIDE.md`
     - `images/` folder with all images
   - Click "Commit changes"

### Step 2: Deploy on Netlify

1. **Sign Up for Netlify**
   - Go to https://www.netlify.com
   - Click "Sign up"
   - Choose "Sign up with GitHub"
   - Authorize Netlify to access your GitHub account

2. **Create New Site**
   - In Netlify dashboard, click "Add new site"
   - Select "Import an existing project"
   - Choose "GitHub" as your Git provider
   - Authorize if prompted
   - Select your `jvc-emas-website` repository

3. **Configure Build Settings**
   - **Base directory**: Leave empty (or set to `.`)
   - **Build command**: Leave empty (no build needed)
   - **Publish directory**: Leave empty (or set to `.`)
   - Click "Deploy site"

4. **Wait for Deployment**
   - Netlify will automatically build and deploy
   - You'll see a URL like: `https://random-name-12345.netlify.app`
   - Your website is now live!

### Step 3: Set Up Custom Domain (Optional)

1. **Purchase Domain**
   - Buy a domain from registrars like:
     - GoDaddy (https://www.godaddy.com)
     - Namecheap (https://www.namecheap.com)
     - Domain.com (https://www.domain.com)
   - Recommended: `jvcemas.com` or `jvcemas.my`

2. **Connect Domain to Netlify**
   - In Netlify dashboard, go to "Site settings"
   - Click "Domain management"
   - Click "Add custom domain"
   - Enter your domain name (e.g., `jvcemas.com`)
   - Click "Verify"

3. **Update DNS Settings**
   - Netlify will provide DNS records
   - Log in to your domain registrar
   - Update DNS records as instructed
   - Wait 24-48 hours for DNS to propagate
   - Your domain will point to your Netlify site

### Step 4: SSL Certificate (HTTPS)

1. **Automatic HTTPS**
   - Netlify automatically provides free SSL certificate
   - Your site is secure: `https://jvcemas.com`
   - No additional action needed

2. **Verify HTTPS**
   - Visit your website
   - Look for the green lock icon in browser
   - You're secure!

---

## Making Updates

### Update Website Content

1. **Edit Files Locally**
   - Edit `index.html`, `style.css`, or `script.js` on your computer
   - Save changes

2. **Upload to GitHub**
   - Go to your GitHub repository
   - Click "Add file" → "Upload files"
   - Select your updated files
   - Click "Commit changes"

3. **Automatic Deployment**
   - Netlify automatically detects changes
   - Website updates within seconds
   - No manual deployment needed!

### Update Images

1. **Replace Images**
   - Go to GitHub repository
   - Navigate to `images/` folder
   - Click each image file
   - Click "Delete" to remove
   - Upload new images with same names

2. **Automatic Update**
   - Netlify rebuilds and deploys
   - Updated images appear on website

---

## Troubleshooting

### Issue: Site shows "Page not found"

**Solution:**
1. Check that `index.html` is in the root directory (not in a subfolder)
2. Verify all files were uploaded to GitHub
3. Check Netlify deployment logs:
   - Go to "Deploys" tab
   - Look for error messages
   - Fix issues and re-upload

### Issue: Images not showing

**Solution:**
1. Verify images are in the `images/` folder
2. Check image file names match exactly in HTML
3. Ensure images were uploaded to GitHub
4. Clear browser cache (Ctrl+Shift+Delete)

### Issue: Styles not applying

**Solution:**
1. Verify `style.css` is in root directory
2. Check file is linked correctly in `index.html`
3. Clear browser cache
4. Hard refresh (Ctrl+Shift+R)

### Issue: JavaScript not working

**Solution:**
1. Verify `script.js` is in root directory
2. Check browser console for errors (F12)
3. Ensure script is linked in `index.html`
4. Test on different browser

### Issue: Form not submitting

**Solution:**
1. Verify WhatsApp number is correct format: `+60123456789`
2. Check browser console for JavaScript errors
3. Test on different browser
4. Ensure JavaScript is enabled

### Issue: Domain not connecting

**Solution:**
1. Wait 24-48 hours for DNS propagation
2. Verify DNS records are correct in domain registrar
3. Use DNS checker: https://www.whatsmydns.net
4. Contact domain registrar support if issues persist

---

## Performance Optimization

### Enable Caching
1. In Netlify dashboard, go to "Site settings"
2. Click "Build & deploy" → "Post processing"
3. Enable "Asset optimization"
4. Enable "Minify CSS" and "Minify JavaScript"

### Monitor Performance
1. Use Google PageSpeed Insights: https://pagespeed.web.dev
2. Enter your website URL
3. Get performance recommendations
4. Implement suggested improvements

### Analytics
1. In Netlify dashboard, go to "Analytics"
2. Enable "Netlify Analytics" (optional, paid feature)
3. Or integrate Google Analytics:
   - Get tracking code from Google Analytics
   - Add to `<head>` section of `index.html`

---

## Security Best Practices

### Enable Security Headers
1. Go to "Site settings" → "Build & deploy"
2. Add custom headers in `netlify.toml`:

```toml
[[headers]]
  for = "/*"
  [headers.values]
    X-Frame-Options = "DENY"
    X-Content-Type-Options = "nosniff"
    X-XSS-Protection = "1; mode=block"
    Referrer-Policy = "strict-origin-when-cross-origin"
```

### Regular Backups
1. Keep local copies of all files
2. Backup GitHub repository regularly
3. Document all changes

### Monitor for Issues
1. Set up Netlify notifications
2. Check deployment logs regularly
3. Monitor website uptime

---

## Advanced Features

### Add Contact Form Backend

**Option 1: Formspree (Recommended)**
1. Go to https://formspree.io
2. Sign up with email
3. Create new form
4. Get form ID
5. Update form action in `index.html`:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

**Option 2: Netlify Forms**
1. Add `netlify` attribute to form:

```html
<form name="contact" method="POST" netlify>
```

2. Deploy to Netlify
3. Form submissions appear in Netlify dashboard

### Add Analytics

**Google Analytics:**
1. Create account at https://analytics.google.com
2. Get tracking code
3. Add to `<head>` in `index.html`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

### Add Blog (Optional)

Use a static site generator:
- **Hugo**: https://gohugo.io
- **Jekyll**: https://jekyllrb.com
- **Gatsby**: https://www.gatsbyjs.com

---

## Maintenance Checklist

### Weekly
- [ ] Check website loads correctly
- [ ] Test contact form
- [ ] Verify all links work

### Monthly
- [ ] Review analytics
- [ ] Check for broken images
- [ ] Update content if needed
- [ ] Test on mobile devices

### Quarterly
- [ ] Update project portfolio
- [ ] Review and refresh content
- [ ] Check performance metrics
- [ ] Backup all files

### Annually
- [ ] Renew domain registration
- [ ] Review and update company information
- [ ] Audit website for security
- [ ] Plan website improvements

---

## Support Resources

### Netlify Help
- Documentation: https://docs.netlify.com
- Support: https://www.netlify.com/support
- Community: https://community.netlify.com

### GitHub Help
- Documentation: https://docs.github.com
- Support: https://support.github.com

### Web Development
- MDN Web Docs: https://developer.mozilla.org
- W3Schools: https://www.w3schools.com
- Stack Overflow: https://stackoverflow.com

---

## Frequently Asked Questions

**Q: How much does Netlify cost?**
A: Free tier includes unlimited sites, bandwidth, and builds. Premium plans available for advanced features.

**Q: Can I use my own domain?**
A: Yes! Connect any domain you own to your Netlify site.

**Q: How long does deployment take?**
A: Usually 30 seconds to 2 minutes.

**Q: Can I rollback to previous versions?**
A: Yes! Netlify keeps deployment history. Go to "Deploys" tab to restore previous versions.

**Q: Is my website secure?**
A: Yes! Netlify provides free SSL/HTTPS certificates for all sites.

**Q: Can I add more features later?**
A: Yes! You can update and redeploy anytime.

**Q: What if I need help?**
A: Contact Netlify support or consult with a web developer.

---

## Next Steps

1. ✅ Create GitHub account and repository
2. ✅ Upload all website files
3. ✅ Deploy on Netlify
4. ✅ Test website thoroughly
5. ✅ Set up custom domain (optional)
6. ✅ Configure analytics
7. ✅ Share website with team
8. ✅ Monitor and maintain

---

**Congratulations! Your website is now live on the internet!**

For any questions or issues, refer to the Netlify documentation or contact support.

**Website Deployed**: April 2024
**Last Updated**: April 2024
