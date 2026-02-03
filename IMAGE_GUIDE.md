# 📸 Image Upload Guide for Prarambh Group Website

## Quick Reference

You need **6 images** total. Create a folder called `images` in your project root.

```
📁 prarambh-group-website/
  📁 images/
    📷 vimal-paradise-main.jpg
    📷 gallery-1.jpg
    📷 gallery-2.jpg
    📷 gallery-3.jpg
    📷 gallery-4.jpg
    📷 gallery-5.jpg
```

---

## 📋 Detailed Image Specifications

### 🏢 Image 1: `vimal-paradise-main.jpg`

**Location on Website:** Project Section (main showcase)

**Recommended Dimensions:** 1600 x 1200 pixels (4:3 ratio)

**What to Photograph:**
- Main exterior view of Vimal Paradise
- Best architectural angle
- Daytime shot with good lighting
- Show full building if possible

**Tips:**
- This is the HERO image of your project
- Use your best, most professional photo
- Avoid shadows or harsh lighting
- Should make a strong first impression

**Example Shots:**
- Front elevation of building
- 3/4 angle showing depth
- Entrance and facade together

---

### 🎨 Image 2: `gallery-1.jpg`

**Location on Website:** Gallery Section (LARGE featured image - takes up 2x space)

**Recommended Dimensions:** 1600 x 1600 pixels (square, 1:1 ratio)

**What to Photograph:**
- Your most impressive shot
- Could be aerial view, full complex, or stunning architectural detail
- This appears LARGEST in the gallery

**Tips:**
- Premium quality required
- Landscape or compound view works well
- Drone shot if available
- Shows scale and grandeur

**Example Shots:**
- Aerial view of entire complex
- Bird's eye view showing layout
- Twilight shot of illuminated building
- Panoramic exterior view

---

### 🛋️ Image 3: `gallery-2.jpg`

**Location on Website:** Gallery Section

**Recommended Dimensions:** 800 x 800 pixels (square, 1:1 ratio)

**What to Photograph:**
- Interior spaces
- Living room, bedroom, or model apartment
- Modern, well-furnished spaces

**Tips:**
- Clean, staged interiors
- Good natural light
- Show spaciousness
- Professional interior photography

**Example Shots:**
- Model flat living room
- Modern kitchen
- Bedroom with furnishings
- Open-plan living area

---

### 🏊 Image 4: `gallery-3.jpg`

**Location on Website:** Gallery Section

**Recommended Dimensions:** 800 x 800 pixels (square, 1:1 ratio)

**What to Photograph:**
- Amenities and facilities
- Gym, swimming pool, clubhouse, etc.
- Community features

**Tips:**
- Show lifestyle benefits
- Active or inviting spaces
- Well-maintained facilities
- Highlight premium features

**Example Shots:**
- Swimming pool area
- Modern gym equipment
- Clubhouse lounge
- Children's play area
- Parking facilities

---

### 🌳 Image 5: `gallery-4.jpg`

**Location on Website:** Gallery Section

**Recommended Dimensions:** 800 x 800 pixels (square, 1:1 ratio)

**What to Photograph:**
- Landscaping and gardens
- Green spaces
- Outdoor areas
- Pathways and courtyards

**Tips:**
- Show natural elements
- Well-maintained gardens
- Peaceful outdoor spaces
- Greenery and open areas

**Example Shots:**
- Garden walkways
- Lawn areas
- Landscape design
- Outdoor seating areas
- Tree-lined paths

---

### 🏗️ Image 6: `gallery-5.jpg`

**Location on Website:** Gallery Section

**Recommended Dimensions:** 800 x 800 pixels (square, 1:1 ratio)

**What to Photograph:**
- Different exterior angle (from vimal-paradise-main.jpg)
- Building details
- Architectural features
- Entrance or facade closeup

**Tips:**
- Complement the main image
- Show different perspective
- Highlight design details
- Architectural elements

**Example Shots:**
- Side or rear elevation
- Entrance closeup
- Balcony details
- Building texture/materials
- Night view with lighting

---

## 🎯 General Photography Tips

### Quality Requirements
- ✅ High resolution (at least 1920px on longest side)
- ✅ Well-lit (natural light preferred)
- ✅ Sharp focus (not blurry)
- ✅ Professional composition
- ✅ Clean, clutter-free

### File Optimization
1. **Format:** Save as JPEG (.jpg)
2. **Compression:** 80-85% quality
3. **File size:** Keep under 500KB each
4. **Tools:** 
   - [TinyPNG.com](https://tinypng.com) - Free compression
   - [Squoosh.app](https://squoosh.app) - Google's tool
   - Photoshop: "Save for Web"

### Naming Rules
- ✅ Use lowercase letters
- ✅ Use hyphens (-) not spaces or underscores
- ✅ Be descriptive but concise
- ❌ Don't use: spaces, special characters, capital letters

---

## 📤 How to Add Images

### Step 1: Prepare Images
1. Collect your 6 photos
2. Edit/crop to recommended sizes
3. Optimize file sizes
4. Rename exactly as specified

### Step 2: Create Images Folder
```bash
# In your project directory
mkdir images
```

### Step 3: Add Images
- Place all 6 images in the `images` folder
- Double-check filenames match exactly

### Step 4: Verify
Your structure should look like:
```
prarambh-group-website/
├── images/
│   ├── vimal-paradise-main.jpg  ✓
│   ├── gallery-1.jpg            ✓
│   ├── gallery-2.jpg            ✓
│   ├── gallery-3.jpg            ✓
│   ├── gallery-4.jpg            ✓
│   └── gallery-5.jpg            ✓
├── index.html
├── styles.css
└── script.js
```

---

## 🔄 Alternative: If You Don't Have Professional Photos Yet

### Option 1: Use Placeholder Service
Replace image paths in `index.html` temporarily:
```html
<img src="https://placehold.co/1600x1200/e8e6e1/8b7355?text=Vimal+Paradise" alt="...">
```

### Option 2: Use Stock Photos Temporarily
- [Unsplash](https://unsplash.com) - Free architecture photos
- [Pexels](https://pexels.com) - Free building images
- Search: "modern apartment building", "luxury residential"

### Option 3: Hire a Photographer
- Budget: ₹5,000 - ₹15,000 for professional real estate shoot
- Include: Exteriors, interiors, amenities, drone shots

---

## ✅ Image Checklist

Before uploading to GitHub/Vercel:

- [ ] All 6 images collected
- [ ] Images properly sized (check dimensions above)
- [ ] Images optimized (file size < 500KB each)
- [ ] Filenames match exactly (lowercase, hyphens)
- [ ] Images placed in `images/` folder
- [ ] Tested website locally with real images
- [ ] Images look good on mobile and desktop

---

## 🆘 Troubleshooting

**Images not showing?**
- Check folder name is exactly `images` (lowercase, plural)
- Check filenames match exactly
- Check file extensions are `.jpg` not `.jpeg` or `.JPG`
- Make sure images are in the root `images` folder, not a subfolder

**Images too large?**
- Use TinyPNG.com to compress
- Reduce dimensions if needed
- Convert to JPEG if using PNG

**Images look pixelated?**
- Use higher resolution source images
- Don't upscale small images
- Maintain aspect ratios when resizing

---

Need help? Contact: info@prarambhgroup.com