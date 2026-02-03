# Prarambh Group Website

A minimalistic modern website for Prarambh Group showcasing the Vimal Paradise project.

## 🚀 Quick Start

### Deploy to Vercel

1. Push this repository to GitHub
2. Go to [Vercel](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Click "Deploy"

That's it! Vercel will automatically deploy your website.

## 📁 Project Structure

```
prarambh-group-website/
├── index.html          # Main HTML file
├── styles.css          # All CSS styles
├── script.js           # JavaScript functionality
├── images/             # Image folder (create this)
│   ├── vimal-paradise-main.jpg
│   ├── gallery-1.jpg
│   ├── gallery-2.jpg
│   ├── gallery-3.jpg
│   ├── gallery-4.jpg
│   └── gallery-5.jpg
└── README.md          # This file
```

## 🖼️ Image Requirements

### Create an `images` folder and add these photos:

#### 1. **vimal-paradise-main.jpg**
- **Purpose**: Main project showcase image
- **Recommended size**: 1600x1200px (4:3 ratio)
- **What to use**: Best exterior shot of Vimal Paradise building
- **Tips**: High-quality, well-lit photo showing the full building

#### 2. **gallery-1.jpg**
- **Purpose**: Large featured gallery image (takes 2x2 grid space)
- **Recommended size**: 1600x1600px (square)
- **What to use**: Most impressive aerial view, full building shot, or architectural highlight
- **Tips**: This is the hero image of the gallery - use your best photo

#### 3. **gallery-2.jpg**
- **Purpose**: Gallery image
- **Recommended size**: 800x800px (square)
- **What to use**: Interior shots - living room, bedroom, or common areas
- **Tips**: Show modern, well-designed interior spaces

#### 4. **gallery-3.jpg**
- **Purpose**: Gallery image
- **Recommended size**: 800x800px (square)
- **What to use**: Amenities - gym, pool, clubhouse, parking
- **Tips**: Highlight lifestyle features

#### 5. **gallery-4.jpg**
- **Purpose**: Gallery image
- **Recommended size**: 800x800px (square)
- **What to use**: Landscaping, gardens, outdoor spaces
- **Tips**: Show green areas, pathways, outdoor seating

#### 6. **gallery-5.jpg**
- **Purpose**: Gallery image
- **Recommended size**: 800x800px (square)
- **What to use**: Another exterior angle or building facade detail
- **Tips**: Different perspective from main image

### Image Optimization Tips

- **Format**: Use JPEG for photos
- **Quality**: 80-85% quality is optimal for web
- **Size**: Keep file sizes under 500KB each
- **Naming**: Use lowercase, hyphens (not spaces)
- **Tools**: Use tools like TinyPNG or Squoosh.app to compress

## 📝 Customization Guide

### Update Contact Information

Edit `index.html` lines with contact details:
- Email: Change `info@prarambhgroup.com`
- Phone: Change `+91 123 456 7890`
- Update any placeholder text

### Update Project Details

In the "Project Section" of `index.html`, update:
- Location
- Type
- Status
- Units

### Change Colors

Edit `styles.css` CSS variables at the top:
```css
:root {
    --primary-dark: #1a1a1a;
    --primary-light: #f8f7f4;
    --accent-gold: #d4af37;
    --accent-muted: #8b7355;
    --text-dark: #2c2c2c;
    --text-light: #666;
    --border-light: #e8e6e1;
}
```

## 🛠️ Local Development

1. Simply open `index.html` in your browser
2. Or use a local server:
   ```bash
   # If you have Python 3
   python -m http.server 8000
   
   # If you have Node.js
   npx serve
   ```

## 📤 GitHub Setup

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Prarambh Group website"

# Add your GitHub repository
git remote add origin https://github.com/yourusername/prarambh-group-website.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## 🌐 Vercel Deployment

### Method 1: Via GitHub (Recommended)
1. Push code to GitHub (see above)
2. Visit [vercel.com](https://vercel.com)
3. Sign in with GitHub
4. Click "New Project"
5. Import your repository
6. Click "Deploy"

### Method 2: Via Vercel CLI
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

### Method 3: Drag & Drop
1. Zip your project folder
2. Go to [vercel.com/new](https://vercel.com/new)
3. Drag and drop the zip file

## 📱 Features

- ✅ Fully responsive design
- ✅ Smooth scrolling navigation
- ✅ Animated elements on scroll
- ✅ Modern minimalist design
- ✅ Optimized for performance
- ✅ SEO-friendly structure
- ✅ Cross-browser compatible

## 🎨 Design Features

- Elegant serif typography (Cormorant Garamond)
- Clean sans-serif body text (Work Sans)
- Sophisticated neutral color palette
- Smooth animations and transitions
- Premium real estate aesthetic

## 📞 Support

For questions or issues, contact: info@prarambhgroup.com

---

Built with ❤️ for Prarambh Group