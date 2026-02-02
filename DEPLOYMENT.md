# Vercel Deployment Guide for Portfolio

## Overview
This guide will help you deploy your portfolio to Vercel with the custom domain **poderosacoding.com** (or poderosacoding.vercel.app).

## Prerequisites
- GitHub account
- Vercel account (free tier is sufficient)
- Domain name: poderosacoding.com (if you want a custom domain)

## Step 1: Set Up GitHub Repository

1. **Create a new GitHub repository**
   - Go to https://github.com/new
   - Repository name: `portfolio` (or any name you prefer)
   - Make it Public or Private
   - Don't initialize with README (we already have files)
   - Click "Create repository"

2. **Push your code to GitHub**
   ```bash
   cd /Users/lidiadelacruz/Documents/Projects/Portfolio
   git init
   git add .
   git commit -m "Initial portfolio commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/portfolio.git
   git push -u origin main
   ```
   Replace `YOUR-USERNAME` with your GitHub username.

## Step 2: Deploy to Vercel

### Option A: Deploy via Vercel Dashboard (Recommended)

1. **Sign in to Vercel**
   - Go to https://vercel.com
   - Sign up or log in (you can use your GitHub account)

2. **Import your project**
   - Click "Add New..." → "Project"
   - Select "Import Git Repository"
   - Choose your portfolio repository
   - Click "Import"

3. **Configure your project**
   - Framework Preset: Leave as "Other"
   - Root Directory: `./`
   - Build Command: Leave empty
   - Output Directory: Leave empty
   - Install Command: Leave empty

4. **Deploy**
   - Click "Deploy"
   - Wait for deployment to complete (usually takes 30-60 seconds)
   - You'll get a URL like: `portfolio-USERNAME.vercel.app`

### Option B: Deploy via Vercel CLI

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**
   ```bash
   vercel login
   ```

3. **Deploy**
   ```bash
   cd /Users/lidiadelacruz/Documents/Projects/Portfolio
   vercel
   ```
   
   Follow the prompts:
   - Set up and deploy? Yes
   - Which scope? Select your account
   - Link to existing project? No
   - Project name? portfolio (or your preferred name)
   - In which directory is your code located? ./
   - Deploy? Yes

## Step 3: Configure Custom Domain (Optional)

### If you have poderosacoding.com domain:

1. **Add domain in Vercel**
   - Go to your project in Vercel Dashboard
   - Click "Settings" → "Domains"
   - Enter `poderosacoding.com`
   - Click "Add"

2. **Configure DNS**
   - Vercel will show you DNS records to add
   - Go to your domain registrar (GoDaddy, Namecheap, etc.)
   - Add the DNS records as shown:
     - Type: A Record
     - Name: @ (or leave blank)
     - Value: 76.76.21.21
     
     - Type: CNAME
     - Name: www
     - Value: cname.vercel-dns.com

3. **Wait for DNS propagation**
   - Can take 24-48 hours
   - Vercel will auto-detect when ready

### If you want to use poderosacoding.vercel.app:

The URL `poderosacoding.vercel.app` might already be taken. Vercel will automatically assign you:
- `portfolio-yourusername.vercel.app`

You can try to claim `poderosacoding.vercel.app` if available by adding it as a domain in Vercel settings.

## Step 4: Verify Deployment

1. **Test your site**
   - Visit your Vercel URL
   - Check all links work
   - Test on mobile device
   - Verify social links open correctly

2. **Run Lighthouse Audit**
   - Open Chrome DevTools (F12)
   - Go to "Lighthouse" tab
   - Click "Generate report"
   - Aim for 90+ scores across all metrics

## Automatic Deployments

Vercel automatically deploys:
- **Production deployments**: Every push to `main` branch
- **Preview deployments**: Every pull request

## Updating Your Portfolio

1. **Make changes locally**
   ```bash
   # Edit index.html or other files
   ```

2. **Commit and push**
   ```bash
   git add .
   git commit -m "Update portfolio content"
   git push origin main
   ```

3. **Auto-deploy**
   - Vercel automatically detects the push
   - Builds and deploys in ~30 seconds
   - Check deployment status in Vercel Dashboard

## Troubleshooting

### Issue: Build fails
- Check Vercel build logs
- Ensure all file paths are correct
- Verify HTML is valid

### Issue: Images not loading
- Check image URLs
- Ensure images are committed to Git
- Use absolute paths or relative paths correctly

### Issue: Domain not working
- Verify DNS records are correct
- Wait for DNS propagation (24-48 hours)
- Check domain status in Vercel Dashboard

### Issue: Custom domain already taken
- Try variations: poderosacoding-portfolio.vercel.app
- Or use your username: yourusername-portfolio.vercel.app

## Performance Tips

1. **Optimize images**
   - Compress images before uploading
   - Use WebP format when possible
   - Limit images to 200KB each

2. **Monitor performance**
   - Check Vercel Analytics (free tier included)
   - Run regular Lighthouse audits
   - Monitor Core Web Vitals

## Environment Variables (if needed later)

If you need to add environment variables:
1. Go to Project Settings → Environment Variables
2. Add key-value pairs
3. Redeploy to apply

## Support Resources

- Vercel Documentation: https://vercel.com/docs
- Vercel Support: https://vercel.com/support
- Community: https://github.com/vercel/vercel/discussions

## Next Steps

1. ✅ Deploy to Vercel
2. ✅ Verify deployment works
3. ⏳ Add custom domain (optional)
4. ⏳ Share link on LinkedIn
5. ⏳ Update portfolio as you complete new projects

---

**Your portfolio is now live on Vercel! 🎉**
