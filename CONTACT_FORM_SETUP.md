# 📧 Contact Form Setup Guide

## ✅ **What's Been Added**

Your website now has a **professional contact form modal** that:
- ✅ Opens when clicking "Schedule Consultation"
- ✅ Collects: Name, Email, Phone, Message
- ✅ Shows success/error messages
- ✅ Closes automatically after submission
- ✅ Works on mobile and desktop
- ✅ Styled to match your website design

---

## 🆓 **Recommended Free/Cheap Contact Form Services**

### **Option 1: Formspree (RECOMMENDED) ⭐**

**Price:** FREE for up to 50 submissions/month
**Paid:** $10/month for unlimited

**Why it's best:**
- ✅ Easiest setup (2 minutes)
- ✅ No backend code needed
- ✅ Email notifications
- ✅ Spam protection
- ✅ Works with any website

**Setup Steps:**

1. Go to [formspree.io](https://formspree.io)
2. Sign up (free account)
3. Click "New Form"
4. Copy your form endpoint (looks like: `https://formspree.io/f/xyzabc123`)
5. Update your `index.html`:

```html
<!-- Find this line around line 745 -->
<form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">

<!-- Replace YOUR_FORM_ID with your actual ID, like: -->
<form id="contactForm" action="https://formspree.io/f/xyzabc123" method="POST">
```

6. Done! Test your form

**Features:**
- Email notifications to your inbox
- View submissions in dashboard
- Export data to CSV
- Spam filtering
- Custom thank you page (paid)

---

### **Option 2: Web3Forms**

**Price:** 100% FREE forever
**Limits:** Unlimited submissions

**Why it's great:**
- ✅ Completely free
- ✅ No limits
- ✅ Spam protection
- ✅ Email notifications

**Setup Steps:**

1. Go to [web3forms.com](https://web3forms.com)
2. Enter your email
3. Get your Access Key (sent to email)
4. Update your form:

```html
<form id="contactForm" action="https://api.web3forms.com/submit" method="POST">
    <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
    
    <!-- Rest of your form fields -->
</form>
```

5. Update the JavaScript submit handler:

```javascript
// Replace the fetch URL with:
const response = await fetch('https://api.web3forms.com/submit', {
    method: 'POST',
    body: formData
});
```

---

### **Option 3: EmailJS**

**Price:** FREE for 200 emails/month
**Paid:** $7/month for 1000 emails

**Why use it:**
- ✅ Send from your own email
- ✅ Custom email templates
- ✅ Multiple email services (Gmail, Outlook, etc.)

**Setup Steps:**

1. Go to [emailjs.com](https://www.emailjs.com)
2. Sign up and verify email
3. Add email service (Gmail recommended)
4. Create email template
5. Get your Service ID, Template ID, and Public Key
6. Add EmailJS script to your HTML:

```html
<!-- Add before closing </head> -->
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>
<script>
    emailjs.init('YOUR_PUBLIC_KEY');
</script>
```

7. Update form submission code (detailed in EmailJS docs)

---

### **Option 4: Getform**

**Price:** FREE for 50 submissions/month
**Paid:** $9.99/month for 1000

**Setup:**
1. Go to [getform.io](https://getform.io)
2. Create form
3. Get form endpoint
4. Update action URL

---

### **Option 5: Basin (Simple)**

**Price:** FREE for 100 submissions/month
**Paid:** $5/month for 1000

Very similar to Formspree, equally easy setup.

---

## 🎯 **Quick Comparison**

| Service | Free Limit | Paid Price | Setup Time | Best For |
|---------|-----------|-----------|------------|----------|
| **Formspree** | 50/month | $10/month | 2 min | Most users ⭐ |
| **Web3Forms** | Unlimited | Free | 3 min | Budget projects |
| **EmailJS** | 200/month | $7/month | 5 min | Custom emails |
| **Getform** | 50/month | $10/month | 2 min | Alternative |
| **Basin** | 100/month | $5/month | 2 min | Cheap option |

---

## 📝 **Recommended: Formspree Setup (Step-by-Step)**

### 1. Create Formspree Account

```
1. Go to: https://formspree.io
2. Click "Get Started Free"
3. Sign up with email
4. Verify your email
```

### 2. Create New Form

```
1. Click "+ New Form" button
2. Name: "Prarambh Group - Contact"
3. Email: your@email.com (where submissions go)
4. Click "Create Form"
```

### 3. Copy Form Endpoint

You'll see something like:
```
https://formspree.io/f/mldejklw
```

### 4. Update Your Website

Open `index.html` and find (around line 745):

```html
<form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

Replace `YOUR_FORM_ID` with your actual ID:

```html
<form id="contactForm" action="https://formspree.io/f/mldejklw" method="POST">
```

### 5. Deploy to Vercel

```bash
git add index.html
git commit -m "Added Formspree contact form"
git push
```

### 6. Test

1. Visit your live site
2. Click "Schedule Consultation"
3. Fill out the form
4. Click "Send Message"
5. Check your email!

---

## 🎨 **Customization Options**

### Change Form Fields

Edit the HTML between `<form>` and `</form>`:

```html
<!-- Add a new field -->
<div class="form-group">
    <label class="form-label" for="budget">Budget Range</label>
    <select id="budget" name="budget" class="form-input">
        <option>Under ₹1 Crore</option>
        <option>₹1-2 Crore</option>
        <option>₹2-5 Crore</option>
        <option>Above ₹5 Crore</option>
    </select>
</div>
```

### Change Button Text

Find:
```html
<button type="submit" class="form-submit">Send Message</button>
```

Change to:
```html
<button type="submit" class="form-submit">Request Callback</button>
```

---

## 📊 **What Happens When Someone Submits**

1. User clicks "Schedule Consultation"
2. Modal opens with form
3. User fills in details
4. Clicks "Send Message"
5. Form data sent to Formspree
6. You receive email instantly
7. User sees success message
8. Modal closes automatically

---

## 💡 **Pro Tips**

### Enable Spam Protection (Formspree)
1. Go to your form in Formspree dashboard
2. Click "Settings"
3. Enable "reCAPTCHA" or "Akismet"

### Email Notifications
All services send you email when someone submits. Make sure to:
- Check spam folder
- Add service to contacts
- Set up email filters

### Track Submissions
- Formspree: Dashboard shows all submissions
- Download as CSV for lead management
- Integrate with CRM (paid plans)

---

## 🔧 **Troubleshooting**

### Form not submitting?
1. Check form action URL is correct
2. Verify service is active
3. Check browser console for errors (F12)
4. Test with simple email first

### Not receiving emails?
1. Check spam folder
2. Verify email in service dashboard
3. Add service email to contacts
4. Check service status page

### Modal not opening?
1. Hard refresh browser (Ctrl+Shift+R)
2. Check JavaScript console for errors
3. Verify button has onclick="openModal()"

---

## 🎯 **Recommended Workflow**

**For Small Budget (< 50 leads/month):**
Use Formspree Free → Upgrade if needed

**For Medium Budget (100-500 leads/month):**
Use Web3Forms (free unlimited) or Formspree paid

**For Professional Setup:**
Use EmailJS to send from your domain email

---

## 📞 **Next Steps**

1. ✅ Choose a service (Formspree recommended)
2. ✅ Sign up and get your form ID
3. ✅ Update index.html with your form ID
4. ✅ Commit and push to GitHub
5. ✅ Test the form on your live site
6. ✅ Check your email for test submission
7. ✅ Start receiving leads! 🎉

---

**Your contact form is ready to go! Just add your Formspree ID and deploy.** 🚀

Need help? All these services have excellent documentation and support.