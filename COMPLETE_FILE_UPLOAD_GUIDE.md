# 📁 Complete File Upload Guide - Images, Logo & Brochure

## 🎯 **ALL FILES YOU NEED TO UPLOAD**

Your website needs these files in specific folders on GitHub:

---

## 📸 **1. PROJECT IMAGES (6 files)**

### **Location:** `images/` folder

### **Required Files:**

#### **1. vimal-paradise-main.jpg**
- **Where it appears:** Featured Project section (main large image)
- **Recommended size:** 1600 x 1200 pixels (4:3 ratio)
- **What to use:** Best exterior shot of Vimal Paradise building
- **Description:** This is the HERO image of your project showcase

#### **2. gallery-1.jpg**
- **Where it appears:** Gallery section (LARGEST image, 2x2 grid space)
- **Recommended size:** 1600 x 1600 pixels (square)
- **What to use:** Most impressive aerial view or architectural highlight
- **Description:** Featured gallery image

#### **3. gallery-2.jpg**
- **Where it appears:** Gallery section
- **Recommended size:** 800 x 800 pixels (square)
- **What to use:** Interior spaces - living room, bedroom, or model flat
- **Description:** Shows interior design

#### **4. gallery-3.jpg**
- **Where it appears:** Gallery section
- **Recommended size:** 800 x 800 pixels (square)
- **What to use:** Amenities - gym, pool, clubhouse
- **Description:** Lifestyle features

#### **5. gallery-4.jpg**
- **Where it appears:** Gallery section
- **Recommended size:** 800 x 800 pixels (square)
- **What to use:** Landscaping, gardens, outdoor spaces
- **Description:** Green areas and landscaping

#### **6. gallery-5.jpg**
- **Where it appears:** Gallery section
- **Recommended size:** 800 x 800 pixels (square)
- **What to use:** Different exterior angle or building detail
- **Description:** Additional architectural view

---

## 🎨 **2. LOGO FILE (1 file)**

### **Location:** `assets/` folder

### **Required File:**

#### **prarambh-logo.png**
- **Where it appears:** Header (top navigation) + Footer
- **Recommended size:** 500 x 200 pixels (or your logo's native size)
- **Format:** PNG with transparent background (preferred) or JPG
- **Description:** Your company logo
- **Height on site:** 40px in header, 50px in footer (auto-width)

**If you don't have a logo yet:**
- The site will show "PRARAMBH GROUP" text instead
- Logo adds automatically when you upload the file

---

## 📄 **3. BROCHURE PDF (1 file)**

### **Location:** `brochures/` folder

### **Required File:**

#### **vimal-paradise-brochure.pdf**
- **Where it appears:** Downloads when user fills brochure form
- **File size:** Your actual PDF (2.5MB in your case)
- **Format:** PDF
- **Description:** Project brochure with details, floor plans, pricing

**CRITICAL:**
- Must be named EXACTLY: `vimal-paradise-brochure.pdf`
- All lowercase
- Use hyphens (-)
- Must be actual PDF, not a renamed file

---

## 📂 **FOLDER STRUCTURE**

Your GitHub repository should look like this:

```
Prarambh-Group-website/
├── assets/                          ← CREATE THIS FOLDER
│   └── prarambh-logo.png           ← Your logo here
├── brochures/                       ← Should exist
│   └── vimal-paradise-brochure.pdf ← Your PDF here (2.5MB)
├── images/                          ← Should exist
│   ├── vimal-paradise-main.jpg     ← Main project image
│   ├── gallery-1.jpg               ← Gallery images
│   ├── gallery-2.jpg
│   ├── gallery-3.jpg
│   ├── gallery-4.jpg
│   └── gallery-5.jpg
├── index.html
└── [other files]
```

---

## 🚀 **HOW TO UPLOAD - METHOD 1: GitHub Website (Easiest)**

### **Step 1: Upload Project Images**

1. Go to your GitHub repository
2. Click on `images` folder
3. Click "Add file" → "Upload files"
4. Drag all 6 images at once:
   - vimal-paradise-main.jpg
   - gallery-1.jpg
   - gallery-2.jpg
   - gallery-3.jpg
   - gallery-4.jpg
   - gallery-5.jpg
5. Scroll down, click "Commit changes"

### **Step 2: Create Assets Folder & Upload Logo**

1. In your repository root, click "Add file" → "Create new file"
2. Type: `assets/prarambh-logo.png` (this creates the folder)
3. You can't upload here directly, so:
   - Cancel this
   - Use desktop GitHub or command line (see Method 2)
   
**OR via GitHub Desktop:**
1. Clone repository to computer
2. Create `assets` folder locally
3. Add `prarambh-logo.png` to it
4. Commit and push

### **Step 3: Upload Brochure PDF**

1. Click on `brochures` folder
2. Click "Add file" → "Upload files"
3. Upload your `vimal-paradise-brochure.pdf`
4. **VERIFY** file size shows as 2.5MB (not 4KB!)
5. Click "Commit changes"

---

## 🚀 **HOW TO UPLOAD - METHOD 2: Command Line (Recommended)**

```bash
# Navigate to your project
cd prarambh-group-website

# Create assets folder if it doesn't exist
mkdir -p assets

# Copy your files to correct locations:
# 1. Copy logo
cp /path/to/your/logo.png assets/prarambh-logo.png

# 2. Copy project images
cp /path/to/your/images/main-building.jpg images/vimal-paradise-main.jpg
cp /path/to/your/images/aerial-view.jpg images/gallery-1.jpg
cp /path/to/your/images/interior.jpg images/gallery-2.jpg
cp /path/to/your/images/amenities.jpg images/gallery-3.jpg
cp /path/to/your/images/landscape.jpg images/gallery-4.jpg
cp /path/to/your/images/exterior-2.jpg images/gallery-5.jpg

# 3. Copy brochure
cp /path/to/your/brochure.pdf brochures/vimal-paradise-brochure.pdf

# Add all files to git
git add assets/ images/ brochures/

# Commit
git commit -m "Added logo, images, and brochure"

# Push to GitHub
git push

# Wait 30-60 seconds for Vercel to deploy
```

---

## ✅ **VERIFICATION CHECKLIST**

After uploading, verify on GitHub:

### **Check Images Folder:**
```
✓ images/vimal-paradise-main.jpg (should see file size, like "450 KB")
✓ images/gallery-1.jpg
✓ images/gallery-2.jpg
✓ images/gallery-3.jpg
✓ images/gallery-4.jpg
✓ images/gallery-5.jpg
```

### **Check Assets Folder:**
```
✓ assets/prarambh-logo.png (should see file size)
```

### **Check Brochures Folder:**
```
✓ brochures/vimal-paradise-brochure.pdf (should show 2.5 MB or similar, NOT 4KB)
```

---

## 🔍 **TEST ON LIVE SITE**

After deployment (wait 30 seconds after push):

1. **Hard refresh:** `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)

2. **Check Header:**
   - Logo should appear in top left
   - If not, text "PRARAMBH GROUP" shows instead

3. **Check Featured Project Image:**
   - Scroll to "Featured Project" section
   - Should see main building image

4. **Check Gallery:**
   - Scroll to gallery section
   - All 5-6 images should display

5. **Check Footer:**
   - Scroll to bottom
   - Logo should appear (or text fallback)
   - Modern footer design visible

6. **Test Brochure Download:**
   - Click "Download Brochure"
   - Fill form
   - Submit
   - File should be 2.5MB and open correctly

7. **Test Direct URLs:**
   ```
   https://your-site.vercel.app/assets/prarambh-logo.png
   https://your-site.vercel.app/images/vimal-paradise-main.jpg
   https://your-site.vercel.app/brochures/vimal-paradise-brochure.pdf
   ```
   All should download/display correctly

---

## 🐛 **TROUBLESHOOTING**

### **Images Still Not Showing?**

**Problem 1: Files not on GitHub**
- Check GitHub repository
- Verify files are there with correct names
- Check file sizes (not 0 KB)

**Solution:**
```bash
git add images/ assets/ brochures/
git commit -m "Added all media files"
git push
```

**Problem 2: Wrong file names**
- Names are case-sensitive
- Must match EXACTLY
- No spaces, use hyphens

**Solution:** Rename files:
```bash
# In images folder
mv "Your Image.jpg" vimal-paradise-main.jpg
mv "Gallery 1.jpg" gallery-1.jpg
# etc.
```

**Problem 3: Files too large**
- GitHub has 100MB file limit (you're fine)
- But optimize for web:
  - Images: compress to ~500KB each
  - PDF: compress if over 10MB

**Problem 4: Cache issue**
- Hard refresh: `Ctrl+Shift+R`
- Clear browser cache completely
- Try Incognito/Private mode

---

### **Logo Not Showing?**

**Check:**
1. File exists at `assets/prarambh-logo.png`
2. File is actually PNG or JPG
3. File isn't corrupted
4. Try accessing directly: `your-site.vercel.app/assets/prarambh-logo.png`

**Fallback:**
- If logo doesn't load, text "PRARAMBH GROUP" shows automatically
- No broken images

---

### **Brochure Download Still 4KB?**

**This means PDF is NOT uploaded to GitHub.**

**Fix:**
1. Verify PDF is in `brochures/` folder on GitHub
2. Check file size shows as 2.5MB (not 4KB)
3. Test direct URL: `your-site.vercel.app/brochures/vimal-paradise-brochure.pdf`
4. Should download full PDF directly

**If still 4KB:**
```bash
# Re-upload the PDF
cp /path/to/actual/brochure.pdf brochures/vimal-paradise-brochure.pdf
git add brochures/vimal-paradise-brochure.pdf
git commit -m "Uploaded actual brochure PDF"
git push
```

---

## 📊 **FILE SIZE REFERENCE**

Typical file sizes:

| File Type | Recommended Size | Maximum |
|-----------|-----------------|---------|
| Project Images | 300KB - 800KB | 2MB |
| Gallery Images | 200KB - 500KB | 1MB |
| Logo PNG | 50KB - 200KB | 500KB |
| Brochure PDF | 1MB - 5MB | 10MB |

**Optimize images:**
- Use tools like TinyPNG.com
- Export at 80% quality
- Resize to recommended dimensions

---

## 🎯 **QUICK SUMMARY**

**What to upload:**
1. 6 images to `images/` folder
2. 1 logo to `assets/` folder
3. 1 PDF to `brochures/` folder

**File names (EXACT):**
- vimal-paradise-main.jpg
- gallery-1.jpg through gallery-5.jpg
- prarambh-logo.png
- vimal-paradise-brochure.pdf

**How to upload:**
- Via GitHub website (drag & drop)
- OR via command line (git add, commit, push)

**After upload:**
- Wait 30 seconds
- Hard refresh browser
- Test all images and download

---

## 💡 **PRO TIPS**

1. **Batch Upload:** Upload all images at once (faster)
2. **Compress First:** Optimize images before uploading
3. **Test Locally:** Put files in folders and test with local server
4. **Backup:** Keep original high-res images separately
5. **Update Easily:** Just replace file with same name, commit, push

---

**Once you upload these 8 files (6 images + 1 logo + 1 PDF), your website will be complete!** 🎉