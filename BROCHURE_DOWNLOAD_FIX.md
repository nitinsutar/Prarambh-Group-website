# 🔧 Brochure Download Fix - 4KB File Issue

## ❌ Problem

Getting a 4KB file instead of your 2.5MB brochure PDF. The small file won't open because it's actually an error page, not your PDF.

## ✅ Solution

The PDF file isn't uploaded to GitHub/Vercel yet. Here's how to fix it:

---

## 📝 Step-by-Step Fix

### Option 1: Upload via GitHub Website (Easiest)

1. **Go to your GitHub repository**
   - Open your browser
   - Go to github.com/yourusername/Prarambh-Group-website

2. **Navigate to brochures folder**
   - Click on the `brochures` folder
   - You should see only `README.txt`

3. **Upload your PDF**
   - Click "Add file" → "Upload files"
   - Drag and drop your PDF file
   - **Make sure it's named:** `vimal-paradise-brochure.pdf`
   - Scroll down and click "Commit changes"

4. **Wait for Vercel**
   - Vercel auto-deploys (30 seconds)
   - Hard refresh your site: `Ctrl+Shift+R`

5. **Test again**
   - Fill the brochure form
   - Should download the full 2.5MB file now!

---

### Option 2: Upload via Git Command Line

```bash
# Navigate to your project
cd prarambh-group-website

# Add your PDF to the brochures folder
# Copy your PDF file to: brochures/vimal-paradise-brochure.pdf

# Add to git
git add brochures/vimal-paradise-brochure.pdf

# Commit
git commit -m "Added Vimal Paradise brochure PDF"

# Push to GitHub
git push

# Wait 30 seconds for Vercel to deploy
```

---

## ⚠️ Important Checklist

Before uploading, verify:

- [ ] PDF file is named EXACTLY: `vimal-paradise-brochure.pdf`
- [ ] All lowercase letters
- [ ] Uses hyphens (-), not underscores (_) or spaces
- [ ] Has `.pdf` extension (not `.PDF` in capitals)
- [ ] File size is 2.5MB (your actual file)
- [ ] PDF opens correctly on your computer

---

## 🔍 Verify Upload

After uploading, check:

1. **On GitHub:**
   - Go to your repository
   - Click `brochures/` folder
   - You should see: `vimal-paradise-brochure.pdf`
   - Click on it to preview
   - Should show "2.5 MB" or similar

2. **On Vercel:**
   - Check deployment succeeded (green checkmark)
   - Wait for "Production" deployment to complete

3. **Test Download:**
   - Go to your live website
   - Click "Download Brochure"
   - Fill the form
   - File should be 2.5MB and open properly

---

## 🎯 Common Issues

### Issue: File still 4KB after upload

**Solution:**
1. Clear browser cache completely
2. Try in Incognito/Private mode
3. Check the file uploaded to GitHub (verify file size)
4. Force Vercel to rebuild:
   ```bash
   git commit --allow-empty -m "Trigger rebuild"
   git push
   ```

### Issue: PDF won't upload to GitHub

**Solution:**
- GitHub has file size limits (usually 100MB, you're fine)
- Make sure you're in the correct branch (main)
- Try uploading via GitHub website instead of command line

### Issue: Different filename

**If your PDF has a different name:**

Option A: Rename your PDF to match
```bash
mv your-brochure.pdf vimal-paradise-brochure.pdf
```

Option B: Update the code to match your filename

In `index.html`, find (around line 920):
```javascript
link.href = './brochures/vimal-paradise-brochure.pdf';
link.download = 'Vimal-Paradise-Brochure.pdf';
```

Change to:
```javascript
link.href = './brochures/your-actual-filename.pdf';
link.download = 'Your-Download-Name.pdf';
```

---

## 📁 Correct File Structure

Your GitHub repository should look like:

```
Prarambh-Group-website/
├── brochures/
│   ├── README.txt                        (can delete this)
│   └── vimal-paradise-brochure.pdf       ← 2.5 MB file
├── images/
│   ├── vimal-paradise-main.jpg
│   ├── gallery-1.jpg
│   ├── gallery-2.jpg
│   ├── gallery-3.jpg
│   ├── gallery-4.jpg
│   └── gallery-5.jpg
├── index.html
└── [other files]
```

---

## ✅ Verification Steps

After upload:

1. **Check GitHub:**
   ```
   https://github.com/yourusername/yourrepo/tree/main/brochures
   ```
   Should show your PDF with correct file size

2. **Check Live URL:**
   ```
   https://your-site.vercel.app/brochures/vimal-paradise-brochure.pdf
   ```
   Should download the full PDF directly

3. **Test Form:**
   - Fill out brochure form
   - Check downloaded file size (should be 2.5MB)
   - Open PDF - should work perfectly

---

## 💡 Pro Tip

You can test the PDF URL directly:

1. Go to: `https://your-site.vercel.app/brochures/vimal-paradise-brochure.pdf`
2. Should download immediately
3. If it's 4KB, the file isn't uploaded yet
4. If it's 2.5MB, you're good!

---

## 🚨 Quick Fix Summary

**The issue:** PDF not uploaded to GitHub/Vercel  
**The fix:** Upload `vimal-paradise-brochure.pdf` to `brochures/` folder  
**Time to fix:** 2 minutes  

Upload the file, wait 30 seconds, test again! 🚀

---

## 📞 Still Having Issues?

1. Verify PDF is in GitHub repository
2. Check Vercel deployment succeeded
3. Try accessing PDF directly via URL
4. Clear all browser cache
5. Test in Incognito mode

The 4KB file is just a "file not found" error page. Once you upload your actual PDF to GitHub, it will work perfectly!

---

**Your form is working great! Just need to upload that PDF.** ✅