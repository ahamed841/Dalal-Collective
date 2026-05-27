# Dalal Collective - Deployment Guide

## Current Status
✅ Repository created and initialized  
✅ GitHub Pages enabled  
✅ Website files ready for deployment

## Important Notes

### PHP Contact Form
Your website includes a `mail.php` contact form handler. **GitHub Pages is a static hosting service and does NOT support PHP.**

To enable the contact form, you have these options:

#### Option 1: Use Formspree (Recommended - Free)
1. Visit [formspree.io](https://formspree.io)
2. Create an account and add your form
3. Update your contact form in `index.html` to point to Formspree
4. This handles email delivery automatically

#### Option 2: Deploy to Server with PHP Support
- Keep current hosting at: honeydew-bison-951207.hostingersite.com
- Or use alternatives like:
  - Heroku
  - PythonAnywhere
  - DigitalOcean
  - AWS Lambda

#### Option 3: Use Netlify Forms
1. Deploy to Netlify instead of GitHub Pages
2. Netlify has built-in form handling
3. Visit [netlify.com](https://netlify.com)

## Deployment Steps

### Step 1: Enable GitHub Pages
1. Go to: https://github.com/ahamed841/Dalal-Collective/settings
2. Scroll to **Pages** section
3. Select:
   - Source: "Deploy from a branch"
   - Branch: "main"
   - Folder: "/ (root)"
4. Click **Save**

### Step 2: Wait for Build
GitHub Pages will automatically build and deploy your site. Check the **Actions** tab to monitor build status.

### Step 3: Access Your Site
Your live site will be available at:
```
https://ahamed841.github.io/Dalal-Collective/
```

## File Structure
```
├── index.html          # Main landing page
├── mail.php            # Contact form (requires PHP server)
├── css/
│   ├── main_new.css    # Main styles
│   ├── plugins.css     # Plugin styles
│   └── loaders/
│       └── loader.css  # Loading animation
├── js/
│   ├── app.js          # Main application script
│   └── libs.min.js     # Libraries
├── img/                # Images and assets
├── video/              # Video files
├── fonts/              # Custom fonts
└── dalal_image/        # Dalal-specific images
```

## Next Steps

1. **Verify Deployment**: Visit the GitHub Pages URL
2. **Set Custom Domain** (optional):
   - If you own a domain, configure it in Settings > Pages
3. **Fix Contact Form**: Choose and implement one of the solutions above
4. **Monitor**: Use GitHub Actions tab to monitor deployments

## Support

For questions about:
- **GitHub Pages**: https://docs.github.com/en/pages
- **Formspree**: https://formspree.io/docs
- **Netlify**: https://docs.netlify.com

## Local Development

To test locally before pushing:
```bash
# Option 1: Use Python
python -m http.server 8000

# Option 2: Use Node.js
npx http-server

# Then visit: http://localhost:8000
```

---

**Your website is now deployed to the cloud! 🚀**
