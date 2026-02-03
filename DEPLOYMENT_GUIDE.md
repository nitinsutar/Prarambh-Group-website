# 🚀 Deployment Guide - GitHub & Vercel

Complete step-by-step guide to deploy your Prarambh Group website.

---

## 📋 Prerequisites

- GitHub account ([Sign up free](https://github.com/signup))
- Vercel account ([Sign up free](https://vercel.com/signup))
- Git installed on your computer ([Download Git](https://git-scm.com/downloads))

---

## 🎯 Step-by-Step Deployment

### PART 1: Setup Your Project Files

#### Step 1: Add Your Images
1. Create an `images` folder in the project directory
2. Add your 6 photos with exact names:
   - `vimal-paradise-main.jpg`
   - `gallery-1.jpg`
   - `gallery-2.jpg`
   - `gallery-3.jpg`
   - `gallery-4.jpg`
   - `gallery-5.jpg`
3. See `IMAGE_GUIDE.md` for detailed photo requirements

#### Step 2: Customize Content
1. Open `index.html` in a text editor
2. Update contact information:
   - Email address
   - Phone number
   - Location details
3. Update project details (location, type, status, units)
4. Save changes

---

### PART 2: Upload to GitHub

#### Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com)
2. Click the **"+"** icon (top right) → **"New repository"**
3. Fill in details:
   - **Repository name:** `prarambh-group-website` (or your choice)
   - **Description:** "Official website for Prarambh Group - Vimal Paradise"
   - **Public** or **Private** (your choice)
   - **DO NOT** initialize with README (we already have one)
4. Click **"Create repository"**

#### Step 2: Initialize Git Locally

Open Terminal/Command Prompt in your project folder:

```bash
# Navigate to your project folder
cd path/to/prarambh-group-website

# Initialize git repository
git init

# Add all files to git
git add .

# Create first commit
git commit -m "Initial commit: Prarambh Group website"

# Rename branch to main (if needed)
git branch -M main
```

#### Step 3: Connect to GitHub

Copy the commands from GitHub (shown after creating repository), or use these:

```bash
# Add your GitHub repository as remote
# Replace YOUR-USERNAME and YOUR-REPO-NAME with your actual details
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git push -u origin main
```

**Example:**
```bash
git remote add origin https://github.com/johnsmith/prarambh-group-website.git
git push -u origin main
```

You'll be asked to login to GitHub - enter your credentials.

#### Step 4: Verify Upload

1. Refresh your GitHub repository page
2. You should see all your files uploaded
3. Check that the `images` folder and all files are there

---

### PART 3: Deploy to Vercel

#### Method 1: Deploy via GitHub (RECOMMENDED)

##### Step 1: Sign Up for Vercel
1. Go to [Vercel.com](https://vercel.com/signup)
2. Click **"Continue with GitHub"**
3. Authorize Vercel to access your GitHub

##### Step 2: Import Project
1. On Vercel dashboard, click **"Add New..."** → **"Project"**
2. Find your `prarambh-group-website` repository
3. Click **"Import"**

##### Step 3: Configure Project
1. **Project Name:** Leave as is or change
2. **Framework Preset:** Leave as "Other" (it's static HTML)
3. **Root Directory:** Leave as `./`
4. **Build Settings:** Leave empty (not needed for static site)

##### Step 4: Deploy!
1. Click **"Deploy"**
2. Wait 30-60 seconds for deployment
3. You'll see a success screen with your live URL!

##### Step 5: Get Your Live URL
- Vercel gives you a URL like: `prarambh-group-website.vercel.app`
- Click the link to view your live site!
- Share this URL with anyone

---

#### Method 2: Deploy via Vercel CLI (Alternative)

If you prefer using command line:

```bash
# Install Vercel CLI globally
npm install -g vercel

# Login to Vercel
vercel login

# Deploy
vercel

# Follow the prompts:
# - Link to existing project? No
# - Project name: prarambh-group-website
# - Directory: ./
# - Override settings? No

# For production deployment
vercel --prod
```

---

#### Method 3: Drag & Drop (Quick Test)

For quick deployment without GitHub:

1. Zip your entire project folder
2. Go to [vercel.com/new](https://vercel.com/new)
3. Drag and drop the ZIP file
4. Wait for deployment

**Note:** This method won't auto-update from GitHub.

---

## 🔄 Making Updates After Deployment

### Update Your Live Site

When you want to make changes:

```bash
# 1. Make your changes to files locally

# 2. Add changes to git
git add .

# 3. Commit changes
git commit -m "Updated contact information"

# 4. Push to GitHub
git push

# 5. Vercel automatically deploys! (if using GitHub method)
# Your site updates in ~30 seconds
```

### Update Images

```bash
# 1. Replace images in the images/ folder

# 2. Commit and push
git add images/
git commit -m "Updated project images"
git push

# Done! Vercel auto-deploys the new images
```

---

## 🌐 Custom Domain (Optional)

### Add Your Own Domain

If you have a domain like `prarambhgroup.com`:

1. In Vercel dashboard, go to your project
2. Click **"Settings"** → **"Domains"**
3. Click **"Add"**
4. Enter your domain name
5. Follow DNS configuration instructions
6. Wait for DNS propagation (5-60 minutes)

**Domain Providers:**
- [Namecheap](https://www.namecheap.com) - ₹500-800/year
- [GoDaddy](https://www.godaddy.com) - ₹600-1000/year
- [Google Domains](https://domains.google) - ₹800-1200/year

---

## ✅ Deployment Checklist

Before going live, verify:

- [ ] All 6 images uploaded and displaying correctly
- [ ] Contact information updated (email, phone)
- [ ] Project details are accurate
- [ ] Website tested on mobile phone
- [ ] Website tested on desktop
- [ ] All links work
- [ ] No Lorem Ipsum or placeholder text
- [ ] Smooth scrolling navigation works
- [ ] Images load quickly (optimized)

---

## 🎨 Post-Deployment Customization

### Add Google Analytics (Optional)

1. Get your Google Analytics tracking code
2. Add before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Add Favicon (Optional)

1. Create a 32x32px icon (favicon.ico)
2. Place in root directory
3. Add to `<head>` in index.html:

```html
<link rel="icon" type="image/x-icon" href="/favicon.ico">
```

---

## 🆘 Troubleshooting

### Problem: Git push rejected
**Solution:** 
```bash
git pull origin main --rebase
git push origin main
```

### Problem: Images not showing on Vercel
**Solution:**
- Check image paths are correct: `images/filename.jpg`
- Check filenames match exactly (case-sensitive)
- Check images are in the `images` folder before pushing

### Problem: Vercel deployment failed
**Solution:**
- Check all files are valid (HTML, CSS, JS)
- Look at deployment logs in Vercel dashboard
- Ensure no build errors

### Problem: Changes not appearing on live site
**Solution:**
- Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Wait 1-2 minutes for Vercel to deploy
- Check Vercel dashboard for deployment status

---

## 📞 Support Resources

- **Vercel Documentation:** [vercel.com/docs](https://vercel.com/docs)
- **GitHub Guides:** [guides.github.com](https://guides.github.com)
- **Git Tutorial:** [git-scm.com/doc](https://git-scm.com/doc)

---

## 🎉 You're Done!

Congratulations! Your website is now live on the internet.

**Share your live URL:**
- `https://your-project-name.vercel.app`

**Next Steps:**
1. Share the link with your team
2. Test on multiple devices
3. Consider adding a custom domain
4. Monitor with Google Analytics
5. Update content as needed

---

Need help? Contact: info@prarambhgroup.com