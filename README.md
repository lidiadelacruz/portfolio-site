# Portfolio Website

A clean, minimalist portfolio website showcasing community management and creator collaboration work.

## 🌟 Overview

This is a single-page portfolio website built for Lidia de la Cruz, highlighting community building, workshop facilitation, and creator relations work. The site is designed to be fast, accessible, and easy to share with potential employers and collaborators.

## 🎯 Features

- **Single-page design** - All content on one page for easy scanning
- **Responsive layout** - Works perfectly on desktop, tablet, and mobile
- **Fast loading** - Optimized for performance (< 2 second load time)
- **Accessible** - WCAG 2.1 Level AA compliant
- **SEO optimized** - Proper meta tags and structured data
- **Zero dependencies** - Pure HTML, CSS, and vanilla JavaScript

## 🚀 Quick Start

### View Locally

1. **Clone or download this repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/portfolio.git
   cd portfolio
   ```

2. **Open in browser**
   - Simply open `index.html` in your web browser
   - Or use a local server:
     ```bash
     python3 -m http.server 8000
     ```
     Then visit: http://localhost:8000

### Deploy to Vercel

See [DEPLOYMENT.md](DEPLOYMENT.md) for complete deployment instructions.

**Quick deploy:**
1. Push to GitHub
2. Import to Vercel
3. Deploy (takes ~30 seconds)
4. Your site is live!

## 📁 Project Structure

```
Portfolio/
├── index.html           # Main portfolio page (all-in-one file)
├── vercel.json         # Vercel configuration
├── DEPLOYMENT.md       # Deployment guide
├── README.md           # This file
├── prd.md             # Product requirements document
└── Technicalprd.md    # Technical specifications
```

## 🎨 Design System

### Colors
- **Primary Black**: #000000 - Main text
- **Navy Blue**: #14213d - Headings and accents
- **Orange**: #fca311 - Call-to-action buttons
- **Light Gray**: #e5e5e5 - Borders
- **White**: #ffffff - Background

### Typography
- **System fonts** for optimal performance
- **Font sizes**: Responsive scaling from mobile to desktop
- **Font weights**: 400 (regular), 500 (medium), 600-700 (headings)

### Layout
- **Max-width**: 800px for optimal readability
- **Mobile-first**: Responsive design
- **Spacing**: Consistent spacing system

## ✏️ Customization

### Update Content

Edit the HTML file directly to update:

1. **Personal Information** (lines 105-140)
   - Name
   - Title
   - Tagline
   - Social links

2. **About Section** (lines 145-160)
   - Bio text
   - Expertise tags

3. **Featured Work** (lines 165-240)
   - Add/remove work examples
   - Update descriptions
   - Change LinkedIn links

### Update Profile Image

Replace the placeholder image URL (line 107):
```html
<img src="https://via.placeholder.com/120" alt="Your Name">
```

With your actual image:
```html
<img src="path/to/your-photo.jpg" alt="Your Name">
```

**Image requirements:**
- Recommended size: 240x240px (displays at 120px)
- Format: JPG or PNG
- Optimized/compressed
- Square aspect ratio

### Update Social Links

Update the URLs in the social links section (lines 135-138):
```html
<a href="https://linkedin.com/in/YOUR-USERNAME">LinkedIn</a>
<a href="https://github.com/YOUR-USERNAME">GitHub</a>
<a href="https://instagram.com/YOUR-USERNAME">Instagram</a>
<a href="https://x.com/YOUR-USERNAME">X (Twitter)</a>
```

### Add New Work Examples

Copy a work item block and update the content:

```html
<article class="work-item">
    <h3 class="work-title">Your Project Title</h3>
    <p class="work-organization">Organization Name</p>
    
    <div class="work-tags">
        <span class="tag">Tag 1</span>
        <span class="tag">Tag 2</span>
    </div>
    
    <p class="work-description">Project description...</p>
    <p class="work-role">Your role and contributions...</p>
    
    <a href="YOUR-LINK" class="work-link">View Details</a>
</article>
```

## 🧪 Testing

### Before Deploying

1. **Validate HTML**
   - Use https://validator.w3.org/
   - Ensure no errors

2. **Test Responsiveness**
   - Test on mobile, tablet, desktop
   - Use browser DevTools responsive mode

3. **Check Links**
   - Verify all external links work
   - Test LinkedIn links
   - Test social media links

4. **Run Lighthouse**
   - Open Chrome DevTools (F12)
   - Go to Lighthouse tab
   - Run audit
   - Aim for 90+ scores

### Performance Checklist

- [ ] Page loads in < 2 seconds
- [ ] All images optimized
- [ ] No console errors
- [ ] Links work correctly
- [ ] Mobile responsive
- [ ] Accessible (keyboard navigation works)

## 📱 Browser Support

Tested and working on:
- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Mobile Safari (iOS 14+)
- Chrome Mobile (latest)

## ♿ Accessibility

This site follows WCAG 2.1 Level AA guidelines:

- ✅ Semantic HTML structure
- ✅ Proper heading hierarchy
- ✅ Alt text for images
- ✅ Keyboard navigation support
- ✅ Color contrast ratios meet standards
- ✅ Focus indicators visible
- ✅ Screen reader compatible

## 📊 Performance

Target metrics:
- **First Contentful Paint**: < 1.0s
- **Largest Contentful Paint**: < 1.5s
- **Time to Interactive**: < 2.0s
- **Lighthouse Score**: 90+

## 🔒 Security & Privacy

- No tracking scripts
- No cookies
- No data collection
- External links use `rel="noopener noreferrer"`

## 🛠️ Built With

- **HTML5** - Semantic markup
- **CSS3** - Modern styling (Grid, Flexbox, Custom Properties)
- **Vanilla JavaScript** - Optional enhancements
- **Vercel** - Hosting platform

## 📝 License

This portfolio template is free to use and modify for personal or commercial projects.

## 💡 Tips for Success

1. **Keep it updated** - Add new work examples as you complete projects
2. **Optimize images** - Compress all images before uploading
3. **Test regularly** - Check your site on different devices
4. **Share widely** - Add your portfolio URL to your LinkedIn, resume, and email signature
5. **Monitor analytics** - Use Vercel Analytics to track visitors

## 🤝 Support

If you encounter issues:
1. Check [DEPLOYMENT.md](DEPLOYMENT.md) for deployment help
2. Review the Technical PRD for detailed specifications
3. Verify your HTML is valid
4. Test in different browsers

## 🎯 Recommended Domain Options

If `poderosacoding.com` is not available, consider:
- `poderosacoding.dev`
- `poderosacoding.io`
- `poderosacoding.me`
- Use the free Vercel subdomain: `yourname.vercel.app`

## 📞 Next Steps

1. ✅ Customize content with your information
2. ✅ Add your profile photo
3. ✅ Update social links
4. ✅ Test locally
5. ✅ Deploy to Vercel
6. ✅ Share your portfolio!

---

**Built with ❤️ for community builders everywhere.**

For deployment instructions, see [DEPLOYMENT.md](DEPLOYMENT.md)
