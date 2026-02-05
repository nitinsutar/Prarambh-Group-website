# ⚡ QUICK START - Updated Version

## 🎉 What's New

1. ✅ **Web3Forms Integration** (100% free, unlimited)
2. ✅ **Contact Form** - Schedule Consultation button
3. ✅ **Brochure Download** - Lead generation + automatic PDF download
4. ✅ **Fixed Image Paths** - Images will display correctly
5. ✅ **Two Call-to-Actions** - Explore Work + Download Brochure

---

## 🚀 3-Step Setup

### Step 1: Get Web3Forms Access Key (2 minutes)

1. Go to [web3forms.com](https://web3forms.com)
2. Enter your email
3. Click "Create Access Key"
4. Check email and copy your key

### Step 2: Update Files (3 minutes)

**A. Add Access Key**

Open `index.html` and find **TWO** places with:
```html
<input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
```

Replace with your actual key in **BOTH** locations (around lines 750 and 785).

**B. Add Brochure PDF**

1. Create your brochure PDF
2. Name it: `vimal-paradise-brochure.pdf`
3. Place in `brochures/` folder

### Step 3: Deploy (2 minutes)

```bash
git add .
git commit -m "Added Web3Forms and brochure download"
git push
```

Hard refresh: `Ctrl+Shift+R` or `Cmd+Shift+R`

---

## 📁 Where to Put Files

### Your Images (Already Done ✓)
```
images/
├── vimal-paradise-main.jpg
├── gallery-1.jpg
├── gallery-2.jpg
├── gallery-3.jpg
├── gallery-4.jpg
└── gallery-5.jpg  (if you have it)
```

### Your Brochure (NEW - Add This)
```
brochures/
└── vimal-paradise-brochure.pdf  ← Your PDF here
```

**IMPORTANT:** 
- Filename must be exactly: `vimal-paradise-brochure.pdf`
- All lowercase
- Use hyphens (-)
- Must be .pdf extension

---

## 🎯 How It Works

### Contact Form ("Schedule Consultation")
1. User clicks button → Modal opens
2. User fills form → Submits
3. You get email with lead details
4. User sees success message

### Brochure Download ("Download Brochure")
1. User clicks button → Modal opens
2. User fills form → Submits
3. You get email with lead details
4. PDF downloads automatically for user
5. Modal closes

**Both forms send you emails via Web3Forms!**

---

## ✅ Complete Checklist

- [ ] Downloaded ZIP file
- [ ] Got Web3Forms access key from web3forms.com
- [ ] Updated index.html with access key (2 places)
- [ ] Created brochure PDF
- [ ] Named it: `vimal-paradise-brochure.pdf`
- [ ] Placed PDF in `brochures/` folder
- [ ] Images already uploaded to GitHub ✓
- [ ] Committed all changes
- [ ] Pushed to GitHub
- [ ] Waited 30 seconds
- [ ] Hard refreshed browser
- [ ] Tested contact form
- [ ] Tested brochure download
- [ ] Received test emails

---

## 📧 Email Configuration

Web3Forms will send emails to the email you used to create the access key.

**Email Subjects:**
- Contact Form: "New Contact Form Submission - Prarambh Group"
- Brochure Form: "Brochure Download Request - Prarambh Group"

**Tip:** Create email filters/labels to organize leads!

---

## 🎨 What Users See

### Hero Section (Top of Page)
- "Explore Our Work" button (scrolls to projects)
- "Download Brochure" button (opens download form)

### Contact Section (Bottom of Page)
- "Schedule Consultation" button (opens contact form)

---

## 📖 Detailed Documentation

- **WEB3FORMS_SETUP.md** - Complete Web3Forms guide
- **IMAGE_FIX_GUIDE.md** - Image display troubleshooting
- **CONTACT_FORM_SETUP.md** - General form services info
- **DEPLOYMENT_GUIDE.md** - Full GitHub/Vercel guide

---

## 🔧 Need to Change Brochure?

1. Replace PDF in `brochures/` folder
2. Keep same filename: `vimal-paradise-brochure.pdf`
3. Push to GitHub:
   ```bash
   git add brochures/
   git commit -m "Updated brochure"
   git push
   ```

---

## 💡 Pro Tips

1. **Use the same Access Key** for both forms (simpler)
2. **Check spam folder** for test emails initially
3. **Add web3forms.com to contacts** to avoid spam
4. **Test forms before announcing** your website
5. **Brochure downloads = Hot leads** - follow up fast!

---

## ⚠️ Common Issues

### Images not showing?
- Hard refresh: `Ctrl+Shift+R`
- Check images are in GitHub `images/` folder
- Verify filenames match exactly (case-sensitive)

### Forms not submitting?
- Check access key is correct (no spaces)
- Make sure it's in BOTH form locations
- Check browser console (F12) for errors

### PDF not downloading?
- Verify filename: `vimal-paradise-brochure.pdf`
- Check it's in `brochures/` folder
- Ensure it's pushed to GitHub
- Must be in GitHub for Vercel to serve it

---

## 🎉 You're Ready!

Your website now has:
- ✅ Beautiful design
- ✅ Two lead generation forms
- ✅ Automatic brochure downloads
- ✅ Email notifications for all leads
- ✅ Mobile-responsive design
- ✅ Professional appearance

**Just add your Web3Forms key and brochure PDF, then deploy!** 🚀

---

**Estimated Time:** 10 minutes total to be fully live with lead generation!