# 🌐 Web3Forms Setup Guide

## ✅ What You Have Now

Your website has TWO lead generation forms:

1. **Contact Form** - "Schedule Consultation" button
2. **Brochure Download Form** - "Download Brochure" button (with automatic PDF download)

Both forms are configured to use **Web3Forms** (100% free, unlimited submissions).

---

## 🚀 Quick Setup (5 Minutes)

### Step 1: Get Your Web3Forms Access Key

1. Go to [web3forms.com](https://web3forms.com)
2. Enter your email address
3. Click "Create Access Key"
4. Check your email inbox
5. Copy your Access Key (looks like: `a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6`)

### Step 2: Update Your Website

Open `index.html` and find these TWO locations:

#### Location 1: Contact Form (around line 750)
```html
<form id="contactForm" action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
```

#### Location 2: Brochure Form (around line 785)
```html
<form id="brochureForm" action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
```

Replace **BOTH** instances of `YOUR_WEB3FORMS_ACCESS_KEY` with your actual key:

```html
<input type="hidden" name="access_key" value="a1b2c3d4-e5f6-7g8h-9i0j-k1l2m3n4o5p6">
```

### Step 3: Add Your Brochure PDF

1. Create/export your Vimal Paradise brochure as PDF
2. Name it exactly: `vimal-paradise-brochure.pdf`
3. Place it in the `brochures/` folder

Your structure should look like:
```
prarambh-group-website/
├── brochures/
│   └── vimal-paradise-brochure.pdf  ← Your PDF here
├── images/
├── index.html
└── ...
```

### Step 4: Deploy

```bash
git add .
git commit -m "Added Web3Forms and brochure download"
git push
```

Wait 30 seconds, hard refresh: `Ctrl+Shift+R`

### Step 5: Test

1. Click "Download Brochure"
2. Fill in the form
3. Click "Download Brochure" button
4. PDF should download automatically
5. Check your email for the lead notification

---

## 📧 How It Works

### Contact Form Flow:
1. User clicks "Schedule Consultation"
2. Modal opens with contact form
3. User fills in: Name, Email, Phone, Message
4. Form submits to Web3Forms
5. You receive email with lead details
6. User sees success message

### Brochure Download Flow:
1. User clicks "Download Brochure"
2. Modal opens with lead form
3. User fills in: Name, Email, Phone, Interest
4. Form submits to Web3Forms
5. You receive email with lead details
6. PDF download starts automatically
7. Modal closes

---

## 📊 Managing Your Leads

### Email Notifications

Every form submission sends you an email with:
- **Subject:** "New Contact Form Submission" or "Brochure Download Request"
- **From:** Web3Forms
- **Contains:** All form field data

**Tips:**
- Create email filter/label for organization
- Add web3forms.com to contacts
- Check spam folder initially

### Using the Same Access Key

✅ **Yes!** You can use the **same Access Key** for both forms.

They'll be differentiated by the subject line:
- Contact Form: "New Contact Form Submission - Prarambh Group"
- Brochure Form: "Brochure Download Request - Prarambh Group"

### Want Separate Keys?

You can use different keys if you want separate inboxes:
1. Get another access key for your sales team email
2. Update one of the forms with the new key
3. Now different people get different form submissions

---

## 🎨 Customization Options

### Change Brochure Filename

In `index.html`, find (around line 850):
```javascript
link.href = './brochures/vimal-paradise-brochure.pdf';
link.download = 'Vimal-Paradise-Brochure.pdf';
```

Change to:
```javascript
link.href = './brochures/your-filename.pdf';
link.download = 'Your-Custom-Name.pdf';
```

### Add More Brochures

Create multiple download buttons for different projects:

1. Add more PDFs to `brochures/` folder:
   ```
   brochures/
   ├── vimal-paradise-brochure.pdf
   ├── project-2-brochure.pdf
   └── company-profile.pdf
   ```

2. Add buttons in HTML:
   ```html
   <button onclick="openBrochureModal('vimal-paradise')">Vimal Paradise</button>
   <button onclick="openBrochureModal('project-2')">Project 2</button>
   ```

3. Update JavaScript to handle different projects

### Customize Form Fields

Add/remove fields in the brochure form:

```html
<!-- Add budget field -->
<div class="form-group">
    <label class="form-label" for="budget">Budget Range</label>
    <select id="budget" name="budget" class="form-input">
        <option value="">Select budget</option>
        <option value="50L-1Cr">₹50 Lakhs - ₹1 Crore</option>
        <option value="1Cr-2Cr">₹1 Crore - ₹2 Crore</option>
        <option value="2Cr+">₹2 Crore+</option>
    </select>
</div>
```

---

## 🔧 Troubleshooting

### Form not submitting?
1. Check access key is correct (no extra spaces)
2. Verify key is added to BOTH forms
3. Check browser console (F12) for errors

### Not receiving emails?
1. Check spam folder
2. Verify email used to create access key
3. Add noreply@web3forms.com to contacts
4. Check Web3Forms status page

### PDF not downloading?
1. Verify PDF is in `brochures/` folder
2. Check filename matches exactly: `vimal-paradise-brochure.pdf`
3. Ensure PDF is pushed to GitHub
4. Check browser console for 404 errors

### Download works locally but not on Vercel?
1. Ensure `brochures/` folder is in Git:
   ```bash
   git add brochures/
   git commit -m "Added brochure PDF"
   git push
   ```
2. Verify PDF path uses `./brochures/` (with `./`)

---

## 📁 File Structure

```
prarambh-group-website/
├── brochures/                           ← Your PDFs here
│   └── vimal-paradise-brochure.pdf     ← Main brochure
├── images/                              ← Your photos
│   ├── vimal-paradise-main.jpg
│   └── gallery-*.jpg
├── index.html                           ← Updated with forms
└── [other files]
```

---

## 💡 Pro Tips

### Track Conversions
- Count brochure downloads separately
- Different subject lines help identify source
- Use different access keys for A/B testing

### Follow Up Strategy
1. Brochure downloads = Hot leads
2. Contact form = Information seekers
3. Prioritize brochure leads for follow-up

### Create Multiple Brochures
- Project-specific brochures
- Floor plan PDFs
- Price sheets (gated)
- Company profile

### Add Analytics
Track which button gets more clicks:
```javascript
// Add this when button is clicked
gtag('event', 'brochure_download', {
    'event_category': 'Lead Generation',
    'event_label': 'Vimal Paradise'
});
```

---

## 🎯 Testing Checklist

Before going live:

- [ ] Got Web3Forms access key
- [ ] Updated BOTH forms with access key
- [ ] Added brochure PDF to `brochures/` folder
- [ ] Correct filename: `vimal-paradise-brochure.pdf`
- [ ] Pushed everything to GitHub
- [ ] Tested contact form submission
- [ ] Tested brochure download form
- [ ] PDF downloads successfully
- [ ] Received test emails
- [ ] Checked spam folder

---

## 📞 Next Steps

1. ✅ Get your Web3Forms access key
2. ✅ Update both forms in index.html
3. ✅ Add your brochure PDF to `brochures/` folder
4. ✅ Deploy to GitHub/Vercel
5. ✅ Test both forms
6. ✅ Start collecting leads! 🎉

---

## 🆓 Why Web3Forms is Perfect

- ✅ **100% Free** - No limits, no credit card
- ✅ **Unlimited** submissions
- ✅ **No setup fees**
- ✅ **Instant email notifications**
- ✅ **Spam protection** included
- ✅ **Simple integration**
- ✅ **No backend required**
- ✅ **Works anywhere**

---

**Your lead generation system is ready! Just add your access key and brochure PDF.** 🚀