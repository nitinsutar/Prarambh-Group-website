# 🔧 Vercel Deployment Troubleshooting Guide

## Issue: Styles Not Loading (Page Looks Unstyled)

### ✅ FIXED IN THIS VERSION

The previous version had incorrect file paths. This has been fixed with:
- `<link rel="stylesheet" href="./styles.css">` (added `./`)
- `<script src="./script.js">` (added `./`)

---

## How to Verify Your Deployment

### Step 1: Check Files on GitHub
Before deploying to Vercel, verify on GitHub:

1. Go to your repository
2. Check that these files exist:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `images/` folder

### Step 2: Redeploy on Vercel

If you already deployed and it looked unstyled:

1. Download the NEW fixed ZIP file
2. Update your GitHub repository:

```bash
# Navigate to your project
cd prarambh-group-website

# Add the fixed files
git add .
git commit -m "Fixed CSS and JS paths for Vercel"
git push
```

3. Vercel will automatically redeploy (takes 30 seconds)
4. Refresh your browser (Ctrl+Shift+R or Cmd+Shift+R)

---

## Common Vercel Deployment Issues & Fixes

### Issue 1: CSS Not Loading ✅ FIXED

**Symptom:** Page shows text but no styling (like your screenshot)

**Cause:** Incorrect file paths in HTML

**Solution:** Use relative paths with `./`
- ❌ `href="styles.css"`
- ✅ `href="./styles.css"`

---

### Issue 2: Images Not Showing

**Symptom:** Image placeholders or broken image icons

**Causes & Solutions:**

**A. Images not uploaded**
```bash
# Check if images folder exists in GitHub
# Should see: images/vimal-paradise-main.jpg, etc.
```

**B. Incorrect image paths**
- ❌ `src="images/photo.jpg"` or `src="/images/photo.jpg"`
- ✅ `src="./images/photo.jpg"`

**C. Wrong image names**
```bash
# Files must match EXACTLY (case-sensitive)
✅ vimal-paradise-main.jpg
❌ Vimal-Paradise-Main.jpg
❌ vimal_paradise_main.jpg
```

---

### Issue 3: 404 Error on Page Load

**Cause:** Vercel can't find index.html

**Solution:**

1. Ensure `index.html` is in the ROOT directory, not in a subfolder
2. Check repository structure:
```
your-repo/
├── index.html      ✅ Here (root level)
├── styles.css
├── script.js
└── images/
```

NOT like this:
```
your-repo/
└── website/
    ├── index.html  ❌ Wrong (inside subfolder)
```

**Fix:**
- In Vercel dashboard → Settings → General
- Set "Root Directory" to `./` or leave blank

---

### Issue 4: Changes Not Showing

**Symptom:** Made updates but site looks the same

**Solutions:**

**A. Clear Browser Cache**
```
Chrome/Edge: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
Firefox: Ctrl+Shift+Delete → Clear cache
```

**B. Wait for Deployment**
- Check Vercel dashboard for deployment status
- Green checkmark = deployed
- Usually takes 30-60 seconds

**C. Check Git Push Succeeded**
```bash
# Verify files pushed to GitHub
git status          # Should say "nothing to commit"
git log --oneline   # Should show your recent commit
```

---

### Issue 5: Fonts Not Loading

**Symptom:** Text appears in default system font

**Cause:** Google Fonts link blocked or failed

**Solution:** 
Already included correctly in HTML:
```html
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=Work+Sans:wght@300;400;500&display=swap" rel="stylesheet">
```

If still not working:
- Check browser console for errors (F12 → Console tab)
- Ensure no ad blockers blocking Google Fonts

---

## Step-by-Step Redeployment (If Needed)

### Method 1: Update Existing Deployment

```bash
# 1. Extract new ZIP file
# 2. Navigate to folder
cd prarambh-group-website

# 3. Commit changes
git add .
git commit -m "Fixed file paths for Vercel deployment"

# 4. Push to GitHub
git push

# 5. Wait 30 seconds
# 6. Hard refresh browser (Ctrl+Shift+R)
```

### Method 2: Fresh Deployment

If completely stuck:

1. Delete existing project on Vercel (Settings → Delete Project)
2. Delete existing GitHub repository
3. Extract fresh ZIP file
4. Create new GitHub repository
5. Push files
6. Import to Vercel again

---

## Vercel Build Settings (Should Be)

When deploying, use these settings:

- **Framework Preset:** Other (or None)
- **Build Command:** (leave empty)
- **Output Directory:** (leave empty)
- **Install Command:** (leave empty)
- **Root Directory:** `./` or (leave empty)

---

## Testing Checklist

After deployment, test:

- [ ] Page loads without errors
- [ ] Navigation bar styled correctly
- [ ] Hero section with gradient background
- [ ] Typography shows correct fonts (Cormorant Garamond + Work Sans)
- [ ] Dark features section visible
- [ ] Gallery grid displays properly
- [ ] Contact section styled
- [ ] Footer dark background
- [ ] Smooth scrolling works
- [ ] Hover effects work on links
- [ ] Mobile responsive (test on phone)

---

## Debug Mode: Check Browser Console

1. Open your deployed site
2. Press `F12` (or right-click → Inspect)
3. Go to "Console" tab
4. Look for errors in red

**Common Errors:**

```
Failed to load resource: styles.css 404
```
**Fix:** File path wrong or file missing

```
Failed to load resource: images/photo.jpg 404
```
**Fix:** Image not uploaded or wrong name

---

## Vercel Deployment Logs

To check what went wrong:

1. Go to Vercel Dashboard
2. Click your project
3. Click latest deployment
4. Click "View Function Logs" or "Build Logs"
5. Look for error messages

---

## Still Having Issues?

### Quick Checklist:

1. ✅ Used the FIXED ZIP file (with ./ paths)
2. ✅ All files in GitHub (index.html, styles.css, script.js)
3. ✅ Images added to images/ folder
4. ✅ File names match exactly (case-sensitive)
5. ✅ Cleared browser cache
6. ✅ Waited for Vercel deployment to complete
7. ✅ Hard refreshed browser (Ctrl+Shift+R)

### Test Locally First:

Before deploying to Vercel, test locally:

```bash
# Using Python
cd prarambh-group-website
python -m http.server 8000

# Open browser to: http://localhost:8000
```

If it works locally but not on Vercel:
- File paths are wrong
- Files not pushed to GitHub
- Cache issue

---

## Contact & Support

If issues persist:

1. Check Vercel Documentation: [vercel.com/docs](https://vercel.com/docs)
2. Check browser console for specific errors
3. Verify all files pushed to GitHub
4. Try fresh deployment

---

**Remember:** The FIXED version has:
- `href="./styles.css"` (with `./`)
- `src="./script.js"` (with `./`)
- `src="./images/photo.jpg"` (with `./`)

This should resolve the styling issue you experienced! 🎉